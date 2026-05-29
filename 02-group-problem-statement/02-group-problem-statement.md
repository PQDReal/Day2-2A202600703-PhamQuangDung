# 02 — Group Problem Statement Draft

## Danh sách vấn đề

| STT | Vấn đề |
|------|---------|
| 1 | Tổng hợp tài liệu ôn thi |
| 2 | Tìm lại thông tin Discord/Zalo |
| 3 | Theo dõi deadline môn học |
| 4 | Tìm quán ăn phù hợp ngân sách |
| 5 | Tìm tuyến đường tối ưu đến trường |
| 6 | Tìm phòng trọ gần trường |
| 7 | Kiến thức AI quá nhiều và tốc độ học quá nhanh |
| 8 | Khó cân bằng giữa việc học ở trường đại học và AI20K |
| 9 | Lớp học đông, trợ giảng không đủ hỗ trợ |
| 10 | Copy-paste Excel vào CMS |
| 11 | Sửa định dạng/dấu cách Excel |
| 12 | Gắn Tags cho thanh Search |
| 13 | Cognitive reframing khi nhận feedback tiêu cực |
| 14 | Reframing tin nhắn mơ hồ để giảm overthinking |
| 15 | Cognitive reframing cho deadline panic thành bước hành động nhỏ |
## Cluster
| Cluster | Candidate examples | Pattern chung |
|----------|----------|----------|
| Tìm kiếm / hỏi đáp tài liệu | Tổng hợp tài liệu ôn thi, Tìm lại thông tin Discord/Zalo, Theo dõi deadline môn học | Thông tin nằm rải rác ở nhiều nguồn, khó tìm lại đúng lúc |
| Đời sống sinh viên | Tìm quán ăn phù hợp ngân sách, Tìm tuyến đường tối ưu đến trường, Tìm phòng trọ gần trường | Sinh viên mất thời gian tìm kiếm và ra quyết định |
| Học tập & hỗ trợ | Kiến thức AI quá nhiều và tốc độ học quá nhanh, Khó cân bằng giữa đại học và AI20K, Lớp học đông trợ giảng không đủ hỗ trợ | Thiếu cá nhân hóa và thiếu hỗ trợ kịp thời |
| Data entry / Automation | Copy-paste Excel vào CMS, Sửa định dạng/dấu cách Excel, Gắn Tags cho thanh Search | Công việc lặp lại, thủ công, dễ sai sót |
| Mental wellness | Cognitive reframing khi nhận feedback tiêu cực, Reframing tin nhắn mơ hồ để giảm overthinking, Reframing deadline panic thành bước hành động nhỏ | Chuyển suy nghĩ tiêu cực thành hành động tích cực |
## Shortlist và Score

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|------------|-----------|------------|-----------------|---------------|---------------|-------------------|------------------|------|
| Cognitive Reframing khi nhận feedback tiêu cực | 5 | 5 | 4 | 5 | 5 | 5 | 5 | 34 |
| Reframing tin nhắn mơ hồ giảm overthinking | 4 | 4 | 3 | 3 | 4 | 4 | 5 | 27 |
| Reframing deadline panic thành action nhỏ | 4 | 5 | 4 | 4 | 5 | 4 | 4 | 30 |

### Nhóm chọn: Cognitive Reframing khi nhận feedback tiêu cực

### Vì sao chọn

- Có actor rất rõ: sinh viên nhận feedback từ giảng viên, TA hoặc peer review.
- Workflow hiện tại và workflow tương lai đều xác định được từng bước cụ thể.
- Pain xuất hiện khá phổ biến trong môi trường học tập.
- Có thể đo lường được bằng các metric rõ ràng:
  - Thời gian từ lúc nhận feedback đến khi bắt đầu sửa bài.
  - Số action items tạo được từ feedback.
  - Mức độ khó chịu (self-rated distress) trước và sau khi reframe.
- AI tạo giá trị ở đúng bottleneck: chuyển từ suy nghĩ tiêu cực sang hành động cụ thể.
- Dễ xây dựng và demo trong phạm vi Day 02 Lab.
- Dễ so sánh giữa No AI, Rule, Workflow và Agent.
- Có boundary rõ ràng, không đi sang therapy hoặc mental health.

### Vì sao không chọn các bài khác

#### Reframing tin nhắn mơ hồ giảm overthinking

