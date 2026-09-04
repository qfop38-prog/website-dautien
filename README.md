Xưởng Vibe
Portfolio một trang cho các dự án vibecoding. Mỗi dự án công khai prompt gốc,
nhật ký vòng lặp, và số liệu prompt / ngày ý-tưởng-đến-deploy / % code do AI viết.
Toàn bộ trang nằm trong một file `index.html` duy nhất — không build step,
không dependency. Chỉ tải font từ Google Fonts.
Chạy thử ở máy
Mở thẳng `index.html` bằng trình duyệt là xong. Hoặc:
```bash
python3 -m http.server 8000   # rồi mở http://localhost:8000
```
Deploy lên GitHub Pages
Push repo này lên GitHub.
Vào Settings → Pages.
Mục Source chọn Deploy from a branch, branch `main`, thư mục `/ (root)`.
Đợi 1–2 phút, trang sẽ chạy ở `https://<username>.github.io/<tên-repo>/`.
Sửa nội dung
Mọi thứ nằm trong mảng `PROJECTS` ở cuối `index.html`:
```js
{
  id:"cho-dem",              // dùng cho anchor, viết không dấu
  name:"Chợ Đêm",
  kind:"Web App",            // tự sinh ra nút lọc
  status:"live",             // live | beta | lab
  tag:"Mô tả một câu.",
  stack:["React","Mapbox GL"],
  prompts:62, days:4, ai:88, // thanh telemetry tự cộng từ đây
  model:"Opus",
  demo:"chodem.demo",
  seed:"Prompt gốc nguyên văn...",
  log:[{t:"Prompt 1–8 · Dựng khung", d:"Chuyện gì đã xảy ra."}],
  lesson:"Rút ra được gì."
}
```
Thanh telemetry và con số "trung bình vòng lặp" tự tính từ mảng này,
nên sửa dự án là số tự khớp.
Cần thay trước khi public
[ ] 6 dự án mẫu trong `PROJECTS`
[ ] Email `xin-chao@xuongvibe.dev` ở mục Liên hệ
[ ] Tên thương hiệu `XƯỞNG//VIBE` ở nav và footer
[ ] `og:url` và `og:image` trong `<head>` (cho link preview khi share)
