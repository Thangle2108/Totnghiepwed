# Hướng dẫn chạy dự án Laravel

Dự án này sử dụng [Laravel](https://laravel.com) để xây dựng một cửa hàng bán quần áo.

## Cài đặt

1. Cài đặt PHP >= 8 và Composer.
2. Cài đặt Node.js và npm.
3. Chạy `composer install` để cài đặt các thư viện PHP.
4. Chạy `npm install` để cài đặt các gói JavaScript.
5. Sao chép file `.env.example` thành `.env` và cập nhật thông tin kết nối cơ sở dữ liệu.
6. Chạy `php artisan key:generate` để tạo khóa ứng dụng.
7. Thực thi `php artisan migrate` để tạo các bảng dữ liệu.
8. Chạy `php artisan storage:link` để liên kết thư mục lưu trữ hình ảnh.
9. Khởi chạy ứng dụng bằng `php artisan serve` và truy cập địa chỉ hiển thị.

## Nội dung dự án

Thư mục `testlaravel` chứa mã nguồn Laravel mẫu. Bạn có thể phát triển thêm các tính năng bán quần áo và quản lý hình ảnh tại đây.
