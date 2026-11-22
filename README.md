# ONTAP — Cơ Sở Dữ Liệu Nâng Cao (SGU K24)

Thư mục tổng hợp slide bài giảng, đề ôn thi giữa kỳ và bộ ghi chú/lời giải chuẩn hóa để ôn tập đồng bộ giữa **máy tính ở nhà (Local)** và **điện thoại (Antigravity Web / Remote Desktop)**.

## Cấu trúc thư mục

```text
ONTAP/
├── AGENTS.md                     # "Bộ não" hướng dẫn AI giữ nguyên ngữ cảnh ở mọi nơi
├── README.md                     # File này
├── 03. Đê Ôn Tập -CSDL NC.pdf    # Đề ôn thi giữa kỳ (4 câu - 120 phút)
├── C1.pdf ... C6.pdf             # Slide bài giảng gốc (Chương 1 -> Chương 6)
└── notes/
    ├── tom-tat-C1-C6.md          # Tóm tắt trọng tâm 6 chương theo đúng slide
    ├── giai-de-03-csdl-nc.md     # Lời giải chi tiết Đề 03 (EER, Chase, SQL Server)
    └── ghi-chu-on-tap.md         # Nhật ký luyện đề & các lỗi cần nhớ
```

## Cách dùng đồng bộ giữa Máy nhà & Điện thoại

### Cách 1: Dùng qua GitHub + Antigravity Web (tắt máy ở nhà vẫn dùng được)
1. Tạo 1 repository **Private** trên GitHub (ví dụ `ontap-csdl-nc`).
2. Đẩy thư mục này lên GitHub:
   ```powershell
   cd C:\Users\Lenovo\Desktop\ONTAP
   git remote add origin https://github.com/<username>/ontap-csdl-nc.git
   git push -u origin main
   ```
3. Mở **Antigravity Web** trên điện thoại → chọn repo `ontap-csdl-nc`. AI sẽ tự đọc `AGENTS.md` và toàn bộ thư mục `notes/` để giữ nguyên 100% kiến thức đã ôn.
4. Khi về nhà: chạy `git pull` để cập nhật ghi chú mới từ điện thoại (hoặc `git push` sau khi luyện ở nhà).

### Cách 2: Điều khiển thẳng máy ở nhà (giữ 100% lịch sử chat Local)
- Cài **Chrome Remote Desktop** (hoặc RustDesk/AnyDesk) trên máy Windows ở nhà và điện thoại.
- Để máy ở nhà bật → mở từ điện thoại để thao tác trực tiếp trên cửa sổ Antigravity Local.
