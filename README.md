# Hướng dẫn cài đặt và chạy dự án

Dự án này xây dựng một trang web bán quần áo sử dụng [Laravel](https://laravel.com). Dưới đây là các bước cài đặt môi trường và khởi chạy ứng dụng trên máy tính của bạn.

## 1. Cài đặt PHP

Laravel yêu cầu PHP phiên bản 8.0 trở lên. Bạn có thể cài đặt PHP thông qua trình quản lý gói của hệ điều hành. Ví dụ trên Ubuntu:

```bash
sudo apt update
sudo apt install php php-cli php-mbstring php-xml php-bcmath php-json php-zip
```

## 2. Cài đặt Composer

Composer là công cụ quản lý thư viện PHP. Tải và cài đặt Composer:

```bash
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php composer-setup.php --install-dir=/usr/local/bin --filename=composer
php -r "unlink('composer-setup.php');"
```

Sau khi cài đặt xong, kiểm tra bằng lệnh:

```bash
composer --version
```

## 3. Cài đặt Laravel

Bạn có thể cài Laravel thông qua Composer:

```bash
composer global require laravel/installer
```

Đảm bảo `~/.composer/vendor/bin` (hoặc đường dẫn tương tự trên hệ điều hành của bạn) đã được thêm vào biến `PATH` để có thể chạy lệnh `laravel` trên terminal.

## 4. Sao chép (clone) kho chứa mã nguồn

Mở terminal và chạy:

```bash
git clone <URL-repo-cua-ban>
cd TenThuMucRepo
```

Trong đó `<URL-repo-cua-ban>` là đường dẫn Git của kho chứa dự án này và `TenThuMucRepo` là thư mục chứa mã nguồn sau khi sao chép.

## 5. Cài đặt các gói PHP cần thiết

Tại thư mục dự án vừa sao chép, chạy:

```bash
composer install
```

Lệnh trên sẽ tải toàn bộ thư viện mà dự án yêu cầu.

## 6. Cấu hình biến môi trường

Laravel sử dụng file `.env` để lưu thông tin cấu hình. Bạn thực hiện như sau:

```bash
cp .env.example .env
php artisan key:generate
```

Sau đó mở file `.env` và cập nhật các thông số kết nối cơ sở dữ liệu hoặc các thiết lập khác (ví dụ `DB_HOST`, `DB_PORT`, `DB_DATABASE`, `DB_USERNAME`, `DB_PASSWORD`).

## 7. Khởi chạy ứng dụng

Để chạy ứng dụng ở môi trường cục bộ, sử dụng lệnh:

```bash
php artisan serve
```

Mặc định ứng dụng sẽ chạy tại địa chỉ `http://localhost:8000`. Truy cập địa chỉ này trên trình duyệt để xem trang web.

Nếu dự án sử dụng thêm các tài nguyên phía client (JavaScript/CSS thông qua Laravel Mix hay Vite), hãy cài Node.js và chạy thêm:

```bash
npm install
npm run dev
```

## 8. Thông tin thêm

Bạn có thể thực hiện migrate cơ sở dữ liệu bằng lệnh:

```bash
php artisan migrate
```

Trong trường hợp cần dữ liệu mẫu, hãy thêm seeder hoặc các bước liên quan khác tùy vào dự án.

Chúc bạn cài đặt và trải nghiệm dự án thành công!
