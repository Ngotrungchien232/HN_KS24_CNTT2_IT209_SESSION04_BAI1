# Báo cáo Bài 1: Khởi tạo Local Repository và Cấu hình Danh tính

## Thông tin học viên
- **Họ tên:** Nguyen Van A
- **Email:** nguyenvana@student.rikkei.edu.vn
- **Ngày thực hiện:** 2026-10-03

---

## Mục tiêu bài tập

1. Khởi tạo thành công một Git repository trống tại thư mục làm việc cục bộ.
2. Thiết lập thông tin danh tính tác giả (tên và email) ở cấp độ **local**.
3. Tạo tệp tin mới, đưa vào Staging Area và thực hiện commit đầu tiên.
4. Đọc và phân tích trạng thái thư mục làm việc và lịch sử commit.

---

## Các lệnh đã thực hiện

### Bước 1: Khởi tạo Git Repository

```bash
git init
```

**Kết quả:**
```
Initialized empty Git repository in D:/RIKKEI/HOC_KI_4/.../SESSION04_BAI1/.git/
```

---

### Bước 2: Cấu hình danh tính cục bộ (--local)

```bash
git config --local user.name "Nguyen Van A"
git config --local user.email "nguyenvana@student.rikkei.edu.vn"
```

> **Lưu ý:** Sử dụng tùy chọn `--local` để cấu hình chỉ áp dụng cho repository này, không ảnh hưởng đến cấu hình toàn cục của máy tính.

---

### Bước 3: Tạo tệp tin mới

```bash
# Tạo file main.py với nội dung khởi tạo dự án
```

Nội dung file `main.py`:
```python
# main.py - Khởi tạo dự án phần mềm mới
def main():
    print("Chào mừng đến với dự án phần mềm!")
    print("Repository đã được khởi tạo thành công với Git.")

if __name__ == "__main__":
    main()
```

---

### Bước 4: Đưa file vào Staging Area (git add)

```bash
git add main.py
```

**Kiểm tra trạng thái:**
```bash
git status
```

**Kết quả:**
```
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   main.py
```

---

### Bước 5: Thực hiện Commit đầu tiên

```bash
git commit -m "feat: Khoi tao du an va them file main.py"
```

**Kết quả:**
```
[master (root-commit) f2649c2] feat: Khoi tao du an va them file main.py
 1 file changed, 10 insertions(+)
 create mode 100644 main.py
```

---

## Kết quả kiểm tra

### Kiểm tra tên tác giả cục bộ

```bash
git config --local user.name
```

**Kết quả:**
```
Nguyen Van A
```

---

### Kiểm tra email cục bộ

```bash
git config --local user.email
```

**Kết quả:**
```
nguyenvana@student.rikkei.edu.vn
```

---

### Xem lịch sử commit

```bash
git log --oneline
```

**Kết quả:**
```
f2649c2 feat: Khoi tao du an va them file main.py
```

---

### Xem toàn bộ cấu hình cục bộ

```bash
git config --local --list
```

**Kết quả:**
```
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true
user.name=Nguyen Van A
user.email=nguyenvana@student.rikkei.edu.vn
```

---

## Tổng kết

| Yêu cầu | Trạng thái |
|---------|-----------|
| Khởi tạo Git repository (`git init`) | ✅ Hoàn thành |
| Cấu hình `user.name` với `--local` | ✅ Hoàn thành |
| Cấu hình `user.email` với `--local` | ✅ Hoàn thành |
| Tạo file mới (`main.py`) | ✅ Hoàn thành |
| Đưa file vào Staging Area (`git add`) | ✅ Hoàn thành |
| Thực hiện commit đầu tiên (`git commit`) | ✅ Hoàn thành |
| Kiểm tra lịch sử commit (`git log --oneline`) | ✅ Hoàn thành |

> Tất cả các yêu cầu của bài tập đã được hoàn thành thành công. Repository cục bộ đã được khởi tạo, danh tính tác giả đã được cấu hình ở cấp độ local (không ảnh hưởng global), và commit đầu tiên đã được ghi lại trong lịch sử Git.
