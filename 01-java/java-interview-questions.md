# Câu hỏi phỏng vấn Java và các chủ đề liên quan
> Tổng hợp câu hỏi phỏng vấn kèm câu trả lời (bản dịch tiếng Việt từ ghi chú tiếng Anh): OOP, Java core, Collection, Exception, đa luồng, bảo mật API, Spring, Agile, design pattern.

## Mục lục

- [Câu hỏi phỏng vấn Java và các chủ đề liên quan](#câu-hỏi-phỏng-vấn-java-và-các-chủ-đề-liên-quan)
  - [Mục lục](#mục-lục)
  - [Bốn nguyên lý chính của OOP là gì?](#bốn-nguyên-lý-chính-của-oop-là-gì)
  - [Sự khác nhau giữa abstract class (bản thiết kế) và interface (hành vi chung)?](#sự-khác-nhau-giữa-abstract-class-bản-thiết-kế-và-interface-hành-vi-chung)
  - [Sự khác nhau giữa method overloading và method overriding?](#sự-khác-nhau-giữa-method-overloading-và-method-overriding)
  - [Các access modifier trong Java?](#các-access-modifier-trong-java)
  - [Có thể có nhiều class trong một file không?](#có-thể-có-nhiều-class-trong-một-file-không)
  - [Từ khóa super trong Java dùng để làm gì?](#từ-khóa-super-trong-java-dùng-để-làm-gì)
  - [Sự khác nhau giữa biến local và biến instance trong Java?](#sự-khác-nhau-giữa-biến-local-và-biến-instance-trong-java)
  - [Collections framework là gì?](#collections-framework-là-gì)
  - [Sự khác nhau giữa ArrayList và LinkedList?](#sự-khác-nhau-giữa-arraylist-và-linkedlist)
  - [HashMap và TreeMap](#hashmap-và-treemap)
  - [Sự khác nhau giữa checked và unchecked exception?](#sự-khác-nhau-giữa-checked-và-unchecked-exception)
  - [Khối try-catch trong Java dùng để làm gì?](#khối-try-catch-trong-java-dùng-để-làm-gì)
  - [Cách hiện thực việc so sánh bằng (equality) trong Java, giữa hai object hoặc hai class?](#cách-hiện-thực-việc-so-sánh-bằng-equality-trong-java-giữa-hai-object-hoặc-hai-class)
  - [Bạn biết gì về synchronization trong Java?](#bạn-biết-gì-về-synchronization-trong-java)
  - [Về Collection trong Java (Collection framework)?](#về-collection-trong-java-collection-framework)
  - [HashSet dùng để làm gì? Sự khác nhau giữa HashSet và SortedSet?](#hashset-dùng-để-làm-gì-sự-khác-nhau-giữa-hashset-và-sortedset)
  - [Sự khác nhau giữa Vector và ArrayList trong Java?](#sự-khác-nhau-giữa-vector-và-arraylist-trong-java)
  - [Xử lý exception trong Java? Các từ khóa chính?](#xử-lý-exception-trong-java-các-từ-khóa-chính)
  - [Có thể có nhiều catch dưới một khối try không?](#có-thể-có-nhiều-catch-dưới-một-khối-try-không)
  - [Nếu muốn một catch cho một exception và có nhiều catch dưới một try, thì cần tuân theo quy tắc nào?](#nếu-muốn-một-catch-cho-một-exception-và-có-nhiều-catch-dưới-một-try-thì-cần-tuân-theo-quy-tắc-nào)
  - [Còn Custom Exception thì sao?](#còn-custom-exception-thì-sao)
  - [Còn Java String Pool thì sao?](#còn-java-string-pool-thì-sao)
  - [Làm thế nào để phòng tránh deadlock?](#làm-thế-nào-để-phòng-tránh-deadlock)
  - [Làm thế nào để bảo mật API (phía BE)?](#làm-thế-nào-để-bảo-mật-api-phía-be)
  - [Nói chung hơn, làm thế nào để hiện thực xác thực (authentication) cho người dùng? Hoặc session?](#nói-chung-hơn-làm-thế-nào-để-hiện-thực-xác-thực-authentication-cho-người-dùng-hoặc-session)
  - [Làm thế nào để kiểm tra quyền (permission) của người dùng? Lấy quyền người dùng từ đâu?](#làm-thế-nào-để-kiểm-tra-quyền-permission-của-người-dùng-lấy-quyền-người-dùng-từ-đâu)
  - [Làm thế nào để viết REST API?](#làm-thế-nào-để-viết-rest-api)
  - [Làm thế nào để hiện thực API Versioning?](#làm-thế-nào-để-hiện-thực-api-versioning)
  - [Ai là người nhận yêu cầu (requirements)?](#ai-là-người-nhận-yêu-cầu-requirements)
  - [Bạn đã từng làm việc với Agile chưa? Làm việc theo sprint không?](#bạn-đã-từng-làm-việc-với-agile-chưa-làm-việc-theo-sprint-không)
  - [Phát triển phần mềm trong nghiên cứu lâm sàng khác gì so với các lĩnh vực khác (như phần mềm văn phòng, game, logistics)?](#phát-triển-phần-mềm-trong-nghiên-cứu-lâm-sàng-khác-gì-so-với-các-lĩnh-vực-khác-như-phần-mềm-văn-phòng-game-logistics)
  - [Thiết kế mô hình cây có độ sâu thay đổi như thế nào?](#thiết-kế-mô-hình-cây-có-độ-sâu-thay-đổi-như-thế-nào)
  - [Command pattern là gì? Ứng dụng hữu ích của pattern này?](#command-pattern-là-gì-ứng-dụng-hữu-ích-của-pattern-này)
  - [Dependency Injection](#dependency-injection)
  - [Vấn đề khó nhất bạn từng gặp?](#vấn-đề-khó-nhất-bạn-từng-gặp)
  - [Optional và NullPointerException](#optional-và-nullpointerexception)
  - [Nguồn tham khảo](#nguồn-tham-khảo)

---

## Bốn nguyên lý chính của OOP là gì?

- Lập trình hướng đối tượng (OOP) là một cách lập trình cho phép lập trình viên tạo và làm việc với các đối tượng (object) trong code.

OOP được xây dựng trên bốn nguyên lý chính:

**Inheritance (Kế thừa):** Cho phép một class kế thừa các field và method từ class khác, giúp tái sử dụng code, mở rộng dễ hơn và giảm trùng lặp. Có 4 loại kế thừa:

- Single inheritance (đơn kế thừa) – một subclass kế thừa một superclass.
- Multi-level inheritance (kế thừa nhiều cấp) – một class kế thừa một subclass của class khác.
- Hierarchical inheritance (kế thừa phân cấp) – nhiều class kế thừa cùng một superclass.
- Multiple inheritance (đa kế thừa) – một class kế thừa nhiều kiểu cùng lúc; trong Java chỉ thực hiện được qua interface.

**Encapsulation (Đóng gói):** gom các field hoặc method liên quan vào một class duy nhất và hạn chế truy cập trực tiếp vào dữ liệu đó. Được thể hiện bằng cách khai báo field là private và cung cấp các getter/setter public.

**Polymorphism (Đa hình):** Một đối tượng có thể thể hiện các hành vi khác nhau tùy theo ngữ cảnh. Trong Java, điều này xuất hiện dưới dạng method overloading (cùng tên method, khác danh sách tham số), method overriding (subclass cung cấp cách hiện thực riêng cho một method của superclass).

**Abstraction (Trừu tượng):** Ẩn chi tiết hiện thực và chỉ phơi ra các method cần thiết. Được thể hiện thông qua abstract class hoặc interface.

## Sự khác nhau giữa abstract class (bản thiết kế) và interface (hành vi chung)?

Abstract class được khai báo bằng từ khóa abstract, và một class chỉ có thể extend một abstract class (hoặc class thường). Nó có thể chứa biến instance để lưu trạng thái (state), và cũng có thể định nghĩa constructor.

Ví dụ: Tôi sẽ xây dựng một dự án đặt vé du lịch. Tôi tạo một abstract class Vehicle với các field như mã chuyến đi, điểm khởi hành, điểm đến, giá cơ bản, và một method cụ thể tên là showTripInfo(). Mỗi loại phương tiện (Bus, Airplane) override abstract method calculatePrice. Tôi chọn abstract class thay vì interface vì tôi cần state và khả năng tái sử dụng, và tất cả phương tiện đều có quan hệ is-a (là một) vehicle rõ ràng.

Interface được khai báo bằng từ khóa interface, và một class có thể implement nhiều interface. Trong interface, tất cả field mặc định (implicitly) là public static final (hằng số), và đây là lý do interface không thể chứa biến instance để lưu state. Từ Java 8 trở lên, method có từ khóa static hoặc default có thể có phần thân.

Ví dụ: Trong hệ thống e-commerce của tôi, tôi tạo một interface generic BaseRepository<T> với các method như add, delete và findById. Tất cả repository (UserRepository, ProductRepository, v.v.) implement interface này và cung cấp logic của riêng chúng.

Tôi chọn interface thay vì abstract class vì:

- Không có state hay thuộc tính dùng chung, chỉ có các hợp đồng (contract) về method.
- Nó cho phép đa kế thừa, nên mỗi repository có thể implement thêm các interface khác nếu cần.

Dùng abstrac t class sẽ không cần thiết và làm giảm tính linh hoạt của kế thừa.

## Sự khác nhau giữa method overloading và method overriding?

**Method Overriding:** Dùng để thay đổi hoặc mở rộng method của superclass. Method phải giống với method trong superclass (cùng tên, cùng danh sách tham số, và cùng kiểu trả về hoặc kiểu con của nó (covariant)).

Ví dụ: Tôi cần các thao tác cơ bản giống nhau cho tất cả entity, như add, findById và delete. Tôi định nghĩa một interface generic BaseRepository<T> chứa các method này. Mỗi repository cụ thể, như userRepository hay ProductRepository, implement interface và override các method để viết logic query riêng.

**Method Overloading:** Cho phép một class có nhiều method cùng tên nhưng khác danh sách tham số (khác số lượng hoặc kiểu tham số).

Ví dụ: Tôi cần lấy dữ liệu để hiển thị lên màn hình, nhưng mỗi trang chỉ cần một số field nhất định của entity. Để giữ cho gọn, tôi tạo một class Converter với nhiều method đều tên là convert, nhưng khác tham số và kiểu trả về, chẳng hạn:

- convert(User entity) → trả về UserDto
- convert(Product entity) → trả về ProductDto

Khi gọi converter, Java tự động chọn đúng method dựa trên kiểu của tham số.

## Các access modifier trong Java?

Java cung cấp bốn mức kiểm soát truy cập: public, protected, default và private.

- **Public:** truy cập được từ mọi nơi - trong cùng class, cùng package, khác package.
- **protected** về phạm vi: cùng class, cùng package, subclass (kể cả khi ở package khác).
- **default (package-private):** khi bạn không chỉ định modifier nào. Phạm vi: chỉ cùng class và cùng package.
- **private:** chỉ truy cập được bên trong chính class nơi nó được định nghĩa.

## Có thể có nhiều class trong một file không?

Có, Java cho phép có nhiều class trong một file Java, nhưng chỉ một class được khai báo là public, và tên file phải trùng với tên của class public đó. Lý do là: Biên dịch và tra cứu dễ hơn, quản lý và bảo trì đơn giản hơn, và tránh xung đột tên.

## Từ khóa super trong Java dùng để làm gì?

super dùng để gọi constructor, method, hoặc biến của class cha, giúp bạn kiểm soát việc kế thừa trong Java.

## Sự khác nhau giữa biến local và biến instance trong Java?

Biến local được khai báo và có phạm vi bên trong một method, constructor hoặc block. Nó được tạo khi method được gọi (invoke) và bị hủy khi method kết thúc. Nó phải được khởi tạo trước khi dùng và được lưu trong stack memory.

Biến instance được khai báo bên trong class nhưng bên ngoài mọi method. Nó gắn với từng object và tồn tại cho đến khi object bị garbage-collected. Nếu bạn không khởi tạo tường minh, Java tự động gán giá trị mặc định (như 0, false hoặc null). Biến instance được lưu trong heap memory.

## Collections framework là gì?

Java Collections Framework là một framework cung cấp các interface, class và thuật toán (algorithm) để quản lý các nhóm đối tượng (như list, set và map) một cách nhất quán và hiệu quả.

## Sự khác nhau giữa ArrayList và LinkedList?

ArrayList dùng mảng động (dynamic array), truy cập nhanh và duyệt hiệu quả, nhưng chèn hoặc xóa ở giữa chậm (O(n)) vì các phần tử phải được dịch chuyển.

LinkedList là danh sách liên kết đôi (doubly linked list), hỗ trợ chèn/xóa nhanh sau khi đã xác định được node (O(1)), nhưng truy cập ngẫu nhiên chậm (O(n)) và tốn nhiều bộ nhớ hơn.

## HashMap và TreeMap

HashMap dùng bảng băm (hash table), tra cứu rất nhanh, cho phép một key null và nhiều value null, nhưng không duy trì thứ tự key nào.

TreeMap giữ các key được sắp xếp tự động (thứ tự tự nhiên hoặc một Comparator tùy chỉnh), cho phép value null, nhưng không cho phép key null.

## Sự khác nhau giữa checked và unchecked exception?

Checked exception được kiểm tra ở compile time. Bạn cần xử lý bằng try-catch hoặc throws. Chúng thường do yếu tố bên ngoài gây ra.

Unchecked exception xảy ra ở run time. Chúng thường do lỗi logic trong quá trình phát triển tính năng.

## Khối try-catch trong Java dùng để làm gì?

try-catch dùng để bao bọc các exception có thể xuất hiện, ngăn chương trình dừng đột ngột. Khối try chứa code có thể ném ra exception, và nếu nó xảy ra, luồng thực thi nhảy sang khối catch để xử lý.

Có thể dùng nhiều khối catch để quản lý các loại exception khác nhau. Cách này giúp tránh việc kết thúc ngoài ý muốn.

Dùng finally để dọn dẹp hoặc đóng tài nguyên và đảm bảo đoạn code này luôn chạy, dù có lỗi xảy ra hay không.

## Cách hiện thực việc so sánh bằng (equality) trong Java, giữa hai object hoặc hai class?

Trong Java, equality được định nghĩa ở mức object, không phải mức class.

Theo mặc định, Object.equals() so sánh hai tham chiếu object, nghĩa là hai object chỉ bằng nhau khi chúng trỏ tới cùng một địa chỉ bộ nhớ.

Để so sánh giá trị của object, ta override method equals và định nghĩa logic dựa trên giá trị, và cũng phải override hashCode() để đảm bảo hoạt động đúng trong các collection dựa trên hash.

## Bạn biết gì về synchronization trong Java?

- Synchronization là cơ chế ngăn nhiều thread truy cập đồng thời vào tài nguyên dùng chung, tránh race condition và đảm bảo tính nhất quán dữ liệu.
- Java cung cấp synchronization bằng từ khóa "synchronized", có thể áp dụng cho method hoặc khối code.

## Về Collection trong Java (Collection framework)?

- Collection là kiến trúc thống nhất dùng để lưu trữ và thao tác một nhóm đối tượng.
- Nó cung cấp interface, class và thuật toán hỗ trợ các thao tác phổ biến như thêm, cập nhật, xóa và tìm kiếm.
- Framework bao gồm các interface cốt lõi như list, set, queue và map, các class hiện thực cụ thể như ArrayList, Vector và HashSet, cung cấp các hành vi và đặc tính hiệu năng khác nhau.

## HashSet dùng để làm gì? Sự khác nhau giữa HashSet và SortedSet?

- HashSet dùng để lưu các phần tử duy nhất với hiệu năng tra cứu nhanh. Nhưng nó không duy trì thứ tự chèn. Cho phép một giá trị null.
- SortedSet (TreeSet) cũng dùng để lưu các phần tử duy nhất nhưng nó được sắp xếp khi bạn chèn. Không cho phép một giá trị null. Vì chúng cần so sánh giữa các phần tử.

Nếu bạn ưu tiên hiệu năng, bạn có thể dùng HashSet, và nếu ưu tiên

> Câu trả lời gốc bị cắt ở đây.

## Sự khác nhau giữa Vector và ArrayList trong Java?

Cả ArrayList và Vector đều là mảng động (dynamic array) implement interface List. Khác biệt chính là vector được đồng bộ (synchronized) và thread-safe, trong khi ArrayList không được đồng bộ nên nhanh hơn. Ngoài ra, arraylist tăng dung lượng 50% khi đầy, còn Vector thì tăng gấp đôi dung lượng.

## Xử lý exception trong Java? Các từ khóa chính?

- Xử lý exception trong Java dùng để xử lý lỗi runtime và ngăn chương trình dừng đột ngột.
- Các từ khóa chính là try, catch, finally, throw, throws.
  - Khối try chứa code có thể ném ra exception.
  - Khối catch dùng để xử lý exception nếu nó xảy ra.
  - Khối finally dùng để dọn dẹp tài nguyên như đóng file hoặc kết nối database.
  - Từ khóa throw dùng để ném một exception cụ thể lúc runtime.
  - Từ khóa throws dùng trong khai báo method để khai báo các exception mà method có thể ném ra.

## Có thể có nhiều catch dưới một khối try không?

Có, bạn có thể có nhiều khối catch dưới một câu lệnh try duy nhất.
Bạn phải đặt exception cụ thể trước, rồi mới đặt exception tổng quát, chẳng hạn Exception ở cuối.
Chỉ một khối catch được thực thi - khối đầu tiên khớp với exception được ném ra.

## Nếu muốn một catch cho một exception và có nhiều catch dưới một try, thì cần tuân theo quy tắc nào?

Chúng ta phải tuân theo quy tắc sắp xếp các khối catch từ exception cụ thể nhất đến tổng quát nhất, vì trình biên dịch (compiler) kiểm tra phân cấp exception (exception hierarchy).

## Còn Custom Exception thì sao?

Java cho phép ta tạo custom exception bằng cách định nghĩa một class mới extend class Exception hoặc RuntimeException, rồi ném nó bằng từ khóa throw.
Cái này gọi là custom Exception.
Ta tạo custom exception khi các exception có sẵn của Java không bao phủ được logic nghiệp vụ cụ thể cho tình huống đó.
Để tạo globalException sử dụng Annotation @RestControllerAdvice (Write a single place to handle errors: When an exception occurs anywhere → it will be handled here.)

## Còn Java String Pool thì sao?

> Câu hỏi gốc ghi "Java Spring Pool"; đã sửa thành String Pool theo yêu cầu của chủ repo.

String pool là một vùng nhớ đặc biệt bên trong heap dùng để lưu các string literal.
Khi ta tạo một string literal, JVM kiểm tra xem giá trị giống vậy đã tồn tại trong pool chưa.
Nếu đã tồn tại, máy ảo Java (java visual machine) trả về tham chiếu tới object có sẵn thay vì tạo object mới.
Nếu chưa tồn tại, một object String mới được tạo và thêm vào pool.

## Làm thế nào để phòng tránh deadlock?

- Khi nào deadlock xảy ra? Nó xảy ra khi bốn điều kiện cùng tồn tại: hold and wait, no preemption (không thể cưỡng chế thu hồi tài nguyên), circular wait, mutual exclusion (tài nguyên mang tính chất độc quyền, tại một thời điểm chỉ có 1 thread dùng được). Để phòng tránh deadlock, ta cần phá vỡ ít nhất một trong các điều kiện này.
- Các thread phải khóa tài nguyên theo cùng một thứ tự → tránh circular wait → tránh deadlock. Ta cũng có thể dùng ReentrantLock.tryLock() với timeout thay vì khối synchronized, để thread không phải chờ khóa vô thời hạn.

Ngoài ra, ta nên thu nhỏ phạm vi của các khối synchronized, tránh các khóa lồng nhau không cần thiết.

## Làm thế nào để bảo mật API (phía BE)?

Để bảo mật backend API (application programming interface), tôi áp dụng cách tiếp cận phòng thủ nhiều lớp (defense-in-depth).

- Đầu tiên, bắt buộc dùng HTTPS (Hypertext Transfer Protocol Secure) để đảm bảo mọi dữ liệu truyền đi đều được mã hóa.
- Sau đó hiện thực authentication (xác thực), thường là JWT hoặc OAuth2.
- Tôi áp dụng authorization (phân quyền) phù hợp để kiểm soát truy cập tài nguyên. Tôi lưu mật khẩu bằng các thuật toán băm mạnh như bcrypt kèm salt.
- Ngoài ra, áp dụng rate limiting, input validation, CORS (Cross origin resource sharing) và logging phù hợp.

## Nói chung hơn, làm thế nào để hiện thực xác thực (authentication) cho người dùng? Hoặc session?

Tôi sẽ lưu thông tin đăng nhập của người dùng an toàn trong database bằng mật khẩu đã băm với BCrypt. Khi đăng nhập, tôi sẽ kiểm tra thông tin và tạo ra server-side session hoặc JWT token. Session có thể được lưu trong Redis để dễ mở rộng. Tôi sẽ bảo mật hệ thống bằng HTTPS, secure cookie, bảo vệ CSRF (Cross-Site Request Forgery), rate limiting và phân quyền theo vai trò (role-based authorization).

## Làm thế nào để kiểm tra quyền (permission) của người dùng? Lấy quyền người dùng từ đâu?

Quyền của người dùng được lưu trong database và được nạp trong quá trình xác thực thông qua UserDetailsService.
Sau khi xác thực thành công, Spring Security tạo một đối tượng Authentication và lưu nó vào SecurityContext. SecurityContext sau đó có thể được lưu trong HTTP session hoặc dùng để tạo JWT token, tùy theo chiến lược xác thực.
Với mỗi request, Spring Security lấy lại hoặc dựng lại Authentication (từ session hoặc JWT) và thực hiện kiểm tra phân quyền trong Security Filter Chain dựa trên các quy tắc HttpSecurity.
Có thể áp dụng thêm bảo mật ở mức method bằng @PreAuthorize, nó lấy các authority của người dùng từ SecurityContext.

```
  ↓
1️⃣ Servlet Filter
   (Infrastructure layer)
   - Xử lý CORS
   - Rate limiting2
   - Logging
   - Encoding
   - Chưa biết user là ai (chưa qua Spring Security Filter Chain)
   - Không biết controller nào

  ↓
2️⃣ Spring Security Filter Chain
   (Security gateway layer)
   - Xác thực (Authentication → bạn là ai?)
   - Phân quyền (Authorization → bạn có quyền không?)
   - Tạo Authentication và lưu vào SecurityContext
   - Nếu fail → trả 401/403 tại đây
   - Không cho vào Spring MVC

  ↓
3️⃣ DispatcherServlet
   (MVC central dispatcher)
   - Là trái tim của Spring MVC
   - Nhận request từ container
   - Gọi HandlerMapping để tìm controller phù hợp

     ↓
     HandlerMapping
     - Dựa vào URL + HTTP method
     - Tìm method trong controller phù hợp

     ↓
4️⃣ HandlerInterceptor (preHandle)
   (MVC lifecycle hook)
   - Chạy trước khi gọi controller
   - Có thể:
       + Log request
       + Check custom header
       + Tracking
   - Nếu trả false → dừng request tại đây

     ↓
5️⃣ AOP Proxy(Aspect oriented programming) là một kỹ thuật cho phép chạy trước, sau hoặc bao quanh một method mà không cần sửa method đó
   (Method-level interception)
   - Bao quanh controller/service bean
   - Xử lý:
       + @PreAuthorize
       + @Transactional
       + @Cacheable
   - Kiểm tra quyền ở mức method
   - Nếu fail → throw exception

     ↓
6️⃣ Controller
   (Entry point của business logic)
   - Nhận request body
   - Validate (@Valid)
   - Gọi service
   - Không nên chứa business logic nặng

     ↓
7️⃣ Service
   (Business logic layer)
   - Xử lý nghiệp vụ chính
   - Có thể có @Transactional
   - Có thể có @PreAuthorize

     ↓
8️⃣ Repository
   (Data access layer)
   - Làm việc với database
   - Gọi JPA/Hibernate
   - Không chứa business logic
```

## Làm thế nào để viết REST API?

Để viết một REST API, tôi định nghĩa mô hình tài nguyên (resource model), tạo repository để truy cập dữ liệu, hiện thực business logic trong tầng service, và phơi các endpoint thông qua @RestController. Tôi tuân theo các nguyên tắc REST bằng cách dùng đúng HTTP method và status code. Tôi dùng DTO (Data transfer object) để truyền dữ liệu, các annotation validation để kiểm tra input, xử lý exception toàn cục (global exception handling), và bảo mật API bằng Spring Security nếu cần.

## Làm thế nào để hiện thực API Versioning?

> Câu hỏi gốc: Một số client dùng version 1, một số client dùng version 2 hoặc version 3. Bạn xử lý tất cả những thứ đó thế nào?

Để hiện thực API versioning, trước tiên tôi sẽ chọn một chiến lược versioning như URI versioning, header-based versioning, hoặc request parameter versioning. Cách phổ biến nhất là URI versioning như /api/v1/users và /api/v2/users. Tôi sẽ tạo các controller hoặc DTO riêng cho từng version trong khi tái sử dụng tầng service khi có thể. Điều này cho phép nhiều client dùng các version khác nhau cùng lúc mà không phá vỡ tính tương thích ngược (backward compatibility).

## Ai là người nhận yêu cầu (requirements)?

Trong Agile, Product Owner chịu trách nhiệm quản lý và ưu tiên hóa (prioritizing) các yêu cầu sản phẩm. Product Owner thu thập yêu cầu từ các stakeholder, những người cung cấp nhu cầu kinh doanh và kỳ vọng đối với sản phẩm.

Thu thập yêu cầu là một quá trình cộng tác. Business Analyst có thể giúp phân tích và ghi lại các yêu cầu, SME (Subject matter expert - chuyên gia lĩnh vực) cung cấp kiến thức chuyên môn và làm rõ các quy tắc nghiệp vụ, và development team tham gia backlog refinement để đảm bảo yêu cầu khả thi (feasible) về mặt kỹ thuật và được hiểu rõ ràng.

Scrum Master chủ yếu giúp quản lý quy trình và hỗ trợ team.

Agile là một phương phát phát triển phần nềm linh hoạt, để thực hiện phương phát này thì người ta hay dùng scrum 
Mục tiêu agile: 
- Thích ứng nhanh với thay đổi yêu cầu.
- Giao sản phẩm sớm và liên tục.
- Quá trình phát triển Agile diễn ra theo các sprint, kéo dài 1-4 tuần.

```
Product Backlog (List tất cả feature sản phẩm)  -> Product owner, stakeholders, BA
↓
Backlog Refinement(Làm rõ các feature bao gồm phân tích user story(mô tả chức năng dưới góc độ người dùng), chia nhỏ task, ước lượng độ phức tạm)  -> Product owner, development team, BA 
↓
Sprint Planning (Team chọn task từ backlog -> xác định sprint goal, chia task cho dev) -> PO, Developmentteam , Scrum master
↓
Development (Giai đoạn build feature gồm: coding, testing) ở giai đoạn này sẽ có daily scrum meeting mỗi này 15p  nói các nội dung (hôm trước làm gì?, hôm nay làm gì? gặp vấn đề gì?) -> Development team, scrum master
↓
Sprint Review (Demo sản phẩm, nhận feedback từ stakeholder)  -> PO, development team, stakeholder, scrum master
↓
Sprint Retrospective(họp team nội bộ để cải thiện quy trình làm việc) -> điều gì làm tốt, điều gì chưa tốt cần cải thiệt. -> Development team , scrum master, PO
```

## Bạn đã từng làm việc với Agile chưa? Làm việc theo sprint không?

Có, tôi đã làm việc trong Agile bằng Scrum. Chúng tôi làm việc theo các sprint. Với vai trò developer, tôi chọn các task từ product backlog và hiện thực các tính năng dựa trên các ticket được giao. Trong sprint, chúng tôi có các buổi họp stand-up hằng ngày để thảo luận tiến độ và các vướng mắc (blocker). Cuối sprint, chúng tôi demo các tính năng đã hoàn thành trong sprint review và sau đó tổ chức retrospective để thảo luận (team làm tốt điều gì? team làm chưa tốt điều gì) nhằm cải thiện cho sprint tiếp theo.

## Phát triển phần mềm trong nghiên cứu lâm sàng khác gì so với các lĩnh vực khác (như phần mềm văn phòng, game, logistics)?

Nhìn chung, phát triển phần mềm trong nghiên cứu lâm sàng khá khác biệt vì mọi tính năng đều phải tuân theo các quy định nghiêm ngặt và các quy trình vận hành chuẩn nội bộ (SOP - standard operating procedures).

Ví dụ, khi kiểm thử một tính năng, chỉ nói rằng test đã pass là chưa đủ. Chúng ta cần ghi lại đã test cái gì, test như thế nào, và ai thực hiện test, cùng với bằng chứng, và những thứ này có thể được xem xét trong các đợt đánh giá (audit).

Một điểm khác biệt quan trọng nữa là quy trình validation trước khi triển khai. Ở nhiều lĩnh vực, bạn có thể deploy phần mềm nhanh chóng, nhưng với hệ thống lâm sàng thì phần mềm phải vượt qua một quy trình validation chính thức trước khi cài đặt.

Vì vậy nhìn chung, trọng tâm không chỉ là tốc độ phát triển, mà còn là khả năng truy vết (traceability), validation và tuân thủ quy định (regulatory compliance).

## Thiết kế mô hình cây có độ sâu thay đổi như thế nào?

> Ví dụ: Sơ đồ tổ chức (Org-Chart) của một công ty

Để thiết kế mô hình cây có độ sâu thay đổi cho sơ đồ tổ chức, dùng Composite Pattern. Mỗi nhân viên được biểu diễn là một node trong hệ thống phân cấp (hierarchy). Một nhân viên thường là leaf node (node lá) không có cấp dưới (subordinate), còn một quản lý là composite node có danh sách cấp dưới. Vì cả employeeLeaf và manageComposite dùng chung một abstraction cơ sở, hệ thống có thể xử lý chúng đồng nhất và dễ dàng hỗ trợ phân cấp với độ sâu bất kỳ.

Pattern này thường được dùng trong các cấu trúc phân cấp như:

- sơ đồ tổ chức
- hệ thống file (thư mục và file)
- cây UI component

Nó giúp thiết kế linh hoạt và dễ mở rộng.
Composite Pattern được dùng để biểu diễn các cấu trúc cây phân cấp, trong đó cả đối tượng đơn lẻ và đối tượng tổng hợp (composite) dùng chung một interface và có thể được xử lý đồng nhất.

## Command pattern là gì? Ứng dụng hữu ích của pattern này?

Command pattern là một behavioral design pattern đóng gói một yêu cầu (request) thành một object.
Điều này cho phép tách rời (decouple) đối tượng gọi thao tác khỏi đối tượng thực sự thực hiện nó.
Mỗi command object thường chứa một method execute(), định nghĩa hành động cần thực hiện..

Ví dụ, trong một trình soạn thảo văn bản, các hành động như copy, paste và delete có thể được hiện thực dưới dạng command object. Mỗi command có một method execute() thực hiện hành động đó.
Bằng cách biểu diễn hành động dưới dạng object, hệ thống có thể dễ dàng hỗ trợ các tính năng như undo, logging, hoặc xếp hàng đợi (queuing) các thao tác.

## Dependency Injection

> Câu hỏi gốc: Chúng tôi cũng dùng DI từ JEE và bằng một hiện thực tự xây dựng (homegrown) dựa trên JMX. DI hoạt động thế nào và bạn có thể hình dung các lý do chính khiến chúng tôi dùng nó không?

Dependency Injection là một design pattern dùng để giảm sự ràng buộc chặt (tight coupling) giữa các thành phần bằng cách inject các dependency từ bên ngoài thay vì tạo chúng bên trong class.
Thông thường, một container (như Spring) chịu trách nhiệm tạo và quản lý các object, rồi inject chúng vào các class phụ thuộc thông qua constructor, setter hoặc field injection.

Các lý do chính để dùng DI là:

- Loose coupling (liên kết lỏng) – các thành phần phụ thuộc vào abstraction thay vì các hiện thực cụ thể
- Khả năng kiểm thử tốt hơn – các dependency có thể dễ dàng được mock hoặc thay thế
- Linh hoạt và dễ bảo trì – có thể thay đổi hiện thực mà không cần sửa code phía client

Tôi hiểu rằng các bạn đang dùng Dependency Injection theo hai cách: DI chuẩn dựa trên JEE và một hiện thực tự xây dựng dùng JMX.
Trong JEE, container quản lý dependency injection bằng các annotation như @Inject.
Giải pháp tự xây dựng dựa trên JMX có lẽ cung cấp nhiều linh hoạt hơn, cho phép các dependency được quản lý và thậm chí được cấu hình lại động ngay lúc runtime.

## Vấn đề khó nhất bạn từng gặp?

Vấn đề khó nhất tôi từng gặp là khi tôi phải xử lý đồng thời đồ án tốt nghiệp đại học và một dự án ở chỗ làm.
Tôi vất vả trong việc cân bằng thời gian giữa hai việc, và khá căng thẳng, đặc biệt vì dự án ở chỗ làm có khối lượng công việc nặng và phải làm thêm giờ.
Sau đó, tôi trao đổi với project manager và team lead để giải thích hoàn cảnh của mình. Tôi cam kết sẽ hoàn thành đồ án đại học trước rồi sau đó bù lại toàn bộ ở chỗ làm.

## Optional và NullPointerException

> Câu hỏi gốc: Optional được cho là giúp tránh NullPointerException - Bằng cách nào? Sự khác nhau giữa kiểm tra null `if(foo != null) {...}` và kiểm tra tương ứng trên Optional `if(foo.isPresent()) {...}` là gì?

Optional giúp tránh NullPointerException (bằng cách làm cho việc không có giá trị trở nên tường minh và buộc lập trình viên phải xử lý trường hợp đó.)
Thay vì trả về null, một method trả về Optional, điều này chỉ rõ rằng giá trị có thể không có. Điều này khuyến khích người gọi xử lý cả hai trường hợp (có giá trị hoặc rỗng) bằng các method như ifPresent, orElse, hoặc orElseThrow.

Tuy nhiên, dùng isPresent() kèm get() không được khuyến khích, vì nó giống với kiểm tra null và vẫn có thể dẫn đến runtime exception nếu dùng sai. Thay vào đó, tốt hơn là dùng các method như ifPresent, orElse, hoặc orElseThrow để xử lý an toàn và diễn đạt rõ ràng hơn.
Kiểm tra null thì ngầm định (implicit) và dễ bị quên, còn Optional làm cho việc không có giá trị trở nên tường minh và khuyến khích cách xử lý an toàn hơn.

## Nguồn tham khảo

- Ghi chú phỏng vấn cá nhân (bản gốc tiếng Anh, dán vào để dịch).
