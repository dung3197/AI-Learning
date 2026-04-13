# Bài 1 — AI là gì? Bản đồ toàn cảnh AI

## 1) AI là gì?

**AI (Artificial Intelligence)** là lĩnh vực làm cho máy tính thực hiện những việc mà ta thường xem là cần “trí thông minh” của con người, ví dụ:

* nhận diện ảnh
* hiểu ngôn ngữ
* trả lời câu hỏi
* dự đoán
* ra quyết định
* lập kế hoạch

### Cách hiểu đơn giản nhất

Nếu phần mềm chỉ làm đúng theo các luật bạn viết cứng từ trước, nó là **automation thông thường**.

Nếu hệ thống có khả năng **học mẫu từ dữ liệu** hoặc **suy ra hành động phù hợp từ ngữ cảnh**, ta đang tiến gần đến AI.

### Ví dụ

* Máy tính cộng 2 + 2 = 4: chưa phải AI
* Hệ thống phát hiện email spam từ hàng triệu email trước đó: đây là AI
* Mô hình đọc câu hỏi tiếng Việt và trả lời: đây là AI
* Hệ thống tự chọn công cụ phù hợp, gọi API, rồi tổng hợp kết quả để hoàn thành nhiệm vụ nhiều bước: đây là dạng **agentic AI**

---

## 2) Bản đồ khái niệm: AI, ML, Deep Learning, NLP, LLM, Agentic AI

Hãy tưởng tượng như sau:

* **AI** là cái ô lớn nhất
* **Machine Learning (ML)** là một nhánh trong AI
* **Deep Learning (DL)** là một nhánh trong ML
* **NLP** là lĩnh vực xử lý ngôn ngữ tự nhiên
* **LLM** là một loại mô hình lớn, thường dùng trong NLP
* **Agentic AI** là cách xây hệ thống AI có khả năng dùng công cụ, lập kế hoạch, và thực hiện workflow nhiều bước

### Quan hệ giữa chúng

#### AI

Khái niệm rộng nhất: mọi kỹ thuật khiến máy “có vẻ thông minh”.

#### Machine Learning

Máy không cần bạn viết hết mọi luật. Thay vào đó, bạn cho nó dữ liệu để nó học ra quy luật.

#### Deep Learning

Một họ mô hình ML dùng mạng nơ-ron nhiều tầng để học biểu diễn phức tạp.

#### NLP

Xử lý ngôn ngữ của con người: văn bản, câu hỏi, dịch máy, tóm tắt, phân tích cảm xúc.

#### LLM

Mô hình ngôn ngữ lớn, thường dựa trên kiến trúc Transformer, được huấn luyện trên lượng văn bản rất lớn để dự đoán token tiếp theo và từ đó làm được nhiều tác vụ ngôn ngữ. Hugging Face mô tả nhiều tác vụ chuẩn như summarization, question answering, sequence classification, NER. OpenAI cũng mô tả các mô hình ngôn ngữ có thể hiểu và sinh ngôn ngữ hoặc code. ([Hugging Face][2])

#### Agentic AI

Không chỉ “trả lời một lượt”, mà còn có thể:

* chia nhỏ nhiệm vụ
* quyết định bước tiếp theo
* dùng tool
* giữ state / memory
* tương tác với hệ thống bên ngoài

OpenAI mô tả agents là các ứng dụng có thể lập kế hoạch, gọi công cụ, cộng tác giữa các chuyên gia và giữ đủ trạng thái để hoàn tất công việc nhiều bước. ([OpenAI Developers][3])

---

## 3) Trực giác cực dễ hiểu: 3 cấp độ “thông minh” của máy

### Cấp 1: Rule-based

Bạn viết luật cứng.

Ví dụ:

* Nếu email chứa “trúng thưởng”, “miễn phí”, “click ngay” thì đánh dấu spam.

Ưu điểm:

* dễ hiểu
* dễ kiểm soát

Nhược điểm:

* dễ vỡ khi dữ liệu phức tạp
* không học được mẫu mới

### Cấp 2: Machine Learning

Bạn không viết tất cả luật. Bạn đưa dữ liệu nhãn:

