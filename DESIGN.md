# DESIGN.md — Landing page tiệm sách độc lập Gác Sách (MSR-43)

> Tài liệu thiết kế chốt cho sprint TEC-325. Dev (task Dev của sprint) dựng đúng tài liệu này, không tự thêm màu, font hay khối ngoài danh sách. QA đối chiếu bản dựng với tài liệu này, kèm kiểm tra đa dạng theo OPERATIONS.md mục 16.5.

## 0. Khác biệt so với các project gần nhất (bắt buộc theo mục 16.5 — đã đọc thật ngày 2026-10-25)

Thứ tự project mới nhất lấy từ mô tả task TEC-326 và đối chiếu trực tiếp DESIGN.md của các project gần nhất trên GitHub (đọc qua raw.githubusercontent.com ngày 2026-10-25):

1. **Thả Lỏng** (m-software-tha-long, TEC-319) — archetype ghi rõ trong file: **A3 Lệch tâm**; cặp font: **Playfair Display + Be Vietnam Pro**; nhiệt màu: **sáng-ấm nhạt** (nền #F4F1EA, chữ #2E2A33, nhấn tím oải hương #7C6A9E); điểm nhấn: "đường thở".
2. **Thời Khắc** (m-software-thoi-khac, TEC-312) — archetype: **A7 Typography-first**; cặp font: **Noto Serif Display + Be Vietnam Pro**; nhiệt màu: **tối-trung tính**.
3. **An Lạc** (m-software-an-lac, TEC-305) — archetype: **A2 Split (chia đôi)**; cặp font: **Lora + Be Vietnam Pro**; nhiệt màu: **sáng-ấm**.

Lựa chọn cho Gác Sách (đối chiếu trực tiếp với 3 project trên):

- **Archetype: A4 Bento-masonry** — KHÁC A3 của project liền trước (Thả Lỏng) và KHÁC A7 của project liền trước nữa (Thời Khắc), thỏa luật "không dùng lại archetype của 2 project liền trước"; cũng khác A2 của An Lạc. Cách bento thể hiện ở: khối kệ sách là lưới ô lệch cỡ (sách nổi bật chiếm ô 2×2, sách thường ô 1×1, xen kẽ ô ngang cho chủ đề); khối không gian đọc và sự kiện là 2 ô rộng đặt cạnh nhau, không chia đôi đều như A2.
- **Cặp font: EB Garamond + Be Vietnam Pro** — KHÁC nguyên cặp Playfair Display + Be Vietnam Pro của project liền trước (Thả Lỏng). EB Garamond là serif cổ điển hợp chất sách giấy, vẫn hỗ trợ tiếng Việt.
- **Nhiệt màu: sáng-ấm** — chuỗi nhiệt gần nhất: An Lạc sáng-ấm → Thời Khắc tối-trung tính → Thả Lỏng sáng-ấm nhạt → Gác Sách sáng-ấm: chỉ 2 project sáng-ấm liên tiếp ở cuối chuỗi (Thả Lỏng + Gác Sách), KHÔNG tạo chuỗi 3 cùng nhiệt màu, thỏa luật "tránh 3 project liên tiếp cùng một nhiệt màu".
- **Công thức gợi ý từ yêu cầu được GIỮ NGUYÊN** (nền #FBF6EE, chữ #2B2620, nhấn #A63D2F; EB Garamond + Be Vietnam Pro; tiệm sách cổ điển châu Âu): không vi phạm luật chống trùng nào nên không cần đổi; lý do giữ được ghi rõ tại đây.

## 1. Archetype và bố cục tổng thể

- **Archetype: A4 Bento-masonry** (lưới ô lệch cỡ, như các ngăn kệ sách).
- Bố cục 1 cột, chiều rộng tối đa 1120px, lề ngoài 24px (mobile) / 48px (desktop). Khoảng trắng giữa các khối: 96px (desktop), 64px (mobile).
- Thứ tự khối (không đổi): (1) hero ảnh lớn toàn màn hình → (2) giới thiệu + triết lý chọn sách → (3) kệ sách chọn lọc → (4) không gian đọc & sự kiện → (5) form liên hệ / đăng ký sự kiện → (6) chân trang.

## 2. Bảng màu — ĐÚNG 6 mã hex (không dùng màu ngoài bảng này)

| Mã | Vai trò |
|---|---|
| `#FBF6EE` | Nền chính — giấy kem, toàn trang |
| `#F1E7D3` | Nền phụ — giấy sậm hơn, dùng cho ô bento xen kẽ và chân trang |
| `#2B2620` | Chữ chính — nâu mực, tiêu đề và nội dung chính; cũng là màu đường kẻ kệ |
| `#6B5D4F` | Chữ phụ — nâu taupe, mô tả phụ, giá thứ cấp, chú thích ảnh |
| `#A63D2F` | Nhấn — đỏ gạch, nút chính, giá nổi bật, gáy sách nhấn |
| `#D8CBB2` | Đường viền — cát nhạt, viền ô bento, đường chia khối |

## 3. Font chữ

- **Tiêu đề: EB Garamond** (serif cổ điển, hỗ trợ tiếng Việt) — tiêu đề khối 40px desktop / 30px mobile, đậm vừa (600), giãn dòng 1.2.
- **Nội dung: Be Vietnam Pro** (sans hỗ trợ tiếng Việt) — nội dung 17px, giãn dòng 1.7; chú thích 14px, màu chữ phụ.
- Tên tiệm "Gác Sách" ở hero dùng EB Garamond 64px desktop / 40px mobile, màu chữ chính trên ảnh (có lớp phủ tối nhẹ 30% để chữ đọc được).

## 4. Phong cách tham chiếu

- **Tiệm sách cổ điển châu Âu kiểu Shakespeare and Company, Paris**: kệ gỗ tối, đèn vàng ấm, sách xếp dày, không khí yên tĩnh, cổ kính nhưng gần gũi — không sang chảnh lạnh, không tối giản hiện đại.

## 5. Quy tắc ảnh (ảnh mẫu, đồng tông)

- Tất cả ảnh mẫu đều tông ấm, ánh đèn vàng dịu, không ảnh lạnh/xanh; mỗi ảnh ghi chú "Ảnh mẫu" trong chú thích hoặc alt.
- Hero: toàn màn hình (100vh), tỉ lệ 16:9 crop, kệ sách gỗ đầy ắp dưới ánh đèn vàng ấm, không người làm chủ thể (tối đa 1 bóng người đọc mờ ở rìa).
- Bìa sách trong kệ: tỉ lệ 2:3, bìa rõ tên sách (tên sách mẫu, không bịa tác giả thật nổi tiếng).
- Không gian đọc: tỉ lệ 3:2, góc đọc có ghế gỗ + đèn bàn vàng.
- Sự kiện: tỉ lệ 4:3, buổi gặp gỡ/CLB đọc sách, ánh sáng ấm.
- Kiểm tra từng link ảnh trả HTTP 200 trước khi merge.

## 6. Điểm nhấn đặc sắc riêng — "Gáy sách làm vạch chia khối"

Mỗi tiêu đề khối đều ngồi trên một "kệ sách thu nhỏ": một đường kẻ ngang 3px màu nâu mực `#2B2620` (như mặt kệ gỗ), phía trên đường kẻ là 3–5 hình chữ nhật đứng (gáy sách) cao 12–20px không đều nhau, rộng 8–14px, chỉ dùng 4 màu trong bảng (đỏ gạch `#A63D2F`, nâu mực `#2B2620`, nâu taupe `#6B5D4F`, cát `#D8CBB2`). Gáy sách không chứa chữ. Đây là dấu hiệu nhận biết duy nhất của trang Gác Sách, lặp lại ở mọi khối, không dùng ở project nào trước đó.

## 7. Chi tiết từng khối

1. **Hero (100vh)**: ảnh kệ sách toàn màn hình + lớp phủ tối 30%; giữa ảnh: tên "Gác Sách", dòng giới thiệu 1 câu ("Tiệm sách độc lập trong hẻm yên tĩnh"), nút chính "Xem kệ sách" (nền đỏ gạch, chữ kem) neo tới khối kệ sách.
2. **Giới thiệu + triết lý**: 2 đoạn văn ngắn (tối đa 4 dòng/đoạn), tiêu đề có vạch "gáy sách"; không ảnh (để chữ thở).
3. **Kệ sách chọn lọc**: lưới bento — 1 ô lớn 2×2 cho sách nổi bật của tuần, các ô 1×1 cho sách theo chủ đề (văn học / thiếu nhi / nghệ thuật); mỗi ô: bìa 2:3, tên sách mẫu, giá mẫu ghi rõ "Giá mẫu" (80.000đ–350.000đ). Nền ô xen kẽ giấy kem / giấy sậm.
4. **Không gian đọc & sự kiện**: 2 ô rộng đặt cạnh nhau (desktop) / xếp dọc (mobile) — ô trái: ảnh góc đọc 3:2 + mô tả góc đọc; ô phải: 3 mục sự kiện (CLB đọc sách cuối tuần, ra mắt sách, góc đọc cho trẻ em), mỗi mục 2 dòng + ngày mẫu ghi rõ "Lịch mẫu".
5. **Form liên hệ / đăng ký sự kiện (CHỈ giao diện)**: 4 trường (họ tên, email, chọn sự kiện, lời nhắn) + nút "Gửi đăng ký" (nền đỏ gạch); submit chỉ preventDefault, không fetch/action/mailto/tel:, không hứa hẹn xử lý thật. Ghi chú dưới form: "Form demo — chưa gửi đi thật".
6. **Chân trang**: nền giấy sậm `#F1E7D3`; địa chỉ, điện thoại, giờ mở cửa, người phụ trách đều để placeholder `[CẦN BỔ SUNG]`, không bịa số liệu thật.

## 8. Responsive

- Breakpoint 768px: lưới bento chuyển từ 4 cột → 2 cột; ô 2×2 thành 2×1; 2 ô không gian/sự kiện xếp dọc.
- Breakpoint 480px: 1 cột cho mọi lưới; hero chữ 40px; khoảng trắng giữa khối 64px.
