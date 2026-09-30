# Quy tắc làm việc trong repo knowledge-base

Đây là các quy tắc của chủ repo. Luôn tuân thủ; khi chủ repo nhắc thêm quy tắc mới thì ghi tiếp vào file này.

## Quy tắc về nội dung ghi chú

1. **Giữ nguyên nội dung**: khi tổ chức lại ghi chú, không đổi câu chữ (kể cả lỗi chính tả, cách diễn đạt của chủ repo). Chỉ được thêm định dạng Markdown (heading, code block, danh sách) và di chuyển vị trí.
2. **Không tự ý sửa**: chỉ được sửa nội dung khi chủ repo cho phép rõ ràng cho từng lần sửa.
3. **Kiến thức sai thì nhắc**: nếu thấy kiến thức không đúng hoặc có lỗi, hãy nhắc chủ repo trong câu trả lời (không sửa trong file), rồi chờ chủ repo quyết định.

## Quy ước tổ chức

- Chia theo chủ đề, thư mục cấp 1 đánh số (`00-inbox`, `01-java`, `02-messaging`, `03-devops`, `04-database`, `05-architecture`, `06-cheatsheets`, `07-troubleshooting`).
- Tên file và thư mục: tiếng Anh, chữ thường, kebab-case, không dấu, không khoảng trắng. Nội dung viết bằng tiếng Việt.
- Mỗi chủ đề có `README.md` làm mục lục; thêm note mới thì cập nhật mục lục.
- Note mới dùng `templates/note-template.md` khi là note viết mới; note chuyển từ ghi chú cũ thì giữ nguyên nội dung theo quy tắc 1.
- Chưa biết đặt đâu thì bỏ vào `00-inbox/`.
- Không commit thông tin nhạy cảm (token, URL nội bộ, config công ty).