* email spam
* email không spam

Máy học từ dữ liệu để dự đoán email mới.

### Cấp 3: Generative AI / LLM / Agent

Hệ thống không chỉ phân loại mà còn:

* sinh câu trả lời
* tóm tắt tài liệu
* truy xuất kiến thức
* dùng công cụ
* lập kế hoạch nhiều bước

---

## 4) Cốt lõi của AI thật ra xoay quanh 4 thứ

Đây là phần quan trọng nhất của cả khóa. Hầu như mọi hệ AI đều xoay quanh 4 thành phần:

### (1) Dữ liệu

Máy học từ dữ liệu.

Ví dụ:

* hình ảnh mèo/chó
* lịch sử giao dịch ngân hàng
* log hệ thống
* email
* tài liệu nội bộ
* hội thoại
* sensor stream

### (2) Biểu diễn dữ liệu

Máy không hiểu chữ hay ảnh theo cách con người hiểu. Mọi thứ cuối cùng phải biến thành số.

Ví dụ:

* ảnh → ma trận pixel
* văn bản → token → vector
* bảng giao dịch → cột số, cột hạng mục mã hóa thành số

### (3) Mô hình

Mô hình là “bộ máy toán học” tìm quan hệ giữa đầu vào và đầu ra.

Ví dụ:

* từ giao dịch → dự đoán gian lận
* từ câu hỏi + tài liệu → sinh câu trả lời
* từ lịch sử bán hàng → dự đoán nhu cầu

### (4) Mục tiêu tối ưu

Mô hình phải có mục tiêu để biết thế nào là đúng hơn.

Ví dụ:

* dự đoán spam đúng nhiều nhất
* lỗi dự đoán nhỏ nhất
* xác suất câu tiếp theo hợp lý nhất

---

## 5) AI không phải “phép màu”, mà là tối ưu hóa trên dữ liệu

Đây là bản chất rất quan trọng.

Nhiều người mới học thấy AI như một “hộp đen biết suy nghĩ”. Thực tế gần đúng hơn là:

> AI hiện đại là các hệ thống toán học học mẫu từ dữ liệu, tối ưu một mục tiêu nào đó, rồi dùng những mẫu đã học để dự đoán hoặc sinh đầu ra.

Nói ngắn gọn:

* có dữ liệu
* có mô hình
* có hàm đo sai số
* có thuật toán tối ưu
* mô hình cải thiện dần

---

## 6) Ví dụ trực quan số 1: Phân loại táo và cam

Giả sử bạn có dữ liệu:

| Quả | Trọng lượng | Màu sắc  | Loại |
| --- | ----------: | -------- | ---- |
| A   |        180g | đỏ xanh  | táo  |
| B   |        170g | cam      | cam  |
| C   |        200g | đỏ       | táo  |
| D   |        160g | cam vàng | cam  |

Bạn đưa cho máy nhiều ví dụ như vậy.

Khi có quả mới:

* 190g
* màu đỏ xanh

Máy dự đoán: **táo**

### Điều gì xảy ra phía sau?

Máy đang học một “ranh giới” để tách hai nhóm.

Con người nhìn bằng mắt.
Mô hình nhìn bằng số.

Đây chính là tư duy nền tảng của ML:

* dữ liệu vào
* học mẫu
* áp dụng cho dữ liệu chưa từng thấy

---

## 7) Ví dụ trực quan số 2: AI hiểu câu chữ như thế nào?

Giả sử có hai câu:

* “Tôi thích con mèo này”
* “Tôi yêu chú mèo này”

Con người thấy hai câu gần nghĩa.

Máy tính thô sơ thì thấy đây là hai chuỗi ký tự khác nhau.

Muốn máy “hiểu gần nghĩa”, ta phải biến câu thành **biểu diễn số học** sao cho các câu gần nghĩa có vector gần nhau hơn. Đây là ý tưởng quan trọng dẫn đến **embedding**, và sau này là nền tảng của semantic search, RAG, recommendation, clustering văn bản. OpenAI mô tả embedding là vector số biểu diễn input; API embeddings trả về một vector float cho mỗi input. ([platform.openai.com][4])

