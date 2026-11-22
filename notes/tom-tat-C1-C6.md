# Tóm Tắt Lý Thuyết Trọng Tâm (C1 – C6)

> Tổng hợp bám sát slide `C1.pdf` → `C6.pdf` (SGU).

---

## Chương 1 (`C1.pdf`): Tổng quan Hệ thống thông tin (HTTT)
- **Dữ liệu vs Thông tin vs Tri thức:**
  - *Dữ liệu (Data):* yếu tố rời rạc (con số, chuỗi ký tự).
  - *Thông tin (Information):* tập hợp dữ liệu được truyền từ nguồn phát đến nơi nhận, mang tính tĩnh, có ngữ cảnh, tường minh.
  - *Tri thức (Knowledge):* thông tin được diễn dịch thành sự hiểu biết (động, ngầm, phụ thuộc cá nhân).
- **Thành phần HTTT:** Con người, Dữ liệu (tĩnh/động), Quy trình/Xử lý, Công nghệ thông tin (phần cứng, phần mềm, truyền thông).
- **Phân loại HTTT theo tháp quản lý:**
  - Chiến lược → **ESS** (Executive Support System)
  - Quản lý → **DSS** (Decision Support System) & **MIS** (Management Information System)
  - Tác vụ → **TPS** (Transaction Processing System)
- **3 mức nhận thức:**
  - *Quan niệm:* "Cái gì?" — trừu tượng, độc lập phương tiện lưu trữ.
  - *Tổ chức:* "Ai, ở đâu, bao giờ?" — phân bố dữ liệu & xử lý.
  - *Vật lý:* "Như thế nào?" — phụ thuộc phần cứng, phần mềm cụ thể.
- **Quy trình phát triển HTTT:** Thác nước (Waterfall), Tăng trưởng, Xoắn ốc (Spiral - Boehm), RAD, RUP.
- **Phân rã hệ thống:** Modularity (đơn thể), **Coupling** (liên kết giữa các đơn thể → càng yếu càng tốt), **Cohesion** (chặt chẽ trong 1 đơn thể → càng cao càng tốt).

---

## Chương 2 (`C2.pdf`): Khởi tạo, Lập kế hoạch & Khảo sát hệ thống
- **Ước lượng thời gian (PERT):**
  - Công thức thời gian ước tính: $ET = \frac{o + 4r + p}{6}$ (`o`: lạc quan, `r`: thường gặp, `p`: bi quan).
  - Biểu diễn bằng **Sơ đồ Gantt** và **Sơ đồ PERT** (tìm đường dẫn tới hạn có $T_E = T_L$).
- **Đánh giá khả thi:**
  1. *Kinh tế:*
     - Giá trị hiện tại: $PV_n = \frac{Y}{(1+i)^n}$
     - $NPV_{\text{dự án}} = NPV_{\text{lợi nhuận lũy kế}} - NPV_{\text{chi phí lũy kế}}$
     - $ROI = \frac{NPV_{\text{dự án}}}{NPV_{\text{chi phí lũy kế}}}$
     - Điểm hòa vốn ($BEA$): $\frac{NPV_{\text{dòng tiền năm } i} - NPV_{\text{dòng tiền lũy kế } i}}{NPV_{\text{dòng tiền năm } i}}$
  2. *Kỹ thuật:* Độ lớn dự án, cấu trúc dự án, kinh nghiệm nhóm phát triển & người dùng (ma trận rủi ro Cash et al.).
  3. *Hoạt động*, *Lịch thực hiện*, *Hợp đồng & hợp luật*.
- **Khảo sát yêu cầu:** Phỏng vấn (câu hỏi mở/đóng, phỏng vấn nhóm), Bảng câu hỏi, Quan sát trực tiếp, Phân tích tài liệu, **JAD** (Joint Application Design), **Prototype**.
- **Đánh giá hiện trạng:** Thiếu/vắng, Kém hiệu lực, Tốn kém/dư thừa.
- **Phân nhóm yêu cầu:** Căn bản bắt buộc → Cần thiết → Mong muốn.

---

