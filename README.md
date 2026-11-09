# Bài 6 : Ứng dụng AI trong khắc phục lỗi Git Permission Denied
## 1. Sử dụng công thức Prompt 3 thành phần
Công thức gồm:
1. Role (Vai trò): Yêu cầu AI đóng vai chuyên gia hỗ trợ kỹ thuật.
2. Context (Bối cảnh): Cung cấp lỗi và tình huống đang gặp.
3. Task (Nhiệm vụ): Yêu cầu AI giải thích và hướng dẫn xử lý.

Prompt hoàn chỉnh:

**ROLE:** Bạn là chuyên gia hỗ trợ kỹ thuật Git và GitHub, có khả năng giải thích vấn đề cho người mới học lập trình.

**CONTEXT:** Tôi đang sử dụng Windows 11 và muốn đẩy mã nguồn lên GitHub. Khi thực hiện lệnh Git, Terminal báo lỗi:

`error: open(".git/FETCH_HEAD"): Permission denied`

Tôi đã thử chạy lại lệnh nhưng vẫn không thành công.

**TASK:**
1. Giải thích lỗi trên bằng ngôn ngữ bình dân, dễ hiểu cho người mới học.
2. Cho biết những nguyên nhân phổ biến gây ra lỗi này.
3. Hướng dẫn từng bước kiểm tra và khắc phục trên Windows 11 bằng PowerShell.
4. Giải thích cách sử dụng Run as Administrator nếu thực sự cần thiết.
5. Đưa ra cách kiểm tra xem lỗi đã được khắc phục chưa.
6. Cảnh báo những thao tác có thể ảnh hưởng đến dữ liệu hoặc quyền truy cập của thư mục dự án.

Không đưa ra lệnh nguy hiểm hoặc yêu cầu xóa thư mục `.git` để sửa lỗi.
## 2. Thực hành xử lý lỗi bằng Run as Administrator
### Bước 1: Mở PowerShell bằng quyền Administrator
<img width="1370" height="768" alt="image" src="https://github.com/user-attachments/assets/befa2f29-1132-4496-b7b8-2c5e9dcecc1f" />

1. Nhấn phím Windows.
2. Gõ `PowerShell`.
3. Nhấn chuột phải vào Windows PowerShell.
4. Chọn `Run as Administrator`.
5. Chọn Yes nếu Windows hỏi xác nhận.
### Bước 2: Di chuyển đến thư mục dự án
Ví dụ dự án nằm ở ổ D:
```Powershell
cd "D:\TenDuAn"
```
Kiểm tra thư mục Git:
```Powershell
git status
```
Nếu lệnh hoạt động, kiểm tra tiếp:
```Powershell
git fetch
```
Nếu không còn lỗi quyền truy cập, bạn có thể tiếp tục quy trình Git bình thường:
```Powershell
git add .
git commit -m "Update project"
git push
```
### Bước 3: Chụp ảnh minh họa để nộp bài
