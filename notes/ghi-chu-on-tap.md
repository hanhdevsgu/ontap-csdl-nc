# Nhật Ký Ôn Tập & Ghi Chú Cá Nhân (CSDL Nâng Cao)

> AI sẽ tự động cập nhật file này sau mỗi buổi luyện tập để dù bạn chuyển từ **máy nhà** sang **điện thoại (Antigravity Web)**, ngữ cảnh vẫn được giữ nguyên 100%.

## Trạng thái hiện tại
- [x] Đọc & phân tích toàn bộ slide `C1.pdf` – `C6.pdf`
- [x] Giải chi tiết đề `03. Đê Ôn Tập -CSDL NC.pdf` (Câu I → Câu IV)
- [ ] Luyện thêm bài tập EER & chuyển đổi sang quan hệ
- [ ] Luyện thêm bài tập Tìm khóa, Phủ tối tiểu, Chase & Chuẩn hóa (từ cuối `C6.pdf`)
- [ ] Luyện thêm bài tập SQL Server (Transaction, Stored Procedure, Window Functions)

## Các lỗi / điểm hay nhầm cần nhớ
- **SQL `LEFT JOIN`:** Điều kiện lọc bảng bên phải (như `YEAR(hd.NgayHD) = 2025`) phải để trong `ON`, nếu để ở `WHERE` sẽ biến thành `INNER JOIN` và làm mất khách hàng chưa mua hàng.
- **Thuật toán Chase:** Nếu bảng dừng lại mà không có dòng nào toàn $a_i$, phép phân rã **mất thông tin**.
- **Tính phủ tối tiểu:** Nhớ kiểm tra lại xem thuộc tính dư thừa ở vế trái có bỏ được không *trước* hoặc *sau* khi tách vế phải, và kiểm tra PTH dư thừa ở bước cuối bằng bao đóng trên tập *không chứa PTH đang xét*.
