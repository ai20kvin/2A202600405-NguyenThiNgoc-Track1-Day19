# PITCH MEMO — TrustLayerAI

**Audience:** Seed VC (Early-stage AI Infrastructure / Enterprise SaaS)

---

## 1. THE PROBLEM

Các doanh nghiệp triển khai chatbot nội bộ (RAG / Enterprise Search) đang phải tin mù vào câu trả lời của AI — không có cách nào biết **khi nào bot đang bịa dữ liệu, bỏ qua tài liệu quan trọng, hay trả lời sai chính sách nội bộ**.

IT Manager tại một tập đoàn 2.000 nhân viên ở TP.HCM cho biết nhóm của anh mất **trung bình 3 giờ/tuần** truy tìm nguồn gốc câu trả lời sai từ chatbot HR — và vẫn không thể nói với ban lãnh đạo mức độ tin cậy thực sự là bao nhiêu.

---

## 2. THE INSIGHT

Vấn đề thực sự không phải là chatbot nội bộ trả lời sai — mà là **doanh nghiệp không có hệ thống đo lường để phát hiện khi nào nó sai**, dẫn đến toàn bộ tổ chức hoặc tin 100% hoặc từ bỏ hoàn toàn.

*(Các công ty đang dùng Confluence, SharePoint, Notion nhưng không ai build lớp đánh giá chất lượng đầu ra — đây là khoảng trống thực sự trong enterprise AI stack.)*

---

## 3. THE SOLUTION

**TrustLayerAI** là nền tảng đánh giá và monitoring liên tục cho chatbot nội bộ RAG/Enterprise Search — không yêu cầu thay đổi hạ tầng hiện có.

**Differentiator:** Không giống các tool eval chạy offline một lần (như RAGAS, DeepEval), TrustLayerAI hoạt động **in-production** — mỗi câu hỏi từ nhân viên được score tự động theo 5 chiều: Faithfulness, Relevancy, Context Recall, Hallucination Risk, và Policy Compliance — và dashboard real-time hiển thị cho IT/Ops ngay lập tức.

**AI giúp:** Mô hình judge nhỏ chạy song song với chatbot chính, so sánh output với tài liệu nguồn, tự động gắn cờ (flag) câu trả lời nghi ngờ và đề xuất reranking — không cần con người review từng query.

---

## 4. WHY NOW

Chi phí chạy LLM judge giảm 10x trong 12 tháng qua (GPT-4o mini, Claude Haiku), lần đầu tiên khả thi về kinh tế để đánh giá **100% queries** thay vì chỉ sample.

Đồng thời, làn sóng enterprise tại Đông Nam Á triển khai RAG chatbot đang bước vào giai đoạn *"đã deploy xong, giờ lo chất lượng"* — nhu cầu observability xuất hiện đúng thời điểm sản phẩm có thể đáp ứng.

---

## 5. TRACTION / PROOF

- **3 pilot khách hàng** (1 ngân hàng, 1 công ty bảo hiểm, 1 tập đoàn bán lẻ) — tổng ~4.500 nhân viên đang dùng chatbot nội bộ
- **Aha moment:** sau 7 ngày dùng TrustLayerAI, IT Manager của pilot đầu tiên phát hiện 23% câu trả lời từ bot HR có Hallucination Risk > 0.7 — con số mà trước đây họ hoàn toàn không biết
- **NPS pilot:** 72 (benchmark SaaS B2B: 40–50)
- **MRR hiện tại:** $1.200/tháng (3 pilots đang trả tiền)
- **LTV/CAC dự kiến:** 5.2x, payback 5 tháng (dựa trên deal size $400/tháng/khách, CAC ~$2.000 qua outbound enterprise)

---

## 6. THE ASK

Gọi **$300.000 USD Seed** để:
1. Mở rộng lên 20 khách hàng enterprise trong 9 tháng (target: MRR $8.000+)
2. Build thêm connector cho top 5 RAG framework phổ biến tại SEA (LlamaIndex, LangChain, Azure AI Search, Vertex AI Search, Haystack)
3. Tuyển 1 Enterprise Sales Rep có background B2B SaaS tại VN/SG

**Milestone 12 tháng:** $10.000 MRR, 15+ paying enterprise customers, sẵn sàng Series A conversation.
