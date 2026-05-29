Case ví dụ: **Đồng bộ dữ liệu đa nền tảng trên Web**

Nhân vật ví dụ: Khoa, Web Admin. Mỗi tuần Khoa phải copy-paste thủ công các thông số (máu, sát thương, giá tiền...) của 48 mục từ bảng tính Excel của team Content vào hệ thống CMS/Database của trang Web Bách khoa toàn thư.

## 1. Bảng Scan


| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Phải copy-paste thủ công thông số cấu hình từ Excel vào CMS. | Khoa (Web Admin) | Mất 2 giờ/tuần, lặp đi lặp lại thao tác bàn phím, cực dễ nhầm lẫn. |
| 2 | Tốn thời gian | Đổi tên thủ công từng file ảnh (sprite/icon) cho khớp ID trên database. | Khoa (Web Admin) | Mất 45 phút/lần up file, gõ sai tên làm hỏng ảnh web. |
| 3 | Pain từ người khác | Excel của team Content bị thừa dấu cách, sai format dữ liệu (chữ/số). | Khoa (Web Admin) | Phải ping team Content trên Slack 2-3 lần/tuần, ngồi xóa khoảng trắng bằng tay. |
| 4 | Lặp lại | Gõ mã HTML thủ công (bọc in đậm thẻ `<b>`) vào các đoạn text mô tả. | Khoa (Web Admin) | Hay quên đóng thẻ khiến giao diện vỡ, tốn 30 phút rà lỗi code. |
| 5 | AI có thể tốt hơn | Tự nghĩ từ khóa (Tags) và gắn vào từng mục cho thanh Search hoạt động. | Khoa (Web Admin) | Gắn tag thiếu ngữ cảnh, user tìm không ra kết quả (Tốn 15 phút rà soát). |

---

## 2. Top 3 Candidates

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Copy-paste Excel vào CMS | Workflow cực kỳ rõ ràng, bottleneck lặp lại, metric thời gian đo đếm được chính xác (2 giờ). | Webhook/API của hệ thống CMS hiện tại có mở để kết nối tự động không? |
| 2 | Sửa định dạng/dấu cách Excel | Pain từ người khác, gây nghẽn trực tiếp cho luồng nhập liệu web. | Có thể đưa các rule validate (chặn nhập sai) thẳng vào Google Sheets được không? |
| 3 | Gắn Tags cho thanh Search | Có đất diễn cho AI (hiểu ngữ cảnh text để sinh tag tự động). | Mức độ phức tạp cao, vẫn tốn thời gian kiểm duyệt đầu ra của AI. |

---

## 3. Top 3 Problem Cards & Draft Workflow

### Problem Card #1: Đồng bộ dữ liệu Excel vào CMS

*   **Problem 1 câu:** Mỗi khi có batch dữ liệu mới, Web Admin mất 2 giờ để copy-paste thủ công thông số từ Excel vào Database; thao tác này cực kỳ dễ gõ sai định dạng gây sập giao diện hiển thị.
*   **Actor:** Khoa (Web Admin).
*   **Thời điểm / bối cảnh:** Thứ Sáu hằng tuần, sau khi team Content chốt file thông số (Patch update).
*   **Bottleneck:** Bước copy-paste 48 mục (khoảng hơn 200 trường dữ liệu) mất 120 phút.
*   **Impact:** Mất 2 tiếng/tuần làm việc tay chân, gây rủi ro sập giao diện web do Human Error (nhầm 1 dấu phẩy là file JSON lỗi parse).
*   **Success metric:** Tổng thời gian đồng bộ giảm từ 120 phút xuống dưới 5 phút. Tỷ lệ lỗi định dạng JSON = 0.
*   **Non-AI alternative:** Viết macro trong Excel.
*   **AI hypothesis:** Chưa cần đến AI Agent phức tạp. Chỉ cần Workflow tự động nối Data.
*   **Quick gut:** Workflow.

**Draft current workflow:**
```text
CURRENT STATE — 120 phút

[1 Nhận file Excel: 2']
→ [2 Mở Excel & CMS: 3']
→ [3 Copy từng ô thông số: 50'] <-- Bottleneck lặp lại
→ [4 Paste vào trường DB: 50'] <-- Bottleneck (Nguy cơ human error)
→ [5 Publish & Check lỗi hiển thị: 15']
```

**Draft future workflow:**
```text
FUTURE STATE — 5 phút

[1 Content team update Google Sheets: 0'] 
→ [2 Automation (Make/n8n) bắt Webhook khi có data mới: 1'] 
→ [3 Script tự động parse Data thành định dạng JSON chuẩn: 1'] 
→ [4 API tự đẩy thẳng JSON vào DB: 1'] 
→ [5 Admin review hiển thị trên frontend & Publish: 2'] -- Human boundary
```

### Problem Cards #2 và #3 — tóm tắt

| Card | Actor | Bottleneck | Metric | Quick gut | Vì sao chưa chọn làm #1 |
|---|---|---|---|---|---|
| Làm sạch dữ liệu Excel | Khoa (Web Admin) | Dò tìm khoảng trắng thừa và lỗi gõ sai định dạng (chữ/số) bằng mắt hoặc hàm thủ công | 25 phút → 0 phút | Rule | Có thể giải quyết triệt để bằng Process Fix (khóa tính năng nhập liệu trên Sheets gốc), không đáng để xây luồng riêng |
| Gắn Tags cho thanh Search | Khoa (Web Admin) | Tự đọc mô tả văn bản, vắt óc suy luận từ khóa và gõ thủ công từng tag | 15 phút → 3 phút | Agent / Workflow | Độ phức tạp khi tích hợp AI cao, vẫn cần con người kiểm duyệt, impact thời gian không lớn bằng bài số #1 |

---