- Impact khó đo chính xác.
- Dễ xảy ra hallucination khi AI suy đoán ý định người khác.
- Boundary khó kiểm soát hơn.
- Cần nhiều giả định về cảm xúc và ý định của người gửi.

#### Reframing deadline panic thành action nhỏ

- Workflow rõ và có thể đo được.
- Tuy nhiên dễ biến thành bài toán productivity/task management.
- Nhiều giải pháp Rule hoặc Checklist đã giải quyết được phần lớn vấn đề.
- Giá trị riêng của Cognitive Reframing chưa nổi bật bằng bài feedback.

### Decision

| Tiêu chí | Kết quả |
|-----------|----------|
| Actor rõ | ✅ |
| Workflow rõ | ✅ |
| Có bottleneck cụ thể | ✅ |
| Impact đo được | ✅ |
| Có thể validate nhanh | ✅ |
| AI tạo thêm giá trị | ✅ |
| Có boundary an toàn | ✅ |
| Quyết định cuối | **GO** |

## Candidate problem nhóm chốt

```text
Cognitive reframing khi sinh viên nhận feedback tiêu cực.
```

Problem 1 câu:

```text
Sinh viên khi nhận feedback hoặc điểm thấp thường diễn giải feedback thành đánh giá tiêu cực về bản thân, thay vì chuyển feedback thành các điểm sửa cụ thể và kế hoạch cải thiện.
```

Domain:

```text
Domain lớn: Empathy
Hướng cụ thể: Cognitive Reframing
Mức AI dự kiến: Workflow
```

Boundary ngắn:

```text
AI không đóng vai AI therapist, không chẩn đoán, không trị liệu, không xử lý khủng hoảng tâm lý, không chấm lại bài và không đánh giá năng lực cá nhân. AI chỉ hỗ trợ self-reflection, cognitive reframing và chuyển feedback thành action items. Người dùng vẫn tự chọn, sửa và quyết định.
```

---

## 1. Group convergence

Nhóm chọn candidate này vì nó có actor rõ, workflow rõ, bottleneck rõ và dễ vẽ before/after workflow. Problem cũng đủ an toàn vì AI không can thiệp vào đánh giá học thuật hay điều trị tâm lý; AI chỉ hỗ trợ người học tự diễn giải feedback theo cách cân bằng hơn.

### Candidate pool

| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Bottleneck | Ghi chú |
|---|---|---|---|---|---|
| 1 | Phúc | Cognitive reframing khi nhận feedback tiêu cực | Sinh viên | Cá nhân hóa feedback thành "mình kém" | Candidate nhóm chốt |
| 2 |  |  |  |  |  |
| 3 |  |  |  |  |  |
| 4 |  |  |  |  |  |
| 5 |  |  |  |  |  |
| 6 |  |  |  |  |  |
| 7 |  |  |  |  |  |
| 8 |  |  |  |  |  |
| 9 |  |  |  |  |  |

### Vì sao chọn candidate này

```text
1. Actor cụ thể: sinh viên nhận feedback/điểm thấp.
2. Current workflow dễ quan sát: nhận feedback → cảm thấy khó chịu → diễn giải tiêu cực → né đọc kỹ → trì hoãn sửa.
3. Bottleneck không nằm ở thiếu thông tin, mà ở bước diễn giải feedback.
4. Success metric có thể đo bằng action items, thời gian bắt đầu sửa bài, và self-rated distress nhẹ.
5. AI intervention nằm ở một bước rõ: hỗ trợ self-reflection và cognitive reframing, không thay người dùng quyết định.
```

### Vì sao không chọn các candidate khác

| Candidate | Lý do chưa chọn |
|---|---|
| Reframing tin nhắn mơ hồ | Dễ trượt sang việc AI đoán ý định người gửi, boundary khó hơn |
| Cognitive reframing cho deadline panic | Dễ biến thành productivity/task planner, mất trọng tâm Empathy |
| Candidate khác của nhóm | Điền sau khi nghe nhóm pitch |

Nếu có disagreement:

```text
Nhóm sẽ không vote ngay theo cảm tính. Nhóm dùng tiêu chí actor rõ, workflow rõ, bottleneck rõ, metric đo được, boundary an toàn, và mức AI phù hợp để so sánh.
```

---

## 2. Quick validation

Tổng số người dự kiến hỏi nhanh: **5 người tính cả Phúc**.

Mục tiêu không phải chứng minh solution hay, mà kiểm tra pain có thật không:

```text
- Có ai thật sự cá nhân hóa feedback thành "mình kém" không?
- Có ai né đọc kỹ feedback vì thấy khó chịu không?
- Có ai mất lâu mới chuyển feedback thành việc cần sửa không?
- Có ai thấy AI có thể phản tác dụng nếu an ủi sáo rỗng hoặc hiểu sai context không?
```

### Câu hỏi validation

```text
1. Lần gần nhất bạn nhận feedback/điểm thấp, suy nghĩ tiêu cực đầu tiên của bạn là gì?
2. Bạn có từng nghĩ kiểu "mình kém", "mình không hợp môn này", hoặc "mình làm gì cũng sai" không?
3. Sau feedback đó, bạn thường đọc kỹ comment ngay hay né/trì hoãn vì thấy khó chịu?
4. Feedback đó có làm bạn mất động lực, sửa bài muộn, hoặc không biết bắt đầu từ đâu không?
5. Bạn mất khoảng bao lâu để biến feedback thành việc cần sửa cụ thể?
6. Nếu có một workflow hỏi gợi mở, giúp reframe suy nghĩ và tạo 3 action items, bạn có dùng không?
7. Điều gì sẽ làm bạn không tin tool đó: an ủi sáo rỗng, hiểu sai feedback, quá giống AI therapist, hay sợ phụ thuộc?
```
### Bảng validation notes

Ghi chú: bảng dưới đây là **draft/synthetic notes** để nhóm chuẩn bị pitch và đi hỏi nhanh. Khi có câu trả lời thật, nhóm nên thay bằng lời người được hỏi.

| Người được hỏi | Có gặp problem không? | Workflow hiện tại | Bottleneck | Insight |
|---|---|---|---|---|
| Phúc | Có | Nhận feedback → hụt mood → nhìn điểm/comment trước → tự nghĩ "mình kém" → để sau mới sửa | Cá nhân hóa feedback thành đánh giá bản thân | Pain mạnh nhất nằm ở 10-20 phút đầu sau khi nhận feedback; cần reframe trước khi né feedback |
| Cung | Có một phần | Đọc comment → thấy khó chịu → hỏi bạn xem feedback có quá nặng không → sau đó mới quay lại sửa | Cần một người phản chiếu để bớt diễn giải quá tiêu cực | Tool có ích nếu AI hỏi ngắn, không phán xét, không an ủi sáo rỗng |
| Anh | Có | Nhận feedback ngắn/cứng → nghĩ TA/giảng viên không thích bài mình → mất động lực sửa | Trộn lẫn fact trong feedback với assumption về ý định người feedback | AI nên tách fact/thought/feeling, nhưng không được đoán ý định người khác |
| Kiên | Có | Thấy điểm thấp → panic → mở nhiều tài liệu cùng lúc → không biết sửa phần nào trước | Không chuyển feedback thành next step cụ thể | Action items là giá trị chính; reframe chỉ có ích nếu dẫn tới bước sửa nhỏ |
| Dũng | Chưa chắc / có nhẹ | Vẫn đọc feedback nhưng dễ defensive nếu comment quá trực diện → chỉ nhớ câu tiêu cực nhất | Phản ứng tự vệ làm bỏ qua phần feedback đúng | Problem không nặng với tất cả mọi người; target nên là sinh viên dễ self-critical hoặc nhận feedback phê bình mạnh |
### Validation takeaway

```text
Điền sau khi hỏi đủ 5 người.

Nếu đa số nói từng né feedback hoặc từng cá nhân hóa feedback, problem được validate tốt hơn.
Nếu đa số đọc feedback và sửa ngay, nhóm cần thu hẹp actor: sinh viên dễ self-criticize, sinh viên mới học môn khó, hoặc sinh viên nhận feedback phê bình mạnh.
```

---

## 3. Research giải pháp / pattern đã có

Phần này nhóm cần bổ sung link nguồn sau khi research. Trước mắt có thể research theo 3 nhóm pattern:

