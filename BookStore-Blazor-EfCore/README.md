# Thực hành xây dựng web quản lý hiệu sách

## Yêu cầu

``` bash
.NET 8.0
cơ sở dữ liệu SQL
```

# Cài đặt, xây dưng cơ sở dữ liệu và chạy ứng dụng:


## Cài đặt Abp Cli:
``` bash
Cài đặt Abp Cli bằng câu lệnh cmd:
$ dotnet tool install -g Volo.Abp.Studio.Cli

Cài đặt các gói npm cần thiết cho dự án khi tạo ứng dụng:
$ abp install-libs
Lệnh abp bundle cung cấp hỗ trợ đóng gói và thu nhỏ cho các tài nguyên cho dự án Blazor.
$ abp bundle
```

## Xây dựng cơ sở dữ liệu
``` bash
Kết nối cơ sở dữ liệu bằng sql server management studio và tạo database, đặt tên là BookStore

Vào tập tin appsettings.json trên thư mục src/Acme.BookStore.Blazor và src/Acme.BookStore.DbMigrator chỉnh sửa lại các connectionstring với server name, user, password phù hợp.

Xóa các file bên trong thư mục src/Acme.BookStore.EntityFrameworkCore/Migrations

Vào command line truy cập thư mục src/Acme.BookStore.EntityFrameworkCore

Gõ các lệnh sau để thêm các migration class vào project:
$ dotnet ef migrations add Created_Book_Entity
$ dotnet ef migrations add Added_Authors
$ dotnet ef migrations add Added_AuthorId_To_Book

Gõ lệnh để cập nhật cơ sở dữ liệu trên SQL:
$ dotnet ef database update
```

## Chạy ứng dụng
``` bash
Chạy ứng dụng với cấu hình C#, với project chính là Acme.BookStore.Blazor

Trang web quản lý hiệu sách: https://localhost:{port}

Truy cập web với tài khoản superadmin:
Username: admin
Password: 1q2w3E*
Có thể đăng ký, tạo thêm tài khoản rồi sử dụng tài khoản superadmin gán quyền và thao tác với web.

Trang web hiển thị danh sách các api: https://localhost:{port}/swagger/index.html


```