## Chương 3 (`C3.pdf`): Mô hình hóa xử lý
- **Sơ đồ dòng dữ liệu (DFD):**
  - 4 thành phần: **Ô xử lý** (động từ + bổ ngữ), **Dòng dữ liệu** (cụm danh từ), **Kho dữ liệu** (danh từ), **Đầu cuối** (danh từ).
  - Nguyên tắc: Không nối trực tiếp Đầu cuối ↔ Đầu cuối, Kho ↔ Kho, Đầu cuối ↔ Kho (phải qua Ô xử lý); mỗi ô xử lý phải có cả đầu vào và đầu ra.
- **7 luật căn bản tinh chế DFD (`T1`–`T7`):**
  - `T1`: Phân rã xử lý có dòng dữ liệu ở giữa.
  - `T2`: Phân rã xử lý có kho dữ liệu ở giữa (khác thời điểm).
  - `T3`: Phân rã xử lý không kết nối.
  - `T4`: Phân rã dòng dữ liệu.
  - `T5`: Hoàn chỉnh dòng dữ liệu (thêm xử lý trung gian).
  - `T6`: Phân rã kho dữ liệu thành các tập con.
  - `T7`: Tạo lập kho dữ liệu mới từ kho cũ qua ô xử lý.
- **Chuyển mô hình vật lý → quan niệm:** Loại bỏ phương tiện/hình thức (email, giấy, sổ...), loại bỏ yếu tố tổ chức/địa điểm, gộp các xử lý/kho trùng lặp nội dung.
- **Đặc tả xử lý:** Mã giả, Bảng quyết định (4 phần: Điều kiện, Giá trị ĐK, Hành động, Giá trị HĐ), Cây quyết định.

---

## Chương 4 (`C4.pdf`): Mô hình hóa dữ liệu mức quan niệm (ER & EER)
- **Thành phần ER:**
  - *Thực thể* (danh từ), *Mối kết hợp* (động từ), *Vai trò*, *Bản số* `(min, max)` (`min ∈ {0, 1, ..., k}`, `max ∈ {1, 2, ..., n}`).
  - *Thuộc tính:* Đơn trị, Đa hợp (Composite), Đa trị (`{...}`, có bản số `(0,n)`/`(1,n)`), Định danh (Khóa).
- **Mở rộng EER:**
  - **Tổng quát hóa / Chuyên biệt hóa:** Tính kế thừa; 2 cặp ràng buộc bao phủ:
    - Toàn phần (**t** - total) vs Bán phần (**p** - partial)
    - Riêng biệt (**e** - exclusive) vs Chồng chéo (**o** - overlapping)
    - 4 tổ hợp: `(t,e)`, `(t,o)`, `(p,e)`, `(p,o)`.
  - **Tập con:** Trường hợp đặc biệt chỉ có 1 thực thể chuyên biệt, luôn là `(p,e)`.
  - **Định danh bên ngoài / phối hợp:** Thực thể yếu định danh nhờ thực thể cha + thuộc tính riêng (ví dụ: Hạng mục đánh số thứ tự riêng trong từng Công trình).
  - **Mối kết hợp mở rộng:** Mối kết hợp định nghĩa trên một mối kết hợp khác (dùng cung định hướng).
- **5 quy tắc vàng khi vẽ ER/EER:**
  1. Mọi thuộc tính chỉ mô tả đặc trưng cho 1 thực thể duy nhất.
  2. Đặc trưng phụ thuộc nhiều thực thể → thuộc tính của mối kết hợp.
  3. Tổ hợp thể hiện của các thực thể tham gia mối kết hợp phải duy nhất.
  4. Nhánh nối vào mối kết hợp phải là nhánh bắt buộc (nếu không phải tách thành nhiều mối kết hợp).
  5. Đặc trưng phụ thuộc vào 1 thuộc tính → tồn tại thực thể ẩn cần tách ra.

---

## Chương 5 (`C5.pdf`): Thiết kế dữ liệu, Hệ thống & Giao diện
- **Thiết kế luận lý cấp cao:**
  - *Dữ liệu suy diễn:* Cân nhắc giữa tốc độ truy vấn (lưu sẵn) và chi phí cập nhật/đồng bộ.
  - *Chuyển đổi tổng quát hóa & tập con (3 cách):*
    1. Dùng thực thể tổng quát (gộp + thêm thuộc tính `LoaiE`).
    2. Dùng thực thể chuyên biệt (tách xuống các lớp con, chỉ áp dụng cho `(t,e)`).
    3. Dùng mối kết hợp `(0,1)`–`(1,1)` từ cha sang con.
