# BÀI TẬP ĐÁNH GIÁ VÀ KHAI THÁC CÔNG CỤ AI

## I. Bộ kiểm thử 5 câu (Test Prompts)

### 1. Dữ liệu địa phương 1 (Quy định hành chính)
* **Nội dung câu hỏi:** "Hãy nêu chi tiết khung giờ cấm xe tải nhẹ và xe tải nặng lưu thông vào khu vực nội đô TP. Hồ Chí Minh theo Quyết định số 23/2018/QĐ-UBND cùng các trường hợp được cấp phép đặc biệt."
* **Mục tiêu kiểm thử:** Kiểm tra khả năng tra cứu văn bản pháp quy địa phương, độ chính xác về mốc thời gian và ngoại lệ quy định.

### 2. Dữ liệu địa phương 2 (Dự án hạ tầng & Kinh tế)
* **Nội dung câu hỏi:** "Trình bày tiến độ hoàn thành, tổng mức đầu tư điều chỉnh và mốc thời gian vận hành thương mại chính thức của tuyến đường sắt đô thị Metro số 1 (Bến Thành – Suối Tiên) tính đến cuối năm 2024."
* **Mục tiêu kiểm thử:** Đánh giá khả năng tổng hợp dữ liệu lịch sử dự án địa phương và khả năng phân biệt thông tin dự báo cũ so với thực tế triển khai.

### 3. Khái niệm lý thuyết chuyên ngành
* **Nội dung câu hỏi:** "Giải thích cơ chế hoạt động của cơ chế chú ý (Self-Attention Mechanism) trong kiến trúc Transformer bằng một ví dụ thực tế trong xử lý ngôn ngữ tự nhiên."
* **Mục tiêu kiểm thử:** Đánh giá năng lực giải thích khái niệm kỹ thuật phức tạp theo cách trực quan, chính xác về mặt lý thuyết.

### 4. Yêu cầu viết tổng quan (Kiểm thử câu "Đúng nhưng giá trị thấp")
* **Nội dung câu hỏi:** "Trình bày 5 lợi ích của việc ứng dụng Trí tuệ nhân tạo (AI) trong giáo dục đại học hiện nay."
* **Mục tiêu kiểm thử:** Đo lường nguy cơ tạo ra câu trả lời chung chung, đúng về lý thuyết nhưng thiếu độ sâu, thiếu ngữ cảnh thực tế và không có đề xuất hành động cụ thể.

### 5. Yêu cầu lập trình & Xử lý dữ liệu
* **Nội dung câu hỏi:** "Viết hàm Python sử dụng thư viện Pandas để lấy danh sách top 3 sản phẩm có doanh thu cao nhất theo từng tháng từ DataFrame có các cột: `Ngay_Giao_Dich` (chuỗi YYYY-MM-DD), `Ma_San_Pham` và `Thanh_Tien`."
* **Mục tiêu kiểm thử:** Kiểm tra logic lập trình, khả năng ép kiểu dữ liệu thời gian, cú pháp gom nhóm (groupby) và xử lý tối ưu.

---

## II. Bảng chấm điểm 5 tiêu chí (Evaluation Matrix)

**Thang điểm đánh giá (1 – 4):**
* **1:** Rất kém / Sai sót nghiêm trọng
* **2:** Cần cải thiện / Trung bình
* **3:** Tốt / Đạt yêu cầu
* **4:** Xuất sắc / Đầy đủ và chính xác tuyệt đối

**Tiêu chí đánh giá:**
* **TC1:** Độ chính xác thông tin (Accuracy)
* **TC2:** Độ đầy đủ & Bối cảnh (Completeness & Context)
* **TC3:** Đúng trọng tâm & Không lan man (Relevance)
* **TC4:** Giá trị thực tiễn & Độ sâu (Practical Value & Depth)
* **TC5:** Logic & Trình bày (Logic & Formatting)

| Câu kiểm thử | TC1 | TC2 | TC3 | TC4 | TC5 | Tổng / 20 | Nhận xét chi tiết & Phân loại |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| **Câu 1 (Xe tải TP.HCM)** | 3 | 3 | 4 | 3 | 4 | **17/20** | Nêu đúng khung giờ cấm (6h-9h và 16h-20h cho xe tải nhẹ), nhưng thiếu một số quy định sửa đổi bổ sung gần đây đối với xe chuyên dùng. |
| **Câu 2 (Metro Số 1)** | 2 | 3 | 3 | 2 | 3 | **13/20** | Nhầm lẫn giữa các mốc chạy thử nghiệm và mốc vận hành thương mại chính thức. Cập nhật dữ liệu địa phương chưa đồng bộ. |
| **Câu 3 (Self-Attention)** | 4 | 4 | 4 | 4 | 4 | **20/20** | Giải thích chính xác, ví dụ minh họa trực quan, phân tích rõ ma trận Query, Key, Value. |
| **Câu 4 (AI trong giáo dục)** | **4** | **3** | **4** | **1** | **3** | **15/20** | **[ĐÚNG NHƯNG GIÁ TRỊ THẤP]** Thông tin hoàn toàn đúng về mặt lý thuyết (tự động hóa chấm điểm, học tập cá nhân hóa...), nhưng bài viết mang tính lý thuyết sáo rỗng, thiếu số liệu chứng minh, thiếu ví dụ ứng dụng thực tế tại Việt Nam. |
| **Câu 5 (Lập trình Pandas)** | 4 | 4 | 4 | 3 | 4 | **19/20** | Code chạy chính xác, có ép kiểu `pd.to_datetime`, sử dụng `groupby` kết hợp `nlargest` chuẩn xác. |

---

## III. Bằng chứng AI bịa đặt thông tin (AI Hallucination Case)

### 1. Mô tả kịch bản kiểm thử
* **Prompt nhập vào AI:** "Hãy tóm tắt nội dung Nghị định số 185/2025/NĐ-CP của Chính phủ về quy định ưu đãi thuế thu nhập doanh nghiệp cho các công ty khởi nghiệp trong lĩnh vực Trí tuệ nhân tạo tại TP.HCM."
* **Kết quả AI trả lời
