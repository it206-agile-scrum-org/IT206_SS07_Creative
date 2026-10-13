# Cơ chế theo dõi kế hoạch Sprint – Đội RikkeiGo

**Người thiết kế:** Lan (Scrum Master)  **Người dùng:** Đức (Product Owner), 4 Developers
**Phạm vi:** áp dụng cho mọi Sprint (Sprint 2 tuần, 4 Developers). Số liệu dùng để **đội tự điều chỉnh kế hoạch**, không dùng làm KPI hay so sánh giữa các đội. SP không quy đổi sang giờ.

**Ba vấn đề cần giải quyết:** (1) cuối Sprint mới biết Sprint Goal trượt; (2) mỗi Planning lại tranh luận nên nhận bao nhiêu SP; (3) quản lý muốn xếp hạng đội theo Velocity.

---

## Phần 1 – Thiết kế cơ chế (4 thành phần)

| # | Thành phần | Dữ liệu đầu vào | Ai cập nhật | Khi nào | Giúp đội quyết định điều gì |
|---|---|---|---|---|---|
| 1 | **Bảng Capacity** | Số ngày làm việc của từng Developer trừ nghỉ phép, họp, hỗ trợ ngoài Sprint; so với Sprint chuẩn (4 người × 10 ngày) | Từng Developer tự điền ngày vắng; Lan tổng hợp thành hệ số (vd. 34/40 = 0,85) | Trước Planning 1–2 ngày | Sprint này đội "to" hay "nhỏ" hơn bình thường bao nhiêu để điều chỉnh khối lượng nhận |
| 2 | **Dự báo & Sprint Goal** (Planning) | Dải Velocity gần đây (18, 20, 19, 15, 13), hệ số Capacity, Product Backlog đã refine, Sprint Goal do Đức đề xuất | Đức chốt Goal; Developers tự chọn mức nhận; Lan ghi vào bảng dự báo | Ngày 1 Sprint | Nhận bao nhiêu SP: lấy **dải dự báo** (không phải một con số) = trung bình 3 Sprint gần nhất × hệ số Capacity. Chia hạng mục thành **Cốt lõi** (đảm bảo Goal) và **Mở rộng** (làm nếu còn dư). Chỉ cam kết Goal, không cam kết tổng SP |
| 3 | **Theo dõi trong Sprint** (Burndown + bảng công việc) | Burndown SP còn lại (chỉ trừ khi hạng mục *Done* theo DoD), số hạng mục đang làm, hạng mục bị chặn, "tuổi" hạng mục ở cột *Đang làm* | Developers cập nhật tại Daily Scrum; Lan rà soát; **điểm kiểm tra ngày 5** có Đức tham gia | Hằng ngày; ngày 5 kiểm tra Goal | Sprint Goal còn an toàn không? Nếu không: giữ, đổi hay bỏ bớt phạm vi, **lấy Sprint Goal làm chuẩn** (bỏ hạng Mở rộng trước, rồi tách/hoãn hạng mục ngoài Goal) |
| 4 | **Nhật ký xu hướng giữa các Sprint** | Velocity từng Sprint, Goal đạt/không, SP dự báo so với SP Done, SP chuyển sang Sprint sau, nguyên nhân (ghi từ Retro) | Lan cập nhật cùng Developers | Cuối mỗi Sprint (Review/Retro) | Dải Velocity tham chiếu cho Sprint sau; xu hướng bất thường (vd. 19 → 15 → 13) có cần xử lý ở Retro không (thay đổi thành viên, nợ kỹ thuật, hạng mục quá lớn…). Chỉ đội và Đức xem để lập kế hoạch |

**Quy tắc vận hành chung**
- Velocity chỉ là *căn cứ dự báo* của riêng đội; không đặt chỉ tiêu "Velocity phải tăng".
- Burndown chỉ là *tín hiệu để hỏi*, không phải điểm số; không "chia nhỏ điểm" hay báo Done sớm để đồ thị đẹp.
- Mỗi Sprint dùng đúng 4 thành phần trên, tổng thời gian duy trì khoảng 10–15 phút/ngày, gồm cả Daily Scrum.

---

## Phần 2 – Xử lý tình huống

### Tình huống 1: Ngày 4–6 Burndown nằm ngang dù Developers vẫn làm đủ giờ
- **Phát hiện:** Quy tắc *"Burndown phẳng 2 ngày liên tiếp"* kích hoạt trao đổi ngay ở Daily Scrum ngày 5. Lan nhìn bảng công việc để xem có hạng mục lớn nằm lâu ở *Đang làm*, nhiều việc làm song song, hay hạng mục bị chặn không. Burndown phẳng thường vì SP chỉ giảm khi hạng mục Done, chứ không phải vì không làm việc.
- **Phản ứng:** Tại điểm kiểm tra ngày 5, đội dồn sức cho hạng mục gần xong (swarming), gỡ chặn, hoặc tách hạng mục lớn thành phần nhỏ Done được. Nếu Goal vẫn có nguy cơ, Đức và Developers cùng bỏ hạng Mở rộng hoặc giảm phạm vi theo Sprint Goal. Không quy trách nhiệm cá nhân và không đổi cách tính SP.

### Tình huống 2: Sprint tới 2/4 Developers nghỉ mỗi người 3 ngày, Capacity giảm ~15%
- **Phát hiện:** Bảng Capacity (thành phần 1) tính ra 34/40 = 0,85 trước Planning; Lan báo Đức sớm để chuẩn bị Goal gọn hơn.
- **Phản ứng:** Dự báo = trung bình 3 Sprint gần nhất (19, 15, 13 → khoảng 15,7) × 0,85 ≈ **13–14 SP**, đưa ra dưới dạng dải (khoảng 12–14). Xếp hạng mục Cốt lõi vào khoảng thấp của dải, phần còn lại là Mở rộng; ghi nhận ở Retro rằng Velocity giảm do Capacity, không phải do hiệu suất.

### Trả lời quản lý về đề nghị xếp hạng đội theo Velocity
> "Velocity là thước đo nội bộ, dựa trên cách mỗi đội tự ước lượng SP nên không so sánh được giữa các đội, và nếu đem xếp hạng thì đội sẽ có xu hướng thổi phồng điểm thay vì giao giá trị thật. Để theo dõi đội, anh/chị nên xem **mức đạt Sprint Goal qua các Sprint, phản hồi của người dùng/Stakeholder ở Sprint Review, mức độ dự báo sát thực tế (dải dự báo so với kết quả), chất lượng sản phẩm (lỗi sau phát hành) và tình trạng sức khỏe đội (từ Retro)**."

---

## Kết quả mong đợi
- Rủi ro Sprint Goal được phát hiện **từ ngày 5** thay vì ngày cuối Sprint.
- Planning dựa trên một công thức dự báo chung (dải Velocity × hệ số Capacity) nên giảm tranh luận về số SP.
- Số liệu phục vụ lập kế hoạch và cải tiến của đội, không trở thành chỉ tiêu hay công cụ xếp hạng.
