# Th?c hành xây d?ng web qu?n lý hi?u sách

## Yêu c?u

``` bash
.NET 8.0
c? s? d? li?u SQL
```

# Cài ??t, xây d?ng c? s? d? li?u và ch?y ?ng d?ng:


## Cài ??t Abp Cli:
``` bash
Cài ??t Abp Cli b?ng câu l?nh cmd:
$ dotnet tool install -g Volo.Abp.Studio.Cli

Cài ??t các gói npm c?n thi?t cho d? án khi t?o ?ng d?ng:
$ abp install-libs
L?nh abp bundle cung c?p h? tr? ?óng gói và thu nh? cho các tài nguyên cho d? án Blazor.
$ abp bundle
```

## Xây d?ng c? s? d? li?u
``` bash
K?t n?i c? s? d? li?u b?ng sql server management studio và t?o database, ??t tên là BookStore

Vào t?p tin appsettings.json trên th? m?c src/Acme.BookStore.Blazor và src/Acme.BookStore.DbMigrator ch?nh s?a l?i các connectionstring v?i server name, user, password phù h?p.

Xóa các file bên trong th? m?c src/Acme.BookStore.EntityFrameworkCore/Migrations

Vào command line truy c?p th? m?c src/Acme.BookStore.EntityFrameworkCore

Gõ các l?nh sau ?? thêm các migration class vào project:
$ dotnet ef migrations add Created_Book_Entity
$ dotnet ef migrations add Added_Authors
$ dotnet ef migrations add Added_AuthorId_To_Book
Gõ l?nh ?? c?p nh?t c? s? d? li?u trên SQL:
$ dotnet ef database update

## Ch?y ?ng d?ng
Ch?y ?ng d?ng v?i c?u hình C#, v?i project chính là Acme.BookStore.Blazor

web qu?n lý hi?u sách: https://localhost:{port}

Truy c?p web v?i tài kho?n superadmin:
Username: admin
Password: 1q2w3E*

Có th? ??ng ký, t?o thêm tài kho?n r?i s? d?ng tài kho?n superadmin gán quy?n và thao tác v?i web.

web danh sách các api: https://localhost:{port}/swagger/index.html


```