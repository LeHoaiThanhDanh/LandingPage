# Hướng dẫn Deploy lên Vercel

## Phương pháp 1: Deploy qua Vercel Dashboard (Khuyên dùng)

### Bước 1: Tạo Git Repository

1. Tạo repository mới trên GitHub/GitLab/Bitbucket
2. Commit tất cả file trong folder này:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin <URL_REPOSITORY_CUA_BAN>
git push -u origin main
```

### Bước 2: Deploy trên Vercel

1. Truy cập [vercel.com](https://vercel.com)
2. Đăng nhập bằng tài khoản GitHub/GitLab/Bitbucket
3. Click **"Add New Project"**
4. Chọn **"Import Git Repository"**
5. Tìm và chọn repository bạn vừa tạo
6. Vercel sẽ tự động:
   - Phát hiện config từ `vercel.json`
   - Build và deploy website
7. Click **"Deploy"**
8. Đợi vài giây, website sẽ live tại URL do Vercel cung cấp

### Bước 3: Custom Domain (Tùy chọn)

1. Vào project settings trên Vercel
2. Chọn tab **"Domains"**
3. Thêm domain của bạn
4. Cập nhật DNS records theo hướng dẫn

---

## Phương pháp 2: Deploy qua Vercel CLI

### Bước 1: Cài đặt Vercel CLI

```bash
npm install -g vercel
```

### Bước 2: Login

```bash
vercel login
```

### Bước 3: Deploy

Trong folder project, chạy:

```bash
vercel
```

Trả lời các câu hỏi:
- **Set up and deploy?** → Yes
- **Which scope?** → Chọn account của bạn
- **Link to existing project?** → No
- **What's your project name?** → uel-study-camp-programme (hoặc tên tùy ý)
- **In which directory?** → ./ (enter)
- **Want to override settings?** → No

### Bước 4: Deploy Production

```bash
vercel --prod
```

---

## Phương pháp 3: Deploy trực tiếp (Drag & Drop)

1. Truy cập [vercel.com](https://vercel.com)
2. Đăng nhập
3. Kéo thả folder **LandingPage** vào trang Vercel
4. Vercel sẽ tự động upload và deploy

**Lưu ý:** Phương pháp này không tự động update khi bạn thay đổi code.

---

## Kiểm tra sau khi Deploy

1. Mở URL do Vercel cung cấp
2. Kiểm tra:
   - ✅ Header hiển thị đúng
   - ✅ Footer hiển thị đúng
   - ✅ Navbar hiển thị đúng
   - ✅ Tất cả hình ảnh load được
   - ✅ Các link hoạt động
   - ✅ Header ẩn/hiện khi scroll
   - ✅ Responsive trên mobile

---

## Troubleshooting

### Vấn đề: Header/Footer không hiển thị

**Nguyên nhân:** Fetch API bị CORS block

**Giải pháp:** File `vercel.json` đã được config CORS headers. Nếu vẫn lỗi, kiểm tra Console trong DevTools.

### Vấn đề: Hình ảnh không hiển thị

**Nguyên nhân:** Path không đúng hoặc file không tồn tại

**Giải pháp:** 
- Đảm bảo tất cả file ảnh trong folder `images/`
- Kiểm tra tên file khớp với code (case-sensitive)
- Deploy lại sau khi thêm ảnh

### Vấn đề: Styles bị lỗi

**Nguyên nhân:** CSS files không được load

**Giải pháp:**
- Kiểm tra path trong `<link>` tags
- Clear cache trình duyệt (Ctrl + Shift + R)
- Kiểm tra Network tab trong DevTools

---

## Cập nhật Website

### Nếu deploy qua Git:
```bash
git add .
git commit -m "Update content"
git push
```
Vercel sẽ tự động rebuild và deploy.

### Nếu deploy qua CLI:
```bash
vercel --prod
```

---

## Environment Variables (Nếu cần)

Nếu cần thêm biến môi trường:

1. Vào Vercel Dashboard
2. Chọn project
3. Settings → Environment Variables
4. Thêm biến và giá trị

---

## Support

- [Vercel Documentation](https://vercel.com/docs)
- [Vercel Support](https://vercel.com/support)