---

## 8) AI truyền thống khác Generative AI như thế nào?

### AI truyền thống

Thường trả lời một trong vài kiểu:

* phân loại
* hồi quy
* phát hiện bất thường
* gợi ý
* clustering

Ví dụ:

* giao dịch này có gian lận không?
* tháng tới bán được bao nhiêu?
* khách hàng này thuộc nhóm nào?

### Generative AI

Không chỉ chọn nhãn, mà còn **sinh nội dung mới**:

* sinh văn bản
* sinh code
* tóm tắt
* dịch
* hỏi đáp
* sinh ảnh / âm thanh

### Ví dụ đối chiếu

* ML truyền thống: “Email này là spam hay không?”
* Generative AI: “Hãy tóm tắt nội dung email này và soạn trả lời lịch sự”

---

## 9) NLP là gì?

**NLP (Natural Language Processing)** là lĩnh vực giúp máy xử lý ngôn ngữ con người.

Các bài toán NLP phổ biến:

* phân loại văn bản
* phân tích cảm xúc
* gán nhãn thực thể (NER)
* dịch máy
* tóm tắt
* hỏi đáp
* trích xuất thông tin

Hugging Face liệt kê các tác vụ chuẩn như summarization, sequence classification, question answering, named entity recognition. ([Hugging Face][2])

### Ví dụ

Câu:

> “Ngân hàng A thông báo khách hàng Nguyễn Văn B mở tài khoản tại Hà Nội”

NLP có thể tách ra:

* “Ngân hàng A” → tổ chức
* “Nguyễn Văn B” → người
* “Hà Nội” → địa điểm

---

## 10) LLM là gì?

**LLM (Large Language Model)** là mô hình ngôn ngữ lớn.

### Hiểu cực trực giác

LLM được huấn luyện trên lượng văn bản rất lớn để học:

* quy luật ngôn ngữ
* quan hệ giữa từ và ngữ cảnh
* cấu trúc câu
* tri thức thống kê
* cách tiếp tục chuỗi văn bản hợp lý

### Cốt lõi vận hành

Ở mức rất cơ bản, LLM thường học nhiệm vụ:

> Dự đoán token tiếp theo

Ví dụ:

* “Hôm nay trời rất ...”
  Mô hình dự đoán token tiếp theo có thể là:
* đẹp
* nóng
* lạnh

Làm việc này ở quy mô cực lớn, mô hình học được cấu trúc ngôn ngữ rất mạnh.

### Nhưng cần nhớ

LLM **không “hiểu” theo đúng nghĩa con người**. Nó rất mạnh trong việc mô hình hóa mẫu ngôn ngữ và ngữ cảnh, nhưng vẫn có thể:

* bịa thông tin
* suy luận sai
* tự tin nhưng sai
* nhạy với prompt và ngữ cảnh

---

## 11) Agentic AI là gì?

Đây là phần bạn đặc biệt muốn hiểu, nên tôi làm thật rõ.

### Chatbot thường

Bạn hỏi một câu → mô hình trả một câu.

### Agentic AI

Bạn giao mục tiêu:

> “Hãy đọc log lỗi, kiểm tra ticket liên quan, tra tài liệu runbook, rồi đề xuất hướng xử lý.”

Hệ thống có thể:

1. phân tích nhiệm vụ
2. quyết định cần dùng công cụ nào
3. gọi tool
4. đọc kết quả
5. thực hiện bước tiếp theo
6. tổng hợp câu trả lời cuối

OpenAI mô tả agent là workflow gồm agent, tools, control-flow logic; còn agents có thể lập kế hoạch, gọi công cụ và giữ trạng thái cho công việc nhiều bước. ([OpenAI Developers][5])

### Ví dụ cho Data Engineer

Một agent nội bộ có thể:

* đọc incident từ Slack/Jira
* truy vấn metadata catalog
* lấy schema từ Kafka registry
* kiểm tra DAG Airflow lỗi
* đọc runbook
* tạo bản tóm tắt nguyên nhân khả dĩ

