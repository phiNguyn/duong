# 📚 TÀI LIỆU HỌC TẬP - WEBSITE TRƯỜNG THPT HỒ THỊ BI

## 🎯 MỤC ĐÍCH DỰ ÁN

Dự án này là một website giới thiệu về Trường THPT Hồ Thị Bi và các câu lạc bộ trong trường. Website được xây dựng bằng HTML và CSS thuần, phù hợp cho việc học tập và thuyết trình về các kỹ thuật web cơ bản.

---

## 📁 CẤU TRÚC THƯ MỤC

```
Duong/
├── index.html              # Trang chủ
├── bongda.html            # Trang chi tiết CLB Bóng đá
├── vannghe.html           # Trang chi tiết CLB Văn nghệ
├── bongchuyen.html        # Trang chi tiết CLB Bóng Chuyền
├── nhay.html              # Trang chi tiết CLB Nhảy
├── css/
│   ├── styles.css         # CSS cho trang chủ
│   └── detail.css         # CSS cho trang chi tiết
├── images/                # Thư mục chứa hình ảnh
│   ├── bongda/
│   ├── cahat/
│   ├── bongchuyen/
│   └── nhay/
└── README.md              # File này
```

---

## 🏷️ CÁC THẺ HTML ĐƯỢC SỬ DỤNG

### 1. **Thẻ Cấu Trúc Cơ Bản**

#### `<html>` và `<head>`

```html
<html lang="vi">
  <head>
    <meta charset="UTF-8" />
    <title>Trường THPT Hồ Thị Bi</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="css/styles.css" />
  </head>
</html>
```

**Giải thích:**

- `<html lang="vi">`: Khai báo ngôn ngữ tiếng Việt
- `<meta charset="UTF-8">`: Định dạng mã hóa ký tự (hỗ trợ tiếng Việt)
- `<meta name="viewport">`: Tối ưu hiển thị trên mobile
- `<link rel="stylesheet">`: Liên kết file CSS

#### `<header>`

```html
<header>
  <p>Học tập – Sáng tạo – Phát triển toàn diện</p>
  <p class="school-name">Trường THPT Hồ Thị Bi</p>
</header>
```

**Giải thích:**

- Thẻ semantic HTML5, dùng cho phần đầu trang
- Chứa thông tin chính của website

#### `<section>`

```html
<section id="gioithieu" class="intro">
  <!-- Nội dung -->
</section>
```

**Giải thích:**

- Thẻ semantic HTML5, chia trang thành các phần
- `id`: Định danh duy nhất (dùng cho anchor links)
- `class`: Nhóm các phần tử để style CSS

### 2. **Thẻ Nội Dung**

#### `<h1>`, `<h2>`, `<h3>` - Tiêu đề

```html
<h1>Tiêu đề chính</h1>
<h2>Tiêu đề phụ</h2>
<h3>Tiêu đề nhỏ</h3>
```

**Giải thích:**

- Thứ bậc từ h1 (lớn nhất) đến h6 (nhỏ nhất)
- Quan trọng cho SEO và cấu trúc trang

#### `<p>` - Đoạn văn

```html
<p>Nội dung đoạn văn bản...</p>
```

**Giải thích:**

- Dùng để chứa đoạn văn bản
- Tự động xuống dòng và có khoảng cách

#### `<div>` - Container

```html
<div class="intro-container">
  <!-- Nội dung -->
</div>
```

**Giải thích:**

- Thẻ không có ý nghĩa ngữ nghĩa, dùng để nhóm và layout
- Rất linh hoạt trong CSS

#### `<span>` - Inline container

```html
<span class="intro-highlight">Hồ Thị Bi</span>
```

**Giải thích:**

- Tương tự `<div>` nhưng inline (không xuống dòng)
- Dùng để style một phần text

### 3. **Thẻ Liên Kết và Điều Hướng**

#### `<a>` - Link

```html
<a href="bongda.html" class="club-link">
  <!-- Nội dung clickable -->
</a>
```

**Giải thích:**

- `href`: Địa chỉ trang đích
- Có thể link nội bộ (trang khác) hoặc ngoài (`target="_blank"`)

### 4. **Thẻ Danh Sách**

#### `<ul>` và `<li>` - Danh sách không thứ tự

```html
<ul>
  <li>Mục 1</li>
  <li>Mục 2</li>
</ul>
```

**Giải thích:**

- `<ul>`: Unordered list (danh sách có dấu chấm)
- `<li>`: List item (từng mục)

### 5. **Thẻ Hình Ảnh**

#### `<img>`

```html
<img src="images/bongda/h1.jpg" alt="CLB Bóng đá hoạt động 1" />
```

**Giải thích:**

- `src`: Đường dẫn hình ảnh
- `alt`: Mô tả hình ảnh (quan trọng cho accessibility và SEO)

### 6. **Thẻ SVG (cho icon Facebook)**

```html
<svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24">
  <path d="..."></path>
</svg>
```

**Giải thích:**

- Vector graphics, không bị vỡ khi zoom
- Dùng cho icon và logo

---

## 🎨 CÁC HIỆU ỨNG CSS VÀ KỸ THUẬT

