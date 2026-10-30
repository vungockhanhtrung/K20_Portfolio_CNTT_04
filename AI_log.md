# Báo cáo lỗi

Ngày kiểm tra: 2026-10-30

## Lỗi đã xác nhận

1. **Liên kết email dùng sai địa chỉ** — `index.html:337`  
	Nội dung hiển thị là `trung@gmail.com`, nhưng liên kết dùng `mailto:trung@gmail.com.com`. Khi nhấn, ứng dụng email sẽ điền địa chỉ nhận không khớp với địa chỉ được hiển thị.  
	**Đề xuất:** sửa `href` thành `mailto:trung@gmail.com` hoặc cập nhật nội dung hiển thị để khớp với địa chỉ nhận đúng.

2. **Hiệu ứng bỏ qua điều hướng kéo dài bất thường** — `style.css:37`  
	`.skip-link` đặt `transition: transform 180s ease`, khiến hiệu ứng hiện liên kết khi nhận focus có thể kéo dài tới 180 giây. Các hiệu ứng tương tự trong stylesheet dùng `180ms`.  
	**Đề xuất:** đổi `180s` thành `180ms`.

## Kết quả kiểm tra

- Chẩn đoán của VS Code: không phát hiện lỗi cú pháp trong `index.html`, `ket-qua.html` hoặc `style.css`.
- Báo cáo này ghi nhận lỗi chức năng/giao diện thấy được khi rà mã; chưa chạy kiểm thử trình duyệt.