| Pattern / tool type | Cần tìm gì? | Bài học kéo về problem nhóm |
|---|---|---|
| CBT-style thought record / cognitive reframing worksheet | Cách tách situation, thought, emotion, evidence, alternative thought | Non-AI alternative có thể là form cố định |
| AI journaling / self-reflection tools | Cách AI hỏi câu gợi mở và phản hồi theo ngữ cảnh | AI có thể hữu ích ở bước ngôn ngữ và empathy |
| Learning feedback / formative assessment tools | Cách feedback được chuyển thành next steps | Action items phải gắn với feedback thật, không chỉ an ủi |

# Research giải pháp
## 

| Nguồn / Tool / Case | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / Rủi ro | Bài học cho nhóm |
|---------------------|------|-------------------------|-----------|----------------------|------------------|
| Woebot | https://woebothealth.com | Hỗ trợ người dùng nhận diện suy nghĩ tiêu cực và thực hiện cognitive reframing qua hội thoại | Đặt câu hỏi dẫn dắt thay vì đưa đáp án trực tiếp | Chưa tập trung vào bối cảnh học tập và feedback từ giảng viên | AI nên đóng vai trò coach, không thay người dùng suy nghĩ |
| Wysa | https://www.wysa.com | Hỗ trợ self-reflection và quản lý cảm xúc | Workflow rõ ràng, từng bước nhỏ dễ làm theo | Nhiều phản hồi mang tính template | Reframing cần có cấu trúc và quy trình nhất quán |
| CBT Thought Record | https://www.psychologytools.com/resource/thought-record | Chuyển suy nghĩ tiêu cực thành góc nhìn cân bằng hơn bằng framework CBT | Có cấu trúc Situation → Thought → Evidence → Alternative Thought | Người dùng phải tự điền thủ công, dễ bỏ cuộc | AI có thể hướng dẫn từng bước và giảm ma sát |
| Reflect | https://reflect.app | Hỗ trợ journaling và tự phản ánh | Khuyến khích suy nghĩ có hệ thống | Không tập trung vào feedback học tập | Reflection là bước quan trọng trước khi tạo action plan |
| Notion AI | https://www.notion.so/product/ai | Chuyển nội dung dài thành tóm tắt và action items | Biến thông tin thành các bước hành động cụ thể | Không hỗ trợ reframing cảm xúc hoặc suy nghĩ | Pattern tốt: AI draft → người dùng review |
| Google Gemini | https://gemini.google.com | Tóm tắt, diễn giải và hỗ trợ brainstorming | Có thể chuyển feedback dài thành checklist dễ hiểu | Dễ đưa ra lời khuyên chung chung hoặc thiếu ngữ cảnh | Cần giới hạn vai trò AI và giữ human review |
## Research Takeaway

* Không nên xây dựng AI therapist hoặc hệ thống tư vấn tâm lý.
* Hướng phù hợp hơn là Workflow hỗ trợ Cognitive Reframing trong bối cảnh học tập.
* AI nên hỗ trợ:

  * Hỏi câu gợi mở.
  * Tách Fact / Feeling / Interpretation.
  * Gợi ý 2–3 cách diễn giải cân bằng hơn.
  * Chuyển feedback thành action items cụ thể.
* Người dùng vẫn:

  * Quyết định câu reframe nào phù hợp.
  * Kiểm tra lại action items.
  * Chịu trách nhiệm sửa bài và cải thiện kết quả.

## Pattern chung từ các sản phẩm đã nghiên cứu

```text
User nhập feedback hoặc tình huống

        ↓

AI hỏi câu gợi mở

        ↓

AI hỗ trợ reflection

        ↓

AI tách Fact / Feeling / Interpretation

        ↓

AI gợi ý Cognitive Reframing

        ↓

AI tạo Action Items

        ↓

Người dùng review và quyết định
```

## Kết luận

Nhóm chọn **Workflow** thay vì **Agent** vì:

* Có workflow rõ ràng và dễ kiểm soát.
* AI chỉ can thiệp ở một số bước cụ thể.
* Giảm rủi ro AI đưa lời khuyên tâm lý không phù hợp.
* Phù hợp với phạm vi Day 02 Lab.
* Phù hợp với pattern thực tế của Woebot, Wysa và CBT Thought Record.

### Decision

**Go with Workflow.**
---

## 4. Current workflow

