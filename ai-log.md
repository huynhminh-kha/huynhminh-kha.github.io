# Nhật ký Sử dụng Công cụ AI (AI Log)

- **Họ và tên:** Huỳnh Minh Kha
- **MSSV:** [2680120002]
- **Vai trò trong dự án:** [Lập trình Backend & Thiết kế CSDL]
- **Đồ án:** [khoa học máy tính]

---

## Log #01: Thiết kế sơ đồ CSDL và API xác thực người dùng
- **Thời gian:** [25/10/2026]
- **Công cụ AI sử dụng:** ChatGPT (GPT-4o) / Claude 3.5 Sonnet
- **Mục tiêu:** Tạo cấu trúc bảng `Users`, `Roles` và API login/register chuẩn RESTful.

### 1. Prompt đã dùng (Input)
> "Tôi đang làm đồ án web quản lý kho. Hãy gợi ý sơ đồ CSDL PostgreSQL cho phần Quản lý người dùng và Phân quyền (RBAC). Sau đó viết code Express.js cho API đăng nhập dùng JWT."

### 2. Kết quả AI trả về (AI Output Summary)
- Đề xuất 3 bảng: `users`, `roles`, `user_roles`.
- Đoạn mã mẫu Express.js xử lý `/login` trả về JWT Token lưu ở phía client.

### 3. Đánh giá & Kiểm chứng (Verification)
- **Điểm hợp lý:** Cấu trúc bảng RBAC cơ bản đúng chuẩn chuẩn hóa 3NF.
- **Hạn chế / Bất cập:** 
  - AI gợi ý lưu JWT ở `LocalStorage` phía Frontend (nguy cơ bị tấn công XSS).
  - Chưa có cơ chế Refresh Token và chưa hash mật khẩu bằng `bcrypt` trước khi so sánh.

### 4. Tùy chỉnh & Tích hợp thực tế (Human Intervention)
- Chỉnh sửa lại API: Chuyển sang trả Refresh Token qua `HttpOnly Cookie`.
- Bổ sung thư viện `bcrypt` để mã hóa mật khẩu.
- Cập nhật lại sơ đồ CSDL để thêm trường `deleted_at` (Soft delete) và `last_login`.
- Commit mã nguồn đã sửa lên nhánh `feature/auth` của Git nhóm.

---

## Log #02: Tối ưu truy vấn SQL cho chức năng tìm kiếm
- **Thời gian:** [25/10/2026]
- **Công cụ AI sử dụng:** GitHub Copilot / Gemini
- **Mục tiêu:** Tối ưu hóa câu truy vấn tìm kiếm sản phẩm theo nhiều tiêu chí.

