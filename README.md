# Portfolio cá nhân – Kim Nguyen

Trang portfolio giới thiệu **Nguyen Thi Kim Nguyen**, chuyên gia tư vấn kỹ thuật SAP, tập trung vào ABAP, chuyển đổi S/4HANA và tích hợp hệ thống.

## Tệp chính

- `index.htlm` — trang web portfolio, gồm cấu trúc HTML, giao diện CSS và mã JavaScript trong cùng một tệp. Tên tệp hiện tại là `index.htlm` (phần mở rộng bị đảo chữ); nếu muốn máy chủ web tự nhận đây là trang mặc định, nên đổi tên thành `index.html`.

## Nội dung trang

Trang được thiết kế theo dạng một trang cuộn, có thanh điều hướng đến các mục:

- **Home:** giới thiệu, chuyên môn và một số số liệu nổi bật.
- **About:** thông tin tổng quan và địa điểm làm việc.
- **Core Skills:** nhóm kỹ năng SAP, phát triển, tích hợp và phương pháp triển khai.
- **Experience:** kinh nghiệm làm việc tại Deloitte Consulting SEA và FPT Software.
- **Featured Projects:** các dự án tiêu biểu về chuyển đổi, tích hợp và triển khai SAP.
- **Certifications & Education:** chứng chỉ SAP, học vấn và đào tạo.
- **Contact:** thông tin liên hệ và biểu mẫu chuẩn bị email.

## Chức năng

- Điều hướng đến từng phần bằng liên kết trên thanh menu; trên màn hình nhỏ có nút mở/đóng menu.
- Lọc dự án theo **All**, **S/4HANA Migration**, **Integration** hoặc **AMS & Rollout** mà không tải lại trang.
- Hiển thị dần một số nội dung khi cuộn trang; hiệu ứng được giảm hoặc tắt nếu thiết bị bật tùy chọn giảm chuyển động.
- Nút **Download CV** tạo và tải xuống CV dạng văn bản `.txt` ngay trên trình duyệt, không cần máy chủ.
- Biểu mẫu liên hệ kiểm tra dữ liệu nhập rồi mở ứng dụng email mặc định với nội dung đã điền sẵn. Biểu mẫu **không gửi dữ liệu đến máy chủ**; người dùng cần tự gửi email.
- Tự động cập nhật năm hiện tại ở chân trang.
- Bố cục thích ứng với màn hình điện thoại, máy tính bảng và máy tính.

## Cách sử dụng

### Xem trên máy tính

1. Tải hoặc clone repository về máy.
2. Mở `index.htlm` bằng trình duyệt hiện đại.
3. Nếu trình duyệt không mở tệp trực tiếp theo cách mong muốn, đổi tên thành `index.html` rồi mở lại.

### Chạy máy chủ cục bộ (tùy chọn)

Sau khi đổi tên tệp thành `index.html`, có thể chạy máy chủ tĩnh đơn giản trong thư mục dự án:

```bash
python -m http.server 8000
```

Sau đó mở `http://localhost:8000` trong trình duyệt.

## Công nghệ và yêu cầu

- HTML5, CSS và JavaScript thuần.
- Tailwind CSS được nạp từ CDN; phông chữ Inter và DM Mono được tải từ Google Fonts.
- Không cần cài đặt gói hay chạy backend để xem các chức năng phía trình duyệt.
- Cần kết nối Internet để tải Tailwind CSS và Google Fonts từ các dịch vụ bên ngoài. Nếu không có mạng, trang vẫn có CSS dự phòng nhưng giao diện có thể khác.

## Tùy chỉnh

Có thể sửa nội dung giới thiệu, kinh nghiệm, dự án và thông tin liên hệ trực tiếp trong `index.htlm`. Nội dung CV tải xuống được khai báo riêng trong mảng `cvText` ở cuối tệp, vì vậy hãy cập nhật phần này nếu muốn CV tải về đồng bộ với nội dung trên trang. Để thay đổi địa chỉ nhận email của biểu mẫu, cập nhật địa chỉ trong xử lý `mailto` ở mã JavaScript.