```text
CURRENT STATE — feedback dễ bị cá nhân hóa

[1 Sinh viên nhận feedback/điểm thấp]
        |
        v
[2 Đọc nhanh comment hoặc chỉ nhìn điểm tổng]
        |
        v
[3 Cảm thấy thất vọng / xấu hổ / defensive]
        |
        v
[4 Diễn giải tiêu cực: "mình kém"]  <-- bottleneck chính
        |
        v
[5 Né đọc kỹ feedback hoặc chưa muốn mở lại bài]
        |
        v
[6 Trì hoãn sửa bài / không biết bắt đầu từ đâu]
        |
        v
[7 Sát deadline mới quay lại sửa, dễ lặp lại lỗi cũ]
```

### Current workflow table

| Bước | Actor | Input | Output | Thời gian/tần suất | Ghi chú |
|---|---|---|---|---|---|
| 1 | Sinh viên | Feedback/điểm | Biết kết quả bài làm | Mỗi lần nhận feedback | Trigger chính |
| 2 | Sinh viên | Comment/điểm | Ấn tượng ban đầu | 1-5 phút | Có thể chỉ nhìn điểm |
| 3 | Sinh viên | Ấn tượng ban đầu | Cảm xúc tiêu cực | Vài phút đến vài giờ | Distress nhẹ |
| 4 | Sinh viên | Cảm xúc + suy nghĩ | Diễn giải "mình kém" | Nhanh nhưng ảnh hưởng lớn | Bottleneck |
| 5 | Sinh viên | Feedback chưa xử lý | Né/trì hoãn | Vài giờ đến vài ngày | Mất cơ hội học từ feedback |
| 6 | Sinh viên | Deadline/sửa bài | Bắt đầu muộn | Không ổn định | Action items mơ hồ |

Bottleneck chính:

```text
Bước 4: sinh viên cá nhân hóa feedback, trộn lẫn "bài làm chưa đạt" với "mình kém", nên không chuyển feedback thành hành động sửa bài cụ thể.
```

---

## 5. Future workflow

```text
FUTURE STATE — feedback được chuyển thành self-reflection + action

[1 Sinh viên nhận feedback/điểm thấp]
        |
        v
[2 Sinh viên paste feedback hoặc tự nhập ý chính]
        |
        v
[3 AI hỏi câu gợi mở]
    - Chuyện gì đã xảy ra?
    - Bạn đang cảm thấy gì?
    - Bạn đang tự nói gì với mình?
    - Feedback này nói về bài làm hay nói về con người bạn?
        |
        v
[4 AI tách fact / feeling / interpretation]
        |
        v
[5 AI gợi ý 2-3 câu reframe cân bằng]  <-- AI intervention
        |
        v
[6 Sinh viên chọn/sửa câu reframe đúng với mình]  <-- human boundary
        |
        v
[7 AI chuyển feedback thành 3 action items cụ thể]
        |
        v
[8 Sinh viên chọn action item nhỏ nhất để bắt đầu]

Fallback:
Nếu AI gợi ý quá chung, quá tích cực giả tạo, hoặc không đúng cảm xúc thật,
sinh viên bỏ gợi ý và dùng reflection template thủ công.
```

### Before / after impact

| Metric | Trước | Sau kỳ vọng | Ghi chú |
|---|---:|---:|---|
| Thời gian để bắt đầu đọc kỹ feedback | Có thể trì hoãn vài giờ hoặc vài ngày | Dưới 15 phút sau khi nhận feedback | Cần validate |
| Số action items rõ ràng | 0 hoặc mơ hồ | Ít nhất 3 action items | Gắn với feedback thật |
| Mức distress tự đánh giá | 4/5 hoặc 5/5 | Giảm xuống 2-3/5 | Không dùng như chỉ số lâm sàng |
| Rủi ro AI | Không có AI | AI an ủi sáo rỗng hoặc hiểu sai feedback | Human boundary bắt buộc |

---