### 1. **CSS Selectors (Bộ Chọn)**

#### Class Selector

```css
.intro-container {
  background: white;
  border-radius: 16px;
}
```

**Giải thích:** Chọn tất cả phần tử có `class="intro-container"`

#### ID Selector

```css
#gioithieu {
  padding: 40px 20px;
}
```

**Giải thích:** Chọn phần tử có `id="gioithieu"`

#### Pseudo-element `::before` và `::after`

```css
header::before {
  content: "";
  position: absolute;
  background: rgba(0, 0, 0, 0.5);
}
```

**Giải thích:**

- Tạo phần tử giả trước/sau phần tử thật
- `content: ""` là bắt buộc
- Dùng để tạo overlay, decoration

#### Pseudo-class `:hover`

```css
.club:hover {
  transform: translateY(-5px);
}
```

**Giải thích:** Áp dụng style khi di chuột vào phần tử

### 2. **Layout Techniques**

#### Flexbox

```css
header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
```

**Giải thích:**

- `display: flex`: Bật flexbox
- `flex-direction: column`: Xếp dọc
- `justify-content: center`: Căn giữa theo trục chính
- `align-items: center`: Căn giữa theo trục phụ

#### CSS Grid

```css
.clubs {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}
```

**Giải thích:**

- `display: grid`: Bật grid layout
- `repeat(auto-fit, minmax(250px, 1fr))`: Tự động điều chỉnh số cột
- `gap: 20px`: Khoảng cách giữa các item

### 3. **Positioning (Định Vị)**

#### `position: relative`

```css
.club {
  position: relative;
}
```

**Giải thích:** Đặt vị trí tương đối, làm mốc cho phần tử con `absolute`

#### `position: absolute`

```css
.view-more-btn {
  position: absolute;
  bottom: 20px;
  left: 50%;
}
```

**Giải thích:** Định vị tuyệt đối so với phần tử cha có `position: relative`

### 4. **Transform và Transition**

#### Transform

```css
.club:hover {
  transform: translateY(-5px) scale(1.02);
}
```

**Giải thích:**

- `translateY(-5px)`: Di chuyển lên 5px
- `scale(1.02)`: Phóng to 2%
- Có thể kết hợp nhiều transform

#### Transition

```css
.club {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
```

**Giải thích:**

- Tạo hiệu ứng chuyển động mượt
- `0.3s`: Thời gian (0.3 giây)
- `ease`: Kiểu chuyển động (nhanh rồi chậm)

### 5. **Background và Gradient**

#### Background Image

```css
header {
  background-image: url("../images/header.jpg");
  background-size: cover;
  background-position: center;
}
```

**Giải thích:**

- `background-size: cover`: Phủ kín, có thể cắt
- `background-position: center`: Căn giữa

#### Linear Gradient

```css
.intro {
  background: linear-gradient(135deg, #f5f7fa 0%, #e8ecf1 100%);
}
```

**Giải thích:**

- `135deg`: Góc gradient (45 độ chéo)
- `#f5f7fa 0%`: Màu bắt đầu
- `#e8ecf1 100%`: Màu kết thúc

### 6. **Box Shadow (Đổ Bóng)**

```css
.intro-container {
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
}
```

**Giải thích:**

- `0`: Offset X (không lệch ngang)
- `10px`: Offset Y (lệch xuống 10px)
- `40px`: Blur radius (độ mờ)
- `rgba(0, 0, 0, 0.1)`: Màu đen với độ trong suốt 10%

### 7. **Z-index (Lớp Xếp)**

```css
header::before {
  z-index: 1;
}
header p {
  z-index: 2;
}
```

**Giải thích:**

- Số càng lớn, càng ở trên
- Chỉ hoạt động với `position: relative/absolute/fixed`

### 8. **Opacity (Độ Trong Suốt)**

```css
.view-more-btn {
  opacity: 0; /* Ẩn */
}
.club:hover .view-more-btn {
  opacity: 1; /* Hiện */
}
```

**Giải thích:**

- `0`: Hoàn toàn trong suốt (ẩn)
- `1`: Hoàn toàn đục (hiện)
- `0.5`: 50% trong suốt

### 9. **Responsive Design (Thiết Kế Đáp Ứng)**

#### Media Queries

```css
@media (max-width: 768px) {
  .intro-container {
    padding: 35px 25px;
  }
}
```

**Giải thích:**

- Áp dụng style khi màn hình ≤ 768px
- Tối ưu cho tablet và mobile

### 10. **Object-fit (Căn Hình Ảnh)**

```css
.gallery-item img {
  object-fit: cover;
}
```

**Giải thích:**

- `cover`: Phủ kín, cắt phần thừa
- `contain`: Hiển thị toàn bộ, có thể có khoảng trống

---

## 🎯 CÁC HIỆU ỨNG ĐẶC BIỆT TRONG DỰ ÁN

### 1. **Hiệu Ứng Overlay trên Header**

```css
header::before {
  content: "";
  position: absolute;
  background: rgba(0, 0, 0, 0.5);
  z-index: 1;
}
```

