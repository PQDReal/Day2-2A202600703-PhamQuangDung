## Đóng góp của Mình trong nhóm

|Hoạt động|Minh đã làm gì?|Kết quả|
|-|-|-|
|Scan cá nhân|Đưa ra 5 problems về vận hành website và dữ liệu.|Nhóm có các candidate về luồng nhập liệu (Data Entry) và CMS|
|Pitch|Pitch bài toán đồng bộ 48 loại cây từ Excel vào CMS.|Bài không được đưa vào shortlist do chưa đủ thuyết phục|
|Challenge|Đặt câu hỏi: "Nếu giao cho AI Agent tự đọc dữ liệu cấu hình mà nó tự bịa số liệu (hallucination) thì ai chịu trách nhiệm sửa web sập?"|Nhóm loại bỏ ngay các ý tưởng lạm dụng AI không cần thiết|
|Workflow|Vẽ current/future workflow cho quy trình update bách khoa toàn thư.|Nhóm dùng làm workflow bản cuối|

## Bảng dùng AI trong reflection

|Phase|Tôi dùng AI để làm gì?|AI hữu ích ở đâu?|AI sai/hời hợt ở đâu?|Tôi sửa gì|
|-|-|-|-|-|
|Scan|Nhờ AI gợi ý thêm các góc nhìn về công việc lặp lại.|Giúp phân loại rõ các lăng kính (Tốn thời gian, Pain từ người khác).|AI dùng Agent để "tự động đọc hiểu file Excel".|Gạt bỏ ý tưởng dùng Agent ngay lập tức|
|Workflow|Nhờ AI tạo mã sơ đồ Mermaid để biểu diễn current và future workflow|Nhận diện và bắt các bước để chuyển thành các khối trong biểu đồ.|Code Mermaid sinh ra thỉnh thoảng render hiển thị quá rối mắt, khó kiểm soát trên GitHub.|Quyết định bỏ Mermaid, chuyển sang vẽ bằng định dạng ASCII thuần túy|
|Research|Tìm tool/ứng dụng hỗ trợ đẩy dữ liệu tự động.|Gợi ý đúng các công cụ mạnh như Make.com.|Đề xuất thêm các AI Agent tự làm sạch dữ liệu.|Loại bỏ vì over-engineering. Rủi ro sai định dạng (chữ/số) có thể giải quyết dứt điểm bằng Data Validation ngay trên Sheet gốc.|
|Problem Statement|Nhờ AI phản biện các field xem có mơ hồ không.|Giúp câu từ trong Problem Statement trở nên súc tích hơn.|AI vẫn cố điều hướng sang việc thêm "AI intervention point" vào một khâu nào đó.|Cương quyết ghi rõ "KHÔNG DÙNG AI"|

## Bài học của Mình

* Problem tốt không nhất thiết phải là problem nghe có vẻ "AI" nhất, mà là problem có điểm nghẽn thực sự và metric thời gian đo đếm được rành mạch. Vẽ workflow giúp thấy phần nào rule đủ, phần nào AI mới có ích.
* Vẽ workflow giúp bóc tách được gốc rễ của việc chậm trễ: rào cản lớn nhất nằm ở thao tác copy/paste cơ học, chứ không phải ở việc dữ liệu quá khó hiểu.
* Agent không phải là đích đến mặc định. Đối với các dự án xây dựng cơ sở dữ liệu tĩnh (như 48-plant database), Workflow API kết hợp Rule chặn lỗi từ đầu vào là sự lựa chọn hợp lý và an toàn nhất.

Nếu làm lại:

```text
Mình sẽ đầu tư thời gian ở bước Individual Scan để chuẩn bị nhiều problem cards chất lượng hơn. Lần này mình có hơi ít lựa chọn để mang ra đề xuất với nhóm, làm hạn chế sự đa dạng khi nhóm cần so sánh các bài toán với nhau.```

\---