Đây không còn là “chat đơn thuần”, mà là **AI gắn với hạ tầng dữ liệu và workflow doanh nghiệp**.

---

## 12) Vì sao AI đặc biệt liên quan tới Big Data?

AI càng mạnh khi có:

* dữ liệu đủ nhiều
* dữ liệu đủ sạch
* pipeline đủ ổn định
* khả năng xử lý ở quy mô lớn

Đó là lý do Big Data và AI đi cùng nhau.

### Mối liên hệ cốt lõi

* **Big Data** lo việc thu thập, lưu trữ, xử lý, phục vụ dữ liệu ở quy mô lớn
* **AI/ML/LLM** dùng dữ liệu đó để học, suy luận, dự đoán, hoặc sinh nội dung

### Ví dụ thực tế

* Kafka dùng cho event streaming và data pipelines thời gian thực. ([kafka.apache.org][1])
* Spark Structured Streaming giúp xây pipeline xử lý stream với API thống nhất. ([spark.apache.org][6])
* Spark MLlib cung cấp thư viện ML phân tán trên Spark. ([spark.apache.org][7])
* Ray Data tập trung vào data processing cho AI workloads như preprocessing, batch inference, data loading. ([docs.ray.io][8])

### Ý nghĩa cho Data Engineer

Nếu không có người làm dữ liệu:

* dữ liệu không sạch
* dữ liệu không đúng schema
* dữ liệu không đến đúng lúc
* mô hình không có input tốt
* agent không có tri thức đáng tin để truy xuất

Nói thẳng:

> **AI tốt phụ thuộc rất lớn vào data engineering tốt.**

---

## 13) Data Engineer đóng vai trò gì trong hệ AI?

Một người mới học AI nhưng đang định hướng Data Engineer cần hiểu điều này thật rõ.

### Data Engineer không nhất thiết phải là người huấn luyện mô hình

Nhưng Data Engineer là người thường xây:

* ingestion pipeline
* ETL/ELT
* batch/stream processing
* feature pipeline
* document pipeline cho RAG
* metadata, lineage, quality
* serving layer cho AI inference

### Ví dụ trong hệ RAG

Một chatbot nội bộ trả lời theo tài liệu công ty cần:

1. ingest PDF / docs / wiki
2. parse và chunk tài liệu
3. sinh embedding
4. index vào vector store
5. truy xuất tài liệu liên quan
6. gửi context vào LLM
7. log truy vấn để đánh giá chất lượng

Trong chuỗi này, Data Engineer có thể phụ trách phần 1–5 và 7, thậm chí cả orchestration toàn bộ pipeline.

---

## 14) Demo trực quan: phân biệt “AI model”, “AI system”, “AI agent”

### Demo A — AI model

Input:

> “Tóm tắt đoạn văn này”

Output:

> mô hình sinh tóm tắt

Đây là **mô hình** làm một tác vụ.

### Demo B — AI system

Input:

> “Tóm tắt 1000 ticket support trong tháng này”

Hệ thống sẽ:

* lấy dữ liệu từ warehouse
* gom theo chủ đề
* gọi mô hình tóm tắt
* xuất dashboard

Đây là **AI system**, vì có pipeline xung quanh model.

### Demo C — AI agent

Input:

> “Phân tích vì sao pipeline customer_360 thất bại sáng nay và đề xuất cách xử lý”

Agent có thể:

* đọc alert
* tra log Airflow
* tra job Spark
* kiểm tra schema mới nhất
* đối chiếu runbook
* viết báo cáo khuyến nghị

Đây là **agent**, vì nó chủ động chạy workflow nhiều bước với tools.

---

## 15) Một sơ đồ tư duy đơn giản để bạn nhớ lâu

Hãy nhớ chuỗi sau:

**Dữ liệu → Biểu diễn → Mô hình → Tối ưu → Suy luận → Ứng dụng**

Và với LLM/Agent thì mở rộng thành:

**Dữ liệu / tài liệu / sự kiện → token / embedding → LLM → tools / retrieval / memory → workflow → business outcome**

---

## 16) Những hiểu lầm người mới thường mắc

### Hiểu lầm 1: AI = chatbot

