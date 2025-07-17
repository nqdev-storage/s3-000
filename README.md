[![s3-000](https://img.shields.io/badge/NQDEV-s3_000-brightgreen.svg)](https://cdn-s3-000.quyit.id.vn)
[![LICENSE](https://img.shields.io/badge/license_scan-passing-brightgreen.svg)](https://cdn-s3-000.quyit.id.vn/LICENSE)
[![CodeQL](https://github.com/nqdev-storage/s3-000/actions/workflows/github-code-scanning/codeql/badge.svg)](https://github.com/nqdev-storage/s3-000/actions/workflows/github-code-scanning/codeql)
[![pages-build-deployment](https://github.com/nqdev-storage/s3-000/actions/workflows/pages/pages-build-deployment/badge.svg?branch=gh-pages)](https://github.com/nqdev-storage/s3-000/actions/workflows/pages/pages-build-deployment)
[![Update Changelog on Release](https://github.com/nqdev-storage/s3-000/actions/workflows/changelog.yml/badge.svg)](https://github.com/nqdev-storage/s3-000/actions/workflows/changelog.yml)

# Simple Storage Service (s3-000)

## Giới thiệu

**s3-000** là một dịch vụ lưu trữ đơn giản (storage service) giống như Amazon S3, nhưng được thiết kế để sử dụng với các ứng dụng nhỏ và trung bình. Nó cung cấp API đơn giản để tải, lấy, và xóa các đối tượng lưu trữ. Dự án này được phát triển bởi nhóm NQDEV và được xây dựng để giúp các nhà phát triển dễ dàng tích hợp và sử dụng dịch vụ lưu trữ trong ứng dụng của họ.

Dự án này là một lựa chọn thay thế nhẹ nhàng và linh hoạt cho các dịch vụ lưu trữ lớn hơn như Amazon S3, giúp bạn dễ dàng quản lý các tệp tin và dữ liệu của mình với chi phí và độ phức tạp thấp hơn.

## Tính năng

- **Lưu trữ đối tượng (Object Storage)**: Lưu trữ và truy xuất tệp tin dễ dàng.
- **API đơn giản**: Các API dễ sử dụng để upload, download và delete đối tượng.
- **Hỗ trợ các tệp tin có kích thước lớn**: Tải lên và lưu trữ các tệp tin dung lượng lớn một cách hiệu quả.
- **Bảo mật**: Tích hợp các cơ chế bảo mật cơ bản để đảm bảo tính toàn vẹn và an toàn của dữ liệu.

## Cài đặt

### 1. Clone Repository
Để bắt đầu sử dụng, bạn có thể clone repository về máy:
```bash
git clone https://github.com/nqdev-storage/s3-000.git
```

### 2. Cài đặt các phụ thuộc
Cài đặt các thư viện phụ thuộc cần thiết thông qua `npm` hoặc `yarn`:
```bash
npm install
```
hoặc
```bash
yarn install
```

### 3. Cấu hình môi trường
Đảm bảo rằng bạn đã cấu hình các biến môi trường cần thiết, ví dụ như thông tin kết nối tới cơ sở dữ liệu, API keys, hoặc các tham số cấu hình khác. Các biến môi trường này có thể được đặt trong file `.env`.

### 4. Chạy ứng dụng
Sau khi cài đặt xong, bạn có thể chạy ứng dụng bằng lệnh:
```bash
npm start
```
hoặc
```bash
yarn start
```
Ứng dụng sẽ được khởi chạy tại `http://localhost:3000` (hoặc port khác tùy vào cấu hình).

## Sử dụng

### Tải lên tệp tin
Để tải một tệp tin lên hệ thống lưu trữ của **s3-000**, bạn có thể sử dụng API sau:
```bash
POST /upload
Content-Type: multipart/form-data
{
  "file": <file_path>
}
```

### Tải xuống tệp tin
Để tải một tệp tin đã lưu trữ xuống, bạn có thể sử dụng API:
```bash
GET /download/<file_id>
```

### Xóa tệp tin
Để xóa tệp tin khỏi hệ thống:
```bash
DELETE /delete/<file_id>
```

### Các API khác
- `GET /files`: Lấy danh sách tất cả các tệp đã lưu trữ.
- `GET /status`: Kiểm tra trạng thái của dịch vụ.

## Cấu trúc dự án
Dưới đây là cấu trúc thư mục của dự án:

```bash
s3-000/
├── src/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── services/
│   └── app.js
├── config/
│   ├── config.js
│   └── env.js
├── public/
├── package.json
└── README.md
```

## Đóng góp
Chúng tôi luôn hoan nghênh sự đóng góp từ cộng đồng. Nếu bạn muốn đóng góp vào dự án, hãy tạo một pull request hoặc mở issue nếu bạn phát hiện lỗi hoặc có đề xuất tính năng mới.

### Các bước đóng góp
1. Fork repository này.
2. Tạo một nhánh mới (`git checkout -b feature-xyz`).
3. Commit thay đổi của bạn (`git commit -am 'Add new feature xyz'`).
4. Push lên nhánh của bạn (`git push origin feature-xyz`).
5. Mở pull request để chúng tôi xem xét.

## Giấy phép
Dự án này sử dụng giấy phép [MIT License](LICENSE).

---

**👉 Đóng góp hoặc liên hệ:**
Hãy mở issue hoặc pull request nếu bạn có đề xuất nâng cấp hoặc phát hiện lỗi.

<p style="text-align: center;"> © 2025 QuyIT Platform. All rights reserved. </p>
