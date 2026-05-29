# Personal Website — GitHub Pages

Website cá nhân tĩnh cho nhà nghiên cứu, gồm phần **Công bố** chia **3 cột** theo 3 hướng nghiên cứu.

## Cấu trúc thư mục

```
.
├── index.html          # Nội dung chính — chỉnh sửa tại đây
├── css/style.css       # Giao diện
├── js/main.js          # Menu mobile, năm footer
├── assets/
│   └── photo.svg       # Ảnh mẫu — thay bằng photo.jpg của bạn
└── README.md
```

## Chỉnh sửa nội dung

1. Mở `index.html` và thay toàn bộ placeholder: tên, email, bio, ORCID, địa chỉ.
2. Đổi tiêu đề 3 hướng nghiên cứu ở cả section **Hướng nghiên cứu** và **Công bố khoa học** (3 cột phải trùng tên).
3. Thêm/xóa bài báo: copy block `<li class="pub-item">...</li>` trong cột tương ứng.
4. Ảnh đại diện: đặt file `assets/photo.jpg`, rồi trong `index.html` đổi:
   ```html
   <img src="assets/photo.jpg" alt="Tên của bạn" ... />
   ```

## Xem trước trên máy

```bash
cd /đường/dẫn/tới/1.PersonalWebsite
python3 -m http.server 8080
```

Mở trình duyệt: http://localhost:8080

---

## Deploy miễn phí lên GitHub Pages

### Bước 1: Tạo repository trên GitHub

1. Đăng nhập [GitHub](https://github.com).
2. **New repository**:
   - **User site** (khuyên dùng): tên repo = `yourusername.github.io` → URL: `https://yourusername.github.io`
   - **Project site**: tên bất kỳ (vd. `personal-website`) → URL: `https://yourusername.github.io/personal-website/`

### Bước 2: Đẩy code lên GitHub

Trong thư mục project (thay `yourusername` và tên repo):

```bash
git init
git add .
git commit -m "Initial personal website"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

### Bước 3: Bật GitHub Pages

1. Vào repo trên GitHub → **Settings** → **Pages**.
2. **Source**: Deploy from a branch.
3. **Branch**: `main` / folder **`/ (root)`**.
4. **Save**. Sau 1–3 phút site có tại URL ở bước 1.

### Project site (repo không phải `username.github.io`)

Nếu repo tên `personal-website`, sau khi bật Pages URL là:

`https://yourusername.github.io/personal-website/`

Không cần sửa đường dẫn CSS/JS vì dùng đường dẫn tương đối (`css/`, `js/`, `assets/`).

### Cập nhật sau này

```bash
# Sửa index.html hoặc css/style.css
git add .
git commit -m "Update publications"
git push
```

GitHub Pages tự build lại trong vài phút.

---

## Gợi ý

- Domain riêng: **Settings → Pages → Custom domain**.
- Xuất publication từ Google Scholar / BibTeX rồi copy vào từng cột thủ công (đơn giản, không cần build tool).
- Nếu cần song ngữ Việt/Anh, có thể nhân đôi section hoặc thêm trang `en.html` sau.

## License

Nội dung website thuộc bạn. Code template dùng tự do cho mục đích cá nhân.
