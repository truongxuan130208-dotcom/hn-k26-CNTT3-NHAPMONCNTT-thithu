# BÀI LÀM –(CHỦ ĐỀ QUẢN LÝ MODEL AI)

- **Mã đề:pham xuan truong**
- **Họ tên:**
- **Lớp:cntt3**
- **Link repository:**
- **Hệ điều hành (Windows/macOS):windows**

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
pwd
ls -Force
mv .\tai_lieu_ban_giao.txt .\docs\
 mkdir backup
  cp .\data\chi_phi_model_thang_11.xlsx .\backup\
   rm .\model_cache_01.tmp
 cd .\logs\
 ls
 cd..
 

```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
 Directory:                                                              
    C:\Users\tTRUONG\Downloads\MiniPrjoect\starter-kit\quan-ly-model-ai     
                                                                            
                                                                            
Mode                 LastWriteTime         Length Name                      
----                 -------------         ------ ----                      
d-----        11/10/2026   1:49 PM                backup                    
d-----        11/10/2026   1:47 PM                data                      
d-----        11/10/2026   1:49 PM                docs                      
d-----        11/10/2026   1:46 PM                evidence                  
d-----        11/10/2026   2:02 PM                logs                      
d-----        11/10/2026   1:41 PM                web                       
-a----        11/10/2026   1:41 PM             96 .env                      
-a----        11/10/2026   2:02 PM            378 tong_hop.ps1              
                                                                            
                                                                            
    Directory: C:\Users\tTRUONG\Downloads\MiniPrjoect\starter-kit\quan-ly-m 
    odel-ai\backup                                                          
                                                                            
                                                                            
Mode                 LastWriteTime         Length Name                      
----                 -------------         ------ ----                      
-a----        11/10/2026   1:41 PM           5815 chi_phi_model_thang_11.xl 
                                                  sx                        
                                                                            
                                                                            
    Directory: C:\Users\tTRUONG\Downloads\MiniPrjoect\starter-kit\quan-ly-m 
    odel-ai\data                                                            
                                                                            
                                                                            
Mode                 LastWriteTime         Length Name                      
----                 -------------         ------ ----                      
-a----        11/10/2026   1:41 PM           5815 chi_phi_model_thang_11.xl 
                                                  sx                        
                                                                            
                                                                            
    Directory: C:\Users\tTRUONG\Downloads\MiniPrjoect\starter-kit\quan-ly-m 
    odel-ai\docs                                                            
                                                                            
                                                                            
Mode                 LastWriteTime         Length Name                      
----                 -------------         ------ ----                      
-a----        11/10/2026   1:41 PM            204 tai_lieu_ban_giao.txt     
                                                                            
                                                                            
    Directory: C:\Users\tTRUONG\Downloads\MiniPrjoect\starter-kit\quan-ly-m 
    odel-ai\logs                                                            
                                                                            
                                                                            
Mode                 LastWriteTime         Length Name                      
----                 -------------         ------ ----                      
-a----        11/10/2026   1:41 PM           1234 inference.log             
-a----        11/10/2026   1:56 PM            846 loi_model.txt             
-a----        11/10/2026   2:02 PM            878 tong_hop.txt              
                                                                            
                                                                            
    Directory:                                                              
    C:\Users\tTRUONG\Downloads\MiniPrjoect\starter-kit\quan-ly-model-ai\web 
                                                                            
                                                                            
Mode                 LastWriteTime         Length Name                      
----                 -------------         ------ ----                      
d-----        11/10/2026   1:41 PM                images                    
-a----        11/10/2026   1:41 PM            644 app.js                    
-a----        11/10/2026   1:41 PM            567 index.html                
-a----        11/10/2026   1:41 PM            460 style.css                 
                                                                            
                                                                            
    Directory: C:\Users\tTRUONG\Downloads\MiniPrjoect\starter-kit\quan-ly-m 
    odel-ai\web\images                                                      
                                                                            
                                                                            
Mode                 LastWriteTime         Length Name                      
----                 -------------         ------ ----                      
-a----        11/10/2026   1:41 PM            339 logo-ai-hub.png           ```

## 4.3. Lọc log vận hành Model AI

### a) Lệnh lọc các dòng ERROR

```shell
 gc .\logs\inference.log |Select-String "ERROR" > .\logs\loi_model.txt
```

### 2 dòng đầu tiên trong logs/loi_model.txt

```text
(Dán kết quả vào đây – xoá dòng này)

```

### b) Lệnh đếm số dòng WARNING và kết quả

```shell
(gc .\logs\inference.log |Select-String "WARNING").COUNT```

```text
5
```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
tong_hop.ps1
### Nội dung file logs/tong_hop.txt

```text
Dang tao bao cao...                                                                                                                                         
Hoan thanh!    
```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] README.md: Heading 1, hình ảnh (`![Alt](path)`), mô tả có **in đậm**, _in nghiêng_ và `inline code`, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | -------------------------- | --------------------------- | -------------- |
| 1   |              network              |        lỗi không hiển thị ảnh                     |  logo-ai-hub.png     logo-ai-hub.png         |
| 2   |                 console           |          lỗi không hiển thị bảng                   |    vào app.js dòng cuối đổi thành hienThiBangModelAI();            |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:** Tôi là sinh viên năm nhất chưa fix lỗi hiển thị dữ liệu của web bao giờ
- **Expected:** Bây giờ trang web xem phim của tôi muốn có đủ dữ liệu ở bảng hiển thị giao diện 
- **Actual:** Dữ liệu trên trang web không có gì và tôi vào tab console thấy thông báo lỗi app.js:18 Uncaught ReferenceError: hienThiBangGia is not
- **Log:** app.js:18 Uncaught ReferenceError: hienThiBangGia is not

### Câu tìm kiếm Google

```text
site:stackoverflow.com "Uncaught ReferenceError"

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/chi_phi_model_thang_11.xlsx`, không cần ghi vào đây.
