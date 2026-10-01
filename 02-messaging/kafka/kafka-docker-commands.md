# Câu lệnh để check trang kafka docker:

## Sơ đồ: gặp tình huống nào thì dùng lệnh nào

```mermaid
flowchart TD
    START([Cần kiểm tra Kafka]) --> Q{Muốn biết điều gì?}

    Q -->|"Kafka có đang chạy không?<br/>có mấy broker?"| C1["14.1 kafka-broker-api-versions.sh"]
    Q -->|"Có những topic nào?"| C2["14.2 kafka-topics.sh --list"]
    Q -->|"Topic chia mấy partition?<br/>leader / replica / ISR là gì?"| C3["14.3 kafka-topics.sh --describe"]
    Q -->|"Trong topic có message gì?"| C4["14.4 kafka-console-consumer.sh"]
    Q -->|"Muốn gửi thử 1 message"| C5["14.5 kafka-console-producer.sh"]
    Q -->|"Consumer có xử lý kịp không?"| C6["14.6 kafka-consumer-groups.sh"]
    Q -->|"Topic có bao nhiêu message?"| C7["14.7 GetOffsetShell"]

    C4 --> C4a["Thêm --partition 0<br/>để chỉ đọc 1 partition"]
    C4 --> C4b["Thêm --property print.key=true<br/>--property print.timestamp=true<br/>để xem key và timestamp"]

    C6 --> C6a["--list: xem các group"]
    C6 --> C6b["--describe --group tên-group:<br/>cột LAG = số message còn chậm"]
```

## Chuỗi debug thường gặp

```mermaid
flowchart LR
    A["Producer gửi rồi<br/>nhưng consumer không nhận"] --> B["14.2 Topic có tồn tại chưa?"]
    B --> C["14.4 Message đã nằm trong topic chưa?"]
    C --> D["14.6 Consumer group có LAG không?"]
    D --> E["14.3 Xem lại partition / leader"]
```

14.1. Xem danh sách broker / thông tin cluster

```bash
docker compose exec kafka /opt/kafka/bin/kafka-broker-api-versions.sh --bootstrap-server localhost:9092
```
Vì đây là single-node KRaft nên chỉ có 1 broker (node id = 1).

14.2. Danh sách topic

```bash
docker compose exec kafka /opt/kafka/bin/kafka-topics.sh --bootstrap-server localhost:9092 --list
```

14.3. Xem chi tiết 1 topic (partition, replica, leader, ISR)

```bash
docker compose exec kafka /opt/kafka/bin/kafka-topics.sh --bootstrap-server localhost:9092 --describe --topic <ten-topic>
```
Không truyền --topic sẽ describe tất cả topic.
```bash
docker compose exec kafka /opt/kafka/bin/kafka-topics.sh --bootstrap-server localhost:9092 --describe --exclude-internal
```

14.4. Đọc message trong topic

Từ đầu topic:
```bash
docker compose exec kafka /opt/kafka/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic <ten-topic> --from-beginning
```
Chỉ đọc 1 partition cụ thể:
```bash
docker compose exec kafka /opt/kafka/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic <ten-topic> --partition 0 --from-beginning
```
Xem cả key + timestamp:
```bash
docker compose exec kafka /opt/kafka/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic <ten-topic> --from-beginning --property print.key=true --property print.timestamp=true
```
Nhấn Ctrl+C để thoát (nó là lệnh chạy liên tục theo kiểu tail -f).

14.5. Gửi thử message (test producer)

```bash
docker compose exec kafka /opt/kafka/bin/kafka-console-producer.sh --bootstrap-server localhost:9092 --topic <ten-topic>
```
Gõ nội dung rồi Enter để gửi, Ctrl+C để thoát.

14.6. Xem consumer group & lag (rất hữu ích để debug backend/mail-service/inventory-service có đang consume kịp không)

```bash
docker compose exec kafka /opt/kafka/bin/kafka-consumer-groups.sh --bootstrap-server localhost:9092 --list
docker compose exec kafka /opt/kafka/bin/kafka-consumer-groups.sh --bootstrap-server localhost:9092 --describe --group <group-id>
```
Cột LAG cho biết consumer đang chậm bao nhiêu message.

14.7. Đếm số message trong topic

```bash
docker compose exec kafka /opt/kafka/bin/kafka-run-class.sh kafka.tools.GetOffsetShell --broker-list localhost:9092 --topic <ten-topic>
```
Kết quả trả về offset cuối mỗi partition (partition:offset:count-ish, cần cộng dồn theo partition).
