# Đưa web Bánh Mì Thơm Ngon lên GitHub Pages

Thư mục cần đưa lên: `C:/Users/admin/.abacusai-bot/bot-home/github-pages/`
Trong đó đã có sẵn: `index.html`, `README.md`, `.nojekyll`

---

## Cách A — Tải file lên bằng trình duyệt (không cần cài gì)

### 1. Tạo tài khoản
Vào **github.com** → **Sign up** → điền email, mật khẩu, tên tài khoản.
Tên tài khoản sẽ thành một phần địa chỉ web, ví dụ tên `banhmihoacai` thì
web sẽ là `https://banhmihoacai.github.io/banh-mi/`.

### 2. Tạo repository
- Bấm dấu **+** ở góc trên phải → **New repository**
- **Repository name**: `banh-mi`
- Chọn **Public** (bắt buộc — Pages miễn phí chỉ chạy với repo công khai)
- Đánh dấu **Add a README file**
- Bấm **Create repository**

### 3. Tải file lên
- Trong repo vừa tạo, bấm **Add file** → **Upload files**
- Kéo 3 file này vào (từ thư mục `github-pages`):
  - `index.html`
  - `README.md`
  - `.nojekyll`
- Ô dưới cùng bấm **Commit changes**

### 4. Bật GitHub Pages
- Vào tab **Settings** (thanh trên cùng của repo)
- Cột trái chọn **Pages**
- **Source**: `Deploy from a branch`
- **Branch**: chọn `main`, thư mục `/ (root)` → **Save**
- Chờ 1–2 phút, tải lại trang Settings → Pages, sẽ thấy dòng xanh:
  **Your site is live at https://...**

### 5. Mở thử
Bấm vào link đó trên điện thoại. Xong.

---

## Cách B — Dùng git trên máy (nhanh hơn khi sửa nhiều lần)

Mở **Git Bash** hoặc **PowerShell** tại thư mục `github-pages`:

```
git init
git add .
git commit -m "Banh Mi Thom Ngon - ban dau"
git branch -M main
git remote add origin https://github.com/<tên-tài-khoản>/banh-mi.git
git push -u origin main
```

Lần đầu push sẽ hỏi đăng nhập. GitHub không nhận mật khẩu thường nữa —
cần **Personal Access Token**:

1. github.com → ảnh đại diện → **Settings**
2. Kéo xuống **Developer settings** → **Personal access tokens** → **Tokens (classic)**
3. **Generate new token (classic)**
4. Note: `banh-mi` · Expiration: 90 days · Tick ô **repo**
5. **Generate token** → copy chuỗi `ghp_...` (chỉ hiện 1 lần)
6. Khi git hỏi Password, dán chuỗi đó vào

Sau đó bật Pages như bước 4 ở Cách A.

---

## Sau này sửa web thì sao

Mỗi lần sửa `index.html`, chỉ cần:

```
git add .
git commit -m "sua gi do"
git push
```

Chờ khoảng 1 phút, web tự cập nhật. Không phải bật lại Pages.

---

## Lưu ý quan trọng

**Dữ liệu không nằm trên GitHub.** Mỗi điện thoại lưu sổ riêng trong trình
duyệt của nó. Hai người mở cùng một link sẽ thấy hai cuốn sổ khác nhau.
Muốn nhiều người dùng chung một sổ thì cần máy chủ và cơ sở dữ liệu.

**Đừng để lộ thông tin cá nhân** trong repo công khai: số điện thoại, địa chỉ
nhà, ảnh giấy tờ.

**Tên miền riêng** (ví dụ `banhmithomngon.vn`) cần mua ở nhà cung cấp tên miền,
giá khoảng 200.000–400.000đ/năm. Sau đó vào Settings → Pages → Custom domain.

---

## Bản dựng sẵn

Thư mục `github-pages/` đã sẵn sàng, không cần sửa gì thêm.
File `index.html` ở đây chính là bản mới nhất của web (57KB, chạy offline).