Sai. Chatbot chỉ là một dạng ứng dụng AI.

### Hiểu lầm 2: Có LLM là đủ

Sai. Muốn dùng thực tế còn cần:

* dữ liệu
* retrieval
* orchestration
* guardrails
* monitoring
* evaluation

### Hiểu lầm 3: Data Engineer ít liên quan AI

Sai. Trong nhiều tổ chức, AI muốn chạy được ở production thì phụ thuộc rất mạnh vào pipeline, quality, metadata, serving và observability.

### Hiểu lầm 4: AI “biết sự thật”

Sai. AI tạo câu trả lời có vẻ hợp lý theo xác suất và ngữ cảnh; không phải lúc nào cũng đúng.

---

## 17) Tóm tắt cực ngắn của Bài 1

* AI là lĩnh vực giúp máy làm các việc cần “trí thông minh”.
* ML là nhánh của AI học từ dữ liệu.
* Deep Learning là nhánh của ML dùng mạng nơ-ron.
* NLP xử lý ngôn ngữ con người.
* LLM là mô hình ngôn ngữ lớn, rất mạnh trong tác vụ ngôn ngữ.
* Agentic AI là AI có thể dùng công cụ và thực hiện workflow nhiều bước.
* Big Data cung cấp nền tảng dữ liệu để AI hoạt động ở quy mô lớn.
* Data Engineer là mắt xích cực quan trọng để AI vận hành thực tế.

---

# Quiz Bài 1 — 20 câu kiểm tra

## Phần A. Trắc nghiệm

1. AI là gì theo nghĩa rộng nhất?
2. Điểm khác nhau chính giữa rule-based system và machine learning là gì?
3. Deep Learning thuộc nhánh nào?
4. NLP xử lý loại dữ liệu gì?
5. LLM thường mạnh nhất với loại bài toán nào?
6. “Dự đoán token tiếp theo” liên quan tới loại mô hình nào?
7. Embedding dùng để làm gì?
8. Agentic AI khác chatbot một lượt ở điểm nào?
9. Big Data hỗ trợ AI ở những mặt nào?
10. Vì sao AI không nên được xem là “phép màu hiểu biết tuyệt đối”?

## Phần B. Đúng / Sai

11. Mọi chatbot đều là agent.
12. ML luôn cần dữ liệu có nhãn.
13. LLM là một phần của AI.
14. Data Engineer không liên quan nhiều đến hệ AI production.
15. NLP chỉ dùng cho dịch ngôn ngữ.

## Phần C. Tự luận ngắn

16. Hãy tự giải thích bằng lời của bạn: AI, ML, Deep Learning khác nhau thế nào.
17. Hãy nêu 3 ví dụ ứng dụng AI trong doanh nghiệp.
18. Hãy nêu 1 ví dụ cho AI model, 1 ví dụ cho AI system, 1 ví dụ cho AI agent.
19. Vì sao Data Engineer quan trọng trong hệ RAG hoặc LLM application?
20. Theo bạn, điều gì là “cốt lõi” nhất của AI sau Bài 1?

---

# Đáp án ngắn gợi ý cho Quiz

Tôi chưa đưa đáp án chi tiết ngay để bạn tự nghĩ trước. Nhưng nếu bạn muốn, ở tin nhắn kế tiếp tôi sẽ:

* chấm từng câu
* giải thích đáp án
* rồi mới dạy **Bài 2: Toán nền tảng tối thiểu cho AI**

---

# Bạn nên học Bài 1 trong bao lâu?

* Đọc và suy ngẫm: 45–60 phút
* Làm quiz: 15–25 phút
* Hỏi lại những điểm chưa rõ: 15–30 phút

Tổng: **khoảng 1.5 giờ**

---

# Gợi ý học thật hiệu quả

Sau Bài 1, bạn chưa cần code ngay. Điều quan trọng là bạn phải trả lời được bằng ngôn ngữ của chính mình:

* AI là gì?
* LLM là gì?
* Agent khác chatbot thế nào?
* Dữ liệu đóng vai trò gì?
* Data Engineer đứng ở đâu trong bức tranh AI?

---
