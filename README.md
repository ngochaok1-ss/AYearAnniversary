# Chương đầu của chúng mình ♡

Landing page kỷ niệm một năm của Quỳnh Chi (Gitchee), từ 02/11/2025 đến 02/11/2026.

Trang dùng HTML, CSS và JavaScript thuần, gồm album 15 ảnh, hai video, bộ đếm ngày kỷ niệm, bộ đếm chuyến đi Huế và phần thư/quà mở từ 00:00 ngày 02/11/2026 theo giờ Việt Nam.

## Chạy trên máy

Không cần cài thư viện hoặc build. Tại thư mục repository:

```sh
python3 -m http.server 8000 --directory dist
```

Sau đó mở http://localhost:8000.

## Deploy lên Netlify

1. Tạo project trên Netlify từ GitHub repository này.
2. Chọn nhánh `main`.
3. Base directory: để trống.
4. Build command: `node scripts/prepare-netlify.mjs`.
5. Publish directory: `dist`.

`netlify.toml` đã khai báo các thiết lập trên. Không cần biến môi trường riêng hay khóa API. Script chuẩn bị chỉ cập nhật URL và ảnh xem trước khi chia sẻ cho đúng địa chỉ Netlify của bản deploy.

## Chỉnh sửa nội dung

- `dist/index.html`: bố cục, lời nhắn, lá thư và món quà.
- `dist/content.js`: danh sách ảnh, chương album, ngày kỷ niệm và giờ khởi hành đi Huế.
- `dist/style.css`: màu sắc, kiểu chữ và bố cục responsive.
- `dist/app.js`: xem ảnh, phát video, đồng hồ và tương tác thư/quà.
- `dist/anniversary.js`: tính ngày giờ và điều kiện mở thư/quà.
- `dist/assets/`: ảnh, ảnh thu nhỏ, ảnh bìa video và video đã tối ưu.

Mốc chuyến đi Huế: `2026-11-22T14:10:00+07:00`.

Khóa thư/quà là tương tác phía trình duyệt, dựa trên thời gian thiết bị; đây không phải cơ chế bảo mật nội dung phía máy chủ.
