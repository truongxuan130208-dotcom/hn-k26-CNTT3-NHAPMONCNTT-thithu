# BÀI LÀM – THI THỬ HACKATHON 02 (GAMEZONE)

- **Họ tên:PHAM XUAN TRUONG** 
- **Lớp:CNTT3** 
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):WINDOWS** 

## 4.2. Thao tác CLI

### Các lệnh đã chạy

```shell
pwd
ls -Force
mv .\cap_nhat.txt docs
mv .\logo_gamezone.png media
cp .\media\ .\backup\
rm .\temp_207.tmp
cd logs
ls
cd ..
 Get-ChildItem -Recurse -Force
Get-Content logs/game.log | Select-String "ERROR" > logs/daily_report.txt
Get-Content logs/daily_report.txt
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
.\auto_report.ps1
Get-Content logs/auto_report.txt
(Get-Content logs/game.log | Select-String "ERROR").Count
"=== TONG HOP LOG ===" > logs/tong_hop.txt
Get-Content logs/game.log | Select-String "WARNING" >> logs/tong_hop.txt
 Get-Content logs/tong_hop.txt
```

### Kết quả liệt kê toàn bộ dự án

```text
Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

PS D:\de-on-tap-game\starter-kit\gamezone-website> pwd

Path
----
D:\de-on-tap-game\starter-kit\gamezone-website


PS D:\de-on-tap-game\starter-kit\gamezone-website> ls -Force


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/26/2026   1:15 PM                backup
d-----        10/26/2026   1:22 PM                data
d-----        10/26/2026   1:15 PM                docs
d-----        10/26/2026   1:23 PM                logs
d-----        10/26/2026   1:15 PM                media
-a----        10/26/2026   1:11 PM             70 .env
-a----        10/26/2026   1:11 PM           1437 bai_lam.md
-a----        10/26/2026   1:11 PM             61 cap_nhat.txt
-a----        10/26/2026   1:11 PM           8542 logo_gamezone.png
-a----        10/26/2026   1:11 PM             22 temp_207.tmp


PS D:\de-on-tap-game\starter-kit\gamezone-website> mv .\cap_nhat.txt docs
PS D:\de-on-tap-game\starter-kit\gamezone-website> mv .\logo_gamezone.png media
PS D:\de-on-tap-game\starter-kit\gamezone-website> cp .\media\ .\backup\
PS D:\de-on-tap-game\starter-kit\gamezone-website> rm .\temp_207.tmp
PS D:\de-on-tap-game\starter-kit\gamezone-website> cd logs
PS D:\de-on-tap-game\starter-kit\gamezone-website\logs> ls


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:11 PM            986 game.log


PS D:\de-on-tap-game\starter-kit\gamezone-website\logs> cd ..
PS D:\de-on-tap-game\starter-kit\gamezone-website> Get-ChildItem -Recurse -Force


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/26/2026   1:15 PM                backup
d-----        10/26/2026   1:22 PM                data
d-----        10/26/2026   1:25 PM                docs
d-----        10/26/2026   1:23 PM                logs
d-----        10/26/2026   1:26 PM                media
-a----        10/26/2026   1:11 PM             70 .env
-a----        10/26/2026   1:11 PM           1437 bai_lam.md


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/26/2026   1:26 PM                media


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:11 PM           5814 giao_dich_thang_11.xlsx


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:11 PM             61 cap_nhat.txt


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:11 PM            986 game.log


    Directory: D:\de-on-tap-game\starter-kit\gamezone-website\media


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:11 PM           8542 logo_gamezone.png


PS D:\de-on-tap-game\starter-kit\gamezone-website> Get-Content logs/shop.log | Select-String "ERROR" > logs/daily_report.txt
Get-Content : Cannot find path 'D:\de-on-tap-game\starter-kit\gamezone-website\logs\shop.log' because it does not
exist.
At line:1 char:1
+ Get-Content logs/shop.log | Select-String "ERROR" > logs/daily_report ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (D:\de-on-tap-ga...e\logs\shop.log:String) [Get-Content], ItemNotFoundEx
   ception
    + FullyQualifiedErrorId : PathNotFound,Microsoft.PowerShell.Commands.GetContentCommand

PS D:\de-on-tap-game\starter-kit\gamezone-website> Get-Content logs/game.log | Select-String "ERROR" > logs/daily_report.txt
PS D:\de-on-tap-game\starter-kit\gamezone-website> Get-Content logs/daily_report.txt

2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:12:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:39:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:42:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:51:15 [ERROR] Loi luu tien trinh choi


PS D:\de-on-tap-game\starter-kit\gamezone-website> Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
PS D:\de-on-tap-game\starter-kit\gamezone-website> .\auto_report.ps1
Dang loc log...
Hoan thanh!
PS D:\de-on-tap-game\starter-kit\gamezone-website> Get-Content logs/auto_report.txt
=== BAO CAO LOI ===

2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:12:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:39:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:42:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:51:15 [ERROR] Loi luu tien trinh choi


PS D:\de-on-tap-game\starter-kit\gamezone-website> (Get-Content logs/shop.log | Select-String "ERROR").Count
Get-Content : Cannot find path 'D:\de-on-tap-game\starter-kit\gamezone-website\logs\shop.log' because it does not
exist.
At line:1 char:2
+ (Get-Content logs/shop.log | Select-String "ERROR").Count
+  ~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (D:\de-on-tap-ga...e\logs\shop.log:String) [Get-Content], ItemNotFoundEx
   ception
    + FullyQualifiedErrorId : PathNotFound,Microsoft.PowerShell.Commands.GetContentCommand

0
PS D:\de-on-tap-game\starter-kit\gamezone-website> (Get-Content logs/game.log | Select-String "ERROR").Count
6
PS D:\de-on-tap-game\starter-kit\gamezone-website> "=== TONG HOP LOG ===" > logs/tong_hop.txt
PS D:\de-on-tap-game\starter-kit\gamezone-website> Get-Content logs/game.log | Select-String "WARNING" >> logs/tong_hop.txt
PS D:\de-on-tap-game\starter-kit\gamezone-website>  Get-Content logs/tong_hop.txt
=== TONG HOP LOG ===

2025-11-05 08:54:15 [WARNING] May chu qua tai CPU 90%

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
 gc .\logs\game.log | Select-String "ERROR"
```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
```

## 4.4. README.md

> Chấm trực tiếp trên `README.md` ở gốc dự án.

- [ ] Heading 1
- [ ] Mô tả in đậm + in nghiêng
- [ ] Bảng `Thư mục | Nội dung` (≥3 dòng)
- [ ] Code block lệnh liệt kê
- [ ] Task list (≥2 việc, ≥1 đã xong)
- [ ] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report

### Lệnh chạy

```shell
#.\auto_report.ps1

```

### Nội dung file logs/auto_report.txt

```text
=== BAO CAO LOI ===

2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:12:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:39:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:42:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:51:15 [ERROR] Loi luu tien trinh choi
```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
#  (Get-Content logs/game.log | Select-String "ERROR").Count
```

### Kết quả đếm
6
```text
(Dán kết quả vào đây)

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
pwd
ls -Force
mv .\cap_nhat.txt docs
mv .\logo_gamezone.png media
cp .\media\ .\backup\
rm .\temp_207.tmp
cd logs
ls
cd ..
 Get-ChildItem -Recurse -Force
Get-Content logs/game.log | Select-String "ERROR" > logs/daily_report.txt
Get-Content logs/daily_report.txt
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
.\auto_report.ps1
Get-Content logs/auto_report.txt
(Get-Content logs/game.log | Select-String "ERROR").Count
"=== TONG HOP LOG ===" > logs/tong_hop.txt
Get-Content logs/game.log | Select-String "WARNING" >> logs/tong_hop.txt
 Get-Content logs/tong_hop.txt
```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG ===

2025-11-05 08:54:15 [WARNING] May chu qua tai CPU 90%

```

## 4.8. Excel

> Chấm trực tiếp trên file `data/giao_dich_thang_11.xlsx`.