**Cách hoạt động:**

- Tạo lớp phủ tối màu đen 50% trên hình nền
- Giúp chữ trắng dễ đọc hơn

### 2. **Hiệu Ứng Card Hover**

```css
.club:hover {
  transform: translateY(-5px) scale(1.02);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
}
.club:hover::before {
  transform: scale(1.1);
}
```

**Cách hoạt động:**

- Khi hover: card nâng lên, phóng to nhẹ, đổ bóng
- Hình ảnh zoom 1.1 lần
- Tạo cảm giác tương tác

### 3. **Hiệu Ứng Nút "Xem thêm" Chạy Từ Dưới Lên**

```css
.view-more-btn {
  transform: translateX(-50%) translateY(100px);
  opacity: 0;
}
.club:hover .view-more-btn {
  transform: translateX(-50%) translateY(0);
  opacity: 1;
}
```

**Cách hoạt động:**

- Ban đầu: nút ở dưới (translateY(100px)) và ẩn (opacity: 0)
- Khi hover: nút chạy lên và hiện ra
- `translateX(-50%)`: Căn giữa ngang

### 4. **Hiệu Ứng Gallery Hover**

```css
.gallery-item:hover {
  transform: translateY(-5px);
}
.gallery-item:hover img {
  transform: scale(1.05);
}
```

**Cách hoạt động:**

- Card nâng lên khi hover
- Hình ảnh bên trong zoom nhẹ
- Tạo độ sâu 3D

### 5. **Gradient Border**

```css
.intro-container::before {
  content: "";
  height: 5px;
  background: linear-gradient(90deg, #133c7a, #1a4fa3, #133c7a);
}
```

**Cách hoạt động:**

- Tạo viền gradient bằng pseudo-element
- Đặt ở trên cùng container

---

## 📝 HƯỚNG DẪN THUYẾT TRÌNH

### Phần 1: Giới Thiệu Dự Án (2 phút)

- Mục đích: Website giới thiệu trường và CLB
- Công nghệ: HTML5, CSS3 thuần
- Tính năng: Responsive, hiệu ứng tương tác

### Phần 2: Cấu Trúc HTML (3 phút)

- Giải thích các thẻ semantic: `<header>`, `<section>`
- Thẻ container: `<div>`, `<span>`
- Thẻ nội dung: `<h1-h3>`, `<p>`, `<ul>`, `<li>`
- Thẻ liên kết: `<a>`

### Phần 3: Layout và CSS (5 phút)

- **Flexbox**: Căn giữa header
- **Grid**: Layout card CLB responsive
- **Position**: Định vị nút "Xem thêm"
- **Transform & Transition**: Hiệu ứng hover

### Phần 4: Hiệu Ứng Đặc Biệt (5 phút)

- **Overlay**: Lớp phủ trên header
- **Card Hover**: Nâng lên, zoom, đổ bóng
- **Nút "Xem thêm"**: Animation từ dưới lên
- **Gallery**: Hover effect cho hình ảnh

### Phần 5: Responsive Design (3 phút)

- Media queries cho mobile/tablet
- Grid tự điều chỉnh số cột
- Font size và padding responsive

### Phần 6: Demo và Kết Luận (2 phút)

- Demo website trên trình duyệt
- Tóm tắt kiến thức đã học
- Q&A

---

## 🎓 KIẾN THỨC CẦN NẮM ĐỂ THUYẾT TRÌNH

### HTML

- ✅ Semantic HTML5 (`<header>`, `<section>`, `<nav>`)
- ✅ Cấu trúc trang web cơ bản
- ✅ Thẻ liên kết và điều hướng
- ✅ Form và input (nếu có)

### CSS

- ✅ Selectors (class, ID, pseudo-class, pseudo-element)
- ✅ Box Model (margin, padding, border)
- ✅ Flexbox và Grid Layout
- ✅ Position (relative, absolute, fixed)
- ✅ Transform và Transition
- ✅ Media Queries (Responsive)
- ✅ Gradient và Shadow

### Best Practices

- ✅ Code có cấu trúc, dễ đọc
- ✅ Đặt tên class có ý nghĩa
- ✅ Responsive design
- ✅ Performance (tối ưu hình ảnh)

---

## 💡 GỢI Ý MỞ RỘNG

1. **Thêm JavaScript**: Tạo menu mobile, slider hình ảnh
2. **Thêm Form**: Form đăng ký tham gia CLB
3. **Animation**: Thêm animation khi scroll
4. **Dark Mode**: Toggle chế độ sáng/tối
5. **SEO**: Tối ưu meta tags, alt text

---

## 📚 TÀI LIỆU THAM KHẢO

- [MDN Web Docs](https://developer.mozilla.org/)
- [CSS-Tricks](https://css-tricks.com/)
- [W3Schools](https://www.w3schools.com/)
- [Can I Use](https://caniuse.com/) - Kiểm tra browser support

---

## 👥 TÁC GIẢ

Dự án được tạo cho mục đích học tập và thuyết trình tại Trường THPT Hồ Thị Bi.

**Chúc các bạn học tập tốt và thuyết trình thành công! 🎉**
