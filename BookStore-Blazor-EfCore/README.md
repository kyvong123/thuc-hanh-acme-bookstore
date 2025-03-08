# Th?c h�nh x�y d?ng web qu?n l� hi?u s�ch

## Y�u c?u

``` bash
.NET 8.0
c? s? d? li?u SQL
```

# C�i ??t, x�y d?ng c? s? d? li?u v� ch?y ?ng d?ng:


## C�i ??t Abp Cli:
``` bash
C�i ??t Abp Cli b?ng c�u l?nh cmd:
$ dotnet tool install -g Volo.Abp.Studio.Cli

C�i ??t c�c g�i npm c?n thi?t cho d? �n khi t?o ?ng d?ng:
$ abp install-libs
L?nh abp bundle cung c?p h? tr? ?�ng g�i v� thu nh? cho c�c t�i nguy�n cho d? �n Blazor.
$ abp bundle
```

## X�y d?ng c? s? d? li?u
``` bash
K?t n?i c? s? d? li?u b?ng sql server management studio v� t?o database, ??t t�n l� BookStore

V�o t?p tin appsettings.json tr�n th? m?c src/Acme.BookStore.Blazor v� src/Acme.BookStore.DbMigrator ch?nh s?a l?i c�c connectionstring v?i server name, user, password ph� h?p.

X�a c�c file b�n trong th? m?c src/Acme.BookStore.EntityFrameworkCore/Migrations

V�o command line truy c?p th? m?c src/Acme.BookStore.EntityFrameworkCore

G� c�c l?nh sau ?? th�m c�c migration class v�o project:
$ dotnet ef migrations add Created_Book_Entity
$ dotnet ef migrations add Added_Authors
$ dotnet ef migrations add Added_AuthorId_To_Book
G� l?nh ?? c?p nh?t c? s? d? li?u tr�n SQL:
$ dotnet ef database update

## Ch?y ?ng d?ng
Ch?y ?ng d?ng v?i c?u h�nh C#, v?i project ch�nh l� Acme.BookStore.Blazor

web qu?n l� hi?u s�ch: https://localhost:{port}

Truy c?p web v?i t�i kho?n superadmin:
Username: admin
Password: 1q2w3E*

C� th? ??ng k�, t?o th�m t�i kho?n r?i s? d?ng t�i kho?n superadmin g�n quy?n v� thao t�c v?i web.

web danh s�ch c�c api: https://localhost:{port}/swagger/index.html


```