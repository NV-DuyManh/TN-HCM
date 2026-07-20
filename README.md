# 📚 Trắc Nghiệm Software Architecture MCQ - Ultimate Edition

Đây là một ứng dụng Web Single-Page Application (SPA) hỗ trợ ôn thi trắc nghiệm môn **Software Architecture** (Kiến trúc Phần mềm). 
Ứng dụng được thiết kế tối giản, nhanh chóng và có thể chạy trực tiếp trên trình duyệt mà không cần cài đặt thêm bất kỳ thư viện hay backend nào (hoạt động offline).

## ✨ Các Tính Năng Nổi Bật

- 📝 **Ngân hàng câu hỏi phong phú:** 168 câu hỏi trắc nghiệm kiến thức Kiến trúc Phần mềm bao phủ nhiều chủ đề (SCD, Module Structure, Patterns, Quality Attributes, ...).
- 🎓 **Giải thích chi tiết:** Mỗi câu hỏi đều kèm theo giải thích ngắn gọn bằng Tiếng Việt giúp người học dễ dàng nắm bắt kiến thức sau khi chọn sai/đúng.
- 🎯 **Chế độ học tập đa dạng:**
  - **Luyện tập tự do:** Trả lời từng câu và xem kết quả giải thích ngay lập tức.
  - **Thi thử (Exam Mode):** Bấm giờ 60 phút, xáo trộn câu hỏi, chỉ biết kết quả sau khi nộp bài.
  - **Ôn tập chuyên sâu (Review Mode):** Đánh dấu các câu "Không biết" hoặc hay sai để tạo thành một bộ đề thu nhỏ chỉ tập trung vào các điểm yếu của bản thân.
- 🎨 **Giao diện hiện đại & tiện dụng:**
  - Hỗ trợ **Chế độ Sáng/Tối (Dark Mode)** bảo vệ mắt.
  - Bảng điều hướng nhanh bên cạnh (Sidebar) với lưới các nút câu hỏi, thể hiện trực quan câu đúng (xanh), sai (đỏ), chưa làm (trắng).
  - Có thanh tìm kiếm (Search) theo thời gian thực giúp tra cứu nhanh nội dung câu hỏi.
  - Giao diện thân thiện và hoạt động tốt trên cả máy tính lẫn thiết bị di động (Responsive Design).
- 🔊 **Trải nghiệm âm thanh (Web Audio API):** Âm thanh sinh động khi trả lời đúng, sai và click chuột (có thể bật/tắt).
- 📊 **Quản lý lịch sử học tập:**
  - Lưu lại tự động (qua `localStorage`) các lần làm bài tập / thi thử kèm theo điểm số, ngày giờ và thời gian hoàn thành.
  - Hỗ trợ Sao lưu (Export) & Khôi phục (Import) dữ liệu lịch sử dưới dạng file JSON.

## 🚀 Cách Sử Dụng

1. Tải toàn bộ mã nguồn về máy.
2. Ứng dụng chỉ sử dụng HTML, CSS và Javascript thuần túy (không cần Node.js, PHP hay cơ sở dữ liệu).
3. Mở trực tiếp file `index.html` bằng bất kỳ trình duyệt web hiện đại nào (Chrome, Edge, Firefox, Safari...).
4. Trải nghiệm!

## 📂 Cấu Trúc Dự Án

Toàn bộ logic, giao diện, và dữ liệu của ứng dụng được gói gọn trong file `index.html`.
- **CSS:** Được viết trực tiếp trong thẻ `<style>`, quản lý màu sắc bằng CSS Variables giúp hỗ trợ tính năng Dark Mode cực nhẹ.
- **Dữ liệu (`quizData` & `explanationData`):** Cứng hóa ngay trong file dưới dạng các biến mảng JSON, chứa danh sách 168 câu hỏi Tiếng Anh và phần giải thích Tiếng Việt.
- **JavaScript:** Chứa logic cốt lõi về xử lý sự kiện, đồng hồ đếm ngược, phân trang, thuật toán tìm kiếm và lưu trữ lịch sử qua trình duyệt web (`localStorage`).

## ⚙️ Thiết Lập Kỹ Thuật (Dành cho Developer)

- **Môi trường:** Client-side 100%.
- **Key LocalStorage sử dụng:**
  - `sa_mcq_history`: Lưu mảng lịch sử làm bài.
  - `sa_mcq_review`: Lưu danh sách ID các câu cần ôn tập.
  - `sa_mcq_dark`: Lưu trạng thái Dark Mode (`true`/`false`).
  - `sa_mcq_sound`: Lưu trạng thái Âm thanh (`true`/`false`).
- **Thay đổi ngưỡng qua bài:** Chế độ thi thử mặc định yêu cầu ít nhất 84/168 câu (50%) để qua môn. Có thể thay đổi bằng cách sửa biến `score >= 84` trong hàm `submitExam()`.