## 6. Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Sinh viên nhận feedback hoặc điểm thấp từ giảng viên, TA, peer review, hoặc hệ thống chấm bài. |
| **Workflow** | Nhận feedback/điểm → đọc nhanh hoặc chỉ nhìn điểm → cảm thấy thất vọng/defensive → diễn giải thành "mình kém" → né đọc kỹ feedback → trì hoãn sửa bài → quay lại sát deadline nhưng không biết bắt đầu từ đâu. |
| **Bottleneck** | Bước diễn giải feedback: sinh viên trộn feedback về bài làm với đánh giá về bản thân, nên không chuyển được feedback thành việc cần sửa. |
| **Impact** | Giảm động lực, trì hoãn sửa bài, bỏ lỡ thông tin hữu ích trong feedback, và dễ lặp lại lỗi cũ. |
| **Success Metric** | Tạo được ít nhất 3 action items từ feedback; giảm thời gian từ lúc nhận feedback đến lúc bắt đầu sửa; giảm self-rated distress sau bước cognitive reframing; không làm thay phần tự học của sinh viên. |
| **Boundary** | AI không chẩn đoán, không trị liệu, không đánh giá năng lực cá nhân, không chấm lại bài. AI chỉ hỗ trợ self-reflection, cognitive reframing và chuyển feedback thành action items; sinh viên tự kiểm tra và quyết định. |
| **Điểm AI can thiệp** | Sau khi sinh viên nhập feedback hoặc cảm xúc ban đầu, trước khi họ né đọc kỹ feedback hoặc trì hoãn sửa bài. |
| **Mức chọn** | **Workflow**: AI hỗ trợ một chuỗi bước rõ ràng gồm hỏi gợi mở, tách fact/thought/feeling, gợi ý reframe, và tạo action items. |
| **Rủi ro & HITL** | Rủi ro: AI an ủi sáo rỗng, hiểu sai feedback, hoặc làm người dùng phụ thuộc. HITL: sinh viên chọn/sửa câu reframe, tự kiểm action items, và tìm người thật/chuyên gia nếu distress nghiêm trọng. |

---

## 7. Rule / Workflow / Agent

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI / process fix** | Reflection template thủ công | Đủ nếu sinh viên tự điền đều và biết tự phản biện suy nghĩ | Dễ bỏ qua khi đang stress | Không chọn làm toàn bộ |
| **Rule** | Form cố định: fact → feeling → thought → evidence → action | Đủ cho case đơn giản | Ít empathy, khó phản hồi theo ngữ cảnh feedback cụ thể | Không chọn làm toàn bộ |
| **Workflow** | AI hỏi gợi mở → tách fact/thought/feeling → gợi ý reframe → tạo action items → người dùng chọn/sửa | Hợp vì các bước rõ, AI chỉ hỗ trợ ngôn ngữ và self-reflection | Có thể gợi ý chung chung hoặc quá tích cực | **Chọn** |
| **Agent** | Agent tự theo dõi feedback, tự đánh giá cảm xúc, tự lập kế hoạch học dài hạn | Chỉ cần nếu có nhiều nguồn dữ liệu, nhiều buổi học, nhiều quyết định động | Quá rộng, nhạy cảm, dễ vượt boundary | Chưa chọn |

Mức chọn:

```text
Workflow.
```

Vì sao chọn:

```text
Workflow đủ vì các bước can thiệp rõ: hỏi gợi mở, tách fact/thought/feeling, gợi ý reframe, tạo action items, rồi để sinh viên tự chọn/sửa. Không cần Agent vì AI không cần tự lập kế hoạch dài hạn hoặc tự quyết định bước tiếp theo.
```

---

## 8. Final decision draft

Decision hiện tại:

```text
Not Yet → cần validation 5 người và research thêm pattern/tool tương tự.
```

Lý do:

```text
Problem có actor, workflow, bottleneck và boundary rõ. Tuy nhiên trước khi Go, nhóm cần validate pain với 5 người và kiểm tra liệu non-AI reflection template đã đủ chưa. Nếu AI chỉ an ủi chung chung, solution không đáng làm.
```

Nếu Go, pilot nhỏ nhất:

```text
1. Lấy một feedback thật hoặc feedback mẫu.
2. Người dùng nhập cảm xúc/suy nghĩ ban đầu.
3. Workflow AI hỏi 4-5 câu gợi mở.
4. AI tạo 2-3 câu reframe và 3 action items.
5. Người dùng đánh giá: câu reframe có đúng không, action items có dùng được không.
```

Nếu Not Yet, cần validate:

```text
- Có bao nhiêu người thật sự cá nhân hóa feedback?
- Có bao nhiêu người trì hoãn sửa bài sau feedback?
- AI có giúp tạo action items tốt hơn template thủ công không?
- Boundary có đủ rõ để không thành AI therapist không?
```