- **Thiết kế luận lý cấp thấp (EER → Quan hệ):**
  - Loại bỏ định danh ngoài (kéo khóa cha xuống làm khóa thành phần), loại bỏ thuộc tính kết hợp & đa trị (tách bảng).
  - 1 thực thể → 1 quan hệ, định danh → khóa chính.
  - Mối kết hợp `1-1`: `(0,1)-(1,1)` đặt khóa ngoại bên `(1,1)`; `(1,1)-(1,1)` có thể gộp bảng.
  - Mối kết hợp `1-N`: Đưa khóa chính bên `1` sang làm khóa ngoại bên `N`.
  - Mối kết hợp `N-N` hoặc đa phân (≥ 3 ngôi): Tạo quan hệ mới có khóa chính gồm khóa chính các thực thể tham gia (+ thuộc tính riêng của mối kết hợp).
- **Thiết kế dữ liệu vật lý:**
  - *Non-intelligent key* (khóa tự tăng/ID thay thế cho khóa ghép phức tạp).
  - *Partition:* Ngang (chia dòng theo năm/khu vực) & Dọc (chia cột theo tần suất truy cập).
  - *Denormalization:* Gộp bảng `1-1` hoặc `1-N` để tối ưu truy vấn đọc nhiều.
- **Thiết kế phần mềm & giao diện:** Biểu đồ cấu trúc (Structured Chart), mô hình 3 lớp (Giao diện – Nghiệp vụ – Lưu trữ/CSDL), tính nhất quán/tiện dụng/hiệu quả.

---

## Chương 6 (`C6.pdf`): Chuẩn hóa CSDL
- **Hệ tiên đề Armstrong:**
  - Phản xạ: $Y \subseteq X \Rightarrow X \to Y$
  - Tăng trưởng: $X \to Y \Rightarrow XZ \to YZ$
  - Bắc cầu: $X \to Y, Y \to Z \Rightarrow X \to Z$
  - *3 hệ quả:* Luật hợp ($X \to Y, X \to Z \Rightarrow X \to YZ$), Luật bắc cầu giả ($X \to Y, WY \to Z \Rightarrow XW \to Z$), Luật phân rã ($X \to Y, Z \subset Y \Rightarrow X \to Z$).
- **Phủ tối tiểu (3 bước):**
  1. Loại bỏ thuộc tính dư thừa ở vế trái (thử bỏ $A$ khỏi $X \to Y$; nếu $(X \setminus A)^+$ chứa $Y$ thì $A$ dư thừa).
  2. Tách vế phải mỗi PTH còn 1 thuộc tính.
  3. Loại bỏ PTH dư thừa (bỏ $X \to A$ khỏi tập; nếu $X^+$ theo tập còn lại vẫn chứa $A$ thì $X \to A$ dư thừa).
- **Tìm tất cả khóa (thuật toán `TN` & `TG`):**
  - `TN`: thuộc tính chỉ ở vế trái hoặc không xuất hiện trong $F$.
  - `TG`: thuộc tính xuất hiện ở cả vế trái và vế phải.
  - Lần lượt xét $TN \cup X_i$ (với $X_i \subseteq TG$), tìm $(TN \cup X_i)^+ = U$ để lấy siêu khóa, rồi loại siêu khóa không tối thiểu.
- **Các dạng chuẩn (cho $F_{1tt}$ với $A \notin X$):**
  - **1NF:** Mọi thuộc tính mang giá trị nguyên tố, có khóa chính.
  - **2NF:** Đạt 1NF và không có phụ thuộc hàm riêng phần (mọi thuộc tính không khóa phụ thuộc đầy đủ vào mọi khóa).
  - **3NF:** Đạt 1NF và với mọi $X \to A$ ($A \notin X$), **$X$ là siêu khóa** HOẶC **$A$ là thuộc tính khóa**.
  - **BCNF:** Đạt 1NF và với mọi $X \to A$ ($A \notin X$), **$X$ là siêu khóa**.
