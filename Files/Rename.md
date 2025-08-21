# Cách đổi tên file trong repo
## Cách 1: Đổi tên file trực tiếp trên GitHub (Nhanh nhất) - ƯU TIÊN
Nếu file đã nằm trong repo và bạn chỉ muốn đổi tên, thì làm như sau:
- **Bước 1**. Vào repo chứa file
Truy cập GitHub → Vào repository → Tìm đến file cần đổi tên.
- **Bước 2**. Mở chế độ chỉnh sửa
Nhấn vào tên file.
Ở góc phải phía trên, nhấn cây bút Edit (🖊).
- **Bước 3**. Đổi tên file
Trong ô Name, đổi tên file thành tên mới.
Nếu muốn đổi cả thư mục chứa file, bạn có thể đổi đường dẫn luôn, ví dụ:
Cpp/Bai2_Cuphap.cpp  →  Cpp/Output.cpp
- **Bước 4**. Commit thay đổi
Kéo xuống cuối trang.
Ở mục Commit changes:
Viết mô tả ngắn, ví dụ: Rename Bai2_Cuphap.cpp to Output.cpp
Chọn Commit directly to the main branch.
Nhấn Commit changes.
✅ Xong! File sẽ được đổi tên ngay trong repo.

---
## Cách 2: Đổi tên file bằng Git trên máy tính (Khuyến nghị nếu bạn hay làm việc với VSCode)
- **Bước 1**. Clone repo về máy (nếu chưa có)
```bash
git clone https://github.com/<username>/<repo-name>.git
cd <repo-name>
```
- **Bước 2**. Đổi tên file
```bash
git mv duong_dan_cu duong_dan_moi
```
Ví dụ:
git mv Cpp/Bai2_Cuphap.cpp Cpp/Output.cpp
- **Bước 3**. Commit và push
```bash
git commit -m "Rename Bai2_Cuphap.cpp to Output.cpp"
git push origin main
```
Nếu repo của bạn dùng branch master thì thay main bằng master.

---
## Cách 3: Đổi tên file bằng VSCode (Dễ thao tác trực quan)
Mở repo bằng VSCode.
Ở Explorer → Chuột phải vào file → Chọn Rename → Đổi tên file.
Lưu thay đổi.
Mở terminal trong VSCode và thực hiện:
```bash
git add .
git commit -m "Rename file"
git push origin main
```
Lưu ý quan trọng
Nên dùng git mv thay vì xóa file cũ + tạo file mới, vì git sẽ giữ lịch sử commit.
Nếu đổi tên nhiều file, có thể dùng:
```bash
git mv file1.cpp new_file1.cpp
git mv file2.cpp new_file2.cpp
```
