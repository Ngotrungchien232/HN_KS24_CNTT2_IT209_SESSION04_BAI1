# Báo cáo Bài 1: Khởi tạo Local Repository và Cấu hình Danh tính

## Thông tin học viên
- **Họ tên:** ngotrungchien
- **Email:** ngotrungchien232@gmail.com
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
git config --local user.name "ngotrungchien"
git config --local user.email "ngotrungchien232@gmail.com"
```

> **Lưu ý:** Sử dụng tùy chọn `--local` để cấu hình chỉ áp dụng cho repository này, không ảnh hưởng đến cấu hình toàn cục của máy tính.

---

### Bước 3: Tạo tệp tin mới

```bash
# Tạo file Main.java với nội dung khởi tạo dự án
```

Nội dung file `Main.java`:
```java
// Main.java - Khởi tạo dự án phần mềm mới
// Tác giả: ngotrungchien

public class Main {
    public static void main(String[] args) {
        System.out.println("Chào mừng đến với dự án phần mềm!");
        System.out.println("Repository đã được khởi tạo thành công với Git.");
    }
}
```

---

### Bước 4: Đưa file vào Staging Area (git add)

```bash
git add Main.java
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
	new file:   Main.java
```

---

### Bước 5: Thực hiện Commit đầu tiên

```bash
git commit -m "feat: Khoi tao du an va them file Main.java"
```

**Kết quả:**
```
[master (root-commit) f2649c2] feat: Khoi tao du an va them file Main.java
 1 file changed, 10 insertions(+)
 create mode 100644 Main.java
```

---

## Kết quả kiểm tra

### Kiểm tra tên tác giả cục bộ

```bash
git config --local user.name
```

**Kết quả:**
```
ngotrungchien
```

---

### Kiểm tra email cục bộ

```bash
git config --local user.email
```

**Kết quả:**
```
ngotrungchien232@gmail.com
```

---

### Xem lịch sử commit

```bash
git log --oneline
```

**Kết quả:**
```
f2649c2 feat: Khoi tao du an va them file Main.java
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
user.name=ngotrungchien
user.email=ngotrungchien232@gmail.com
```

---

## Tổng kết

| Yêu cầu | Trạng thái |
|---------|-----------|
| Khởi tạo Git repository (`git init`) | ✅ Hoàn thành |
| Cấu hình `user.name` với `--local` | ✅ Hoàn thành |
| Cấu hình `user.email` với `--local` | ✅ Hoàn thành |
| Tạo file mới (`Main.java`) | ✅ Hoàn thành |
| Đưa file vào Staging Area (`git add`) | ✅ Hoàn thành |
| Thực hiện commit đầu tiên (`git commit`) | ✅ Hoàn thành |
| Kiểm tra lịch sử commit (`git log --oneline`) | ✅ Hoàn thành |

> Tất cả các yêu cầu của bài tập đã được hoàn thành thành công. Repository cục bộ đã được khởi tạo, danh tính tác giả đã được cấu hình ở cấp độ local (không ảnh hưởng global), và commit đầu tiên đã được ghi lại trong lịch sử Git.
