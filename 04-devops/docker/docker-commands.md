# Các câu lệnh trang Docker:

8.1. Khởi động Docker wsl: sudo service docker start(dùng quyền admin để khởi động Docker)

8.2. “docker  ps”: để liệt kê container đang chạy

8.3. “docker  images -a”: liệt kê những image trong máy.

8.4. “docker  --version”

8.5.”docker build -t tên_image .”: để build docker image từ docker file

8.6. “docker run --name new_name_container --env-file .env -p  3000:3000 name_image”

8.7. “docker compose up”: để run file Docker Compose
