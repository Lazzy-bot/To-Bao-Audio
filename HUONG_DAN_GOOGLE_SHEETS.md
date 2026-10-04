# 📖 Hướng Dẫn Quản Lý Link Bio Qua Google Sheets & Đẩy Lên GitHub Pages

Tài liệu này hướng dẫn cách giúp **người không biết lập trình** có thể tự do thay đổi, thêm bớt link bio hàng ngày chỉ bằng cách nhập vào **Google Sheets** (trên máy tính hoặc app điện thoại).

---

## BƯỚC 1: Tạo Bảng Google Sheets Mẫu

1. Truy cập [Google Sheets (Trang tính)](https://sheets.new) để tạo 1 file mới. Đặt tên là `Tổ Báo Audio - Link Bio`.
2. Tạo **5 cột** ở hàng đầu tiên (Dòng 1):

| Vị trí | Biểu tượng | Tiêu đề | Mô tả | Đường link |
| :--- | :---: | :--- | :--- | :--- |
| Mới nhất | 🎧 | Nghe tập mới nhất | Tập mới lên sóng mỗi tối | https://youtube.com/watch?v=... |
| Tổ Báo Audio | ▶️ | Trọn bộ Playlist | Bấm để nghe liền mạch toàn bộ các tập | https://youtube.com/playlist?list=... |
| Mạng xã hội | 📺 | YouTube | | https://youtube.com/@tobaoaudio |
| Mạng xã hội | 🎵 | TikTok | | https://tiktok.com/@tobaoaudio |
| Mạng xã hội | 📘 | Facebook | | https://facebook.com/tobaoaudio |
| Mạng xã hội | 🎧 | Spotify | | https://spotify.com/... |

> 💡 **Quy ước đơn giản:**
> - Cột **Vị trí**: 
>   - Ghi `Mới nhất` -> Nút to nổi bật trên cùng.
>   - Ghi `Mạng xã hội` -> Nút tròn nhỏ ở dưới cùng.
>   - Ghi tên bất kỳ (vd: `Tổ Báo Audio`, `Kênh thứ hai`, `Truyện ma đêm khuya`) -> Tự tạo nhóm riêng tương ứng.
> - Cột **Đường link**: Muốn đổi link chỉ cần dán đè link mới vào cột này.

---

## BƯỚC 2: Mở Quyền Xem Cho Trang Web

1. Ở góc trên bên phải Google Sheets, bấm nút **Chia sẻ** (Share).
2. Tại mục *Quyền truy cập chung*, chuyển từ **Hạn chế** sang **"Bất kỳ ai có đường liên kết"** (Anyone with the link) với quyền **Người xem** (Viewer).
3. Bấm **Sao chép đường liên kết**.
   *(Link sẽ có dạng: `https://docs.google.com/spreadsheets/d/1a2b3c.../edit?usp=sharing`)*

---

## BƯỚC 3: Dán Link Vào File `index.html`

1. Mở file [index.html](file:///c:/Users/Giap/OneDrive%20-%20Industrial%20University%20of%20HoChiMinh%20City/Desktop/ToBaoAudio/index.html).
2. Tìm dòng số **82**:
   ```javascript
   const GOOGLE_SHEET_URL = ""; 
   ```
3. Dán link Google Sheets của bạn vào giữa 2 dấu `""`:
   ```javascript
   const GOOGLE_SHEET_URL = "https://docs.google.com/spreadsheets/d/1a2b3c.../edit?usp=sharing";
   ```
4. Bấm `Ctrl + S` để lưu file.

---

## BƯỚC 4: Đẩy Lên GitHub Pages

1. Đăng nhập vào [GitHub](https://github.com/) và tạo 1 repository mới (ví dụ tên: `bio` hoặc `tobaoaudio`), chọn chế độ **Public**.
2. Tải toàn bộ các file trong thư mục này lên (đặc biệt là file `index.html`).
3. Vào mục **Settings** của repository trên GitHub:
   - Chọn mục **Pages** ở menu bên trái.
   - Tại phần **Branch**, chọn `main` (hoặc `master`) và thư mục `/(root)`, sau đó bấm **Save**.
4. Sau 1–2 phút, bạn sẽ nhận được đường link web có dạng:
   `https://<tên-tài-khoản-github>.github.io/<tên-repo>/`

---

## 🎉 Từ Giờ Về Sau:
Mỗi khi ra tập mới, đổi kênh, thêm mạng xã hội:
👉 **Bạn chỉ cần mở Google Sheets trên điện thoại hoặc máy tính, dán link vào ô tương ứng.**
Trang web Link Bio sẽ tự động cập nhật ngay lập tức mà **không cần mở file code nữa!**
