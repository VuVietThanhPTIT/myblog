# CẨM NANG HƯỚNG DẪN VIẾT BÀI BLOG (HUGO THEME STACK)

Tài liệu này hướng dẫn chi tiết cách tạo một bài viết mới từ A-Z: cấu trúc thư mục, ảnh đại diện, ảnh minh họa, gắn tag/danh mục và cú pháp định dạng chữ (to, nhỏ, in đậm, in nghiêng,...).

---

## 1. Cấu trúc thư mục bài viết chuẩn (Page Bundle)

Mỗi bài viết bạn nên tạo thành **1 thư mục riêng** đặt bên trong `content/post/`.

```text
blog/
└── content/
    └── post/
        └── ten-bai-viet-khong-dau/      <-- Tên thư mục bài viết
            ├── index.md                 <-- BẮT BUỘC: Nội dung bài viết
            ├── cover.jpg                <-- Ảnh bìa hiển thị ngoài trang chủ
            ├── anh-1.jpg                <-- Ảnh minh họa trong bài
            └── anh-2.png
```

> ⚠️ **Lưu ý quan trọng về tên file & thư mục:**
> - Đặt tên viết thường, không dấu, dùng dấu gạch ngang `-` thay vì khoảng trắng (ví dụ: `chuyen-di-da-lat`, `hoc-lap-trinh-c`).
> - File bài viết bắt buộc phải đặt tên là `index.md`.

---

## 2. Phần thông tin đầu bài (Front Matter)

Mỗi file `index.md` bắt đầu bằng khối thông tin kẹp giữa 2 cặp dấu gạch ngang `---`:

```yaml
---
title: "Tiêu đề bài viết hiển thị trên blog"
description: "Đoạn mô tả ngắn tóm tắt bài viết (hiện ở card trang chủ)"
date: 2026-11-15 21:00:00+0700
slug: ten-bai-viet-tren-duong-dan-url
image: cover.jpg           # Ảnh bìa làm banner và card ngoài trang chủ
draft: false               # false: xuất bản ngay; true: bài nháp (không hiện lên web)
categories:
    - Lập trình            # Danh mục chính
    - Chia sẻ
tags:
    - Hugo                 # Các thẻ tag để lọc bài
    - GitHub
    - Markdown
weight: 1                  # (Tùy chọn) Số càng nhỏ bài càng được ghim lên đầu
---
```

---

## 3. Cách chèn hình ảnh vào bài viết

Vì ảnh nằm cùng thư mục với `index.md`, bạn chỉ cần gọi tên file trực tiếp:

### 3.1. Chèn một ảnh đơn lẻ
```markdown
![Mô tả ảnh khi không tải được](anh-1.jpg)
```

### 3.2. Chèn album ảnh dạng lưới (Gallery - Thế mạnh của Theme Stack)
Khi bạn đặt 2 hoặc nhiều ảnh **trên cùng 1 dòng** (ngăn cách bởi dấu cách), theme sẽ tự động ghép thành lưới ảnh đẹp mắt và hỗ trợ bấm vào để phóng to toàn màn hình:

```markdown
![Ảnh 1](anh-1.jpg) ![Ảnh 2](anh-2.png)
```

---

## 4. Định dạng chữ trong Markdown (To, nhỏ, in đậm, in nghiêng,...)

### 4.1. Tiêu đề các cấp (Độ to nhỏ của chữ)
Sử dụng dấu thăng `#` ở đầu dòng (càng ít `#` chữ càng to):

```markdown
# Tiêu đề cấp 1 (Heading 1 - Thường chỉ dùng cho tên bài)
## Tiêu đề cấp 2 (Heading 2 - Mục lớn)
### Tiêu đề cấp 3 (Heading 3 - Mục nhỏ)
#### Tiêu đề cấp 4 (Heading 4 - Mục chi tiết)
```

### 4.2. In đậm, in nghiêng, gạch xóa
```markdown
- **Chữ in đậm** (hoặc __Chữ in đậm__)
- *Chữ in nghiêng* (hoặc _Chữ in nghiêng_)
- ***Vừa in đậm vừa in nghiêng***
- ~~Chữ gạch ngang~~
```

### 4.3. Danh sách (Gạch đầu dòng & Đánh số)
```markdown
* Mục thứ nhất
* Mục thứ hai
    * Mục con thụt dòng (bấm 4 phím cách hoặc 1 tab)

1. Bước 1
2. Bước 2
3. Bước 3
```

### 4.4. Trích dẫn (Quote) & Chú thích
```markdown
> Đây là một đoạn trích dẫn nổi bật hoặc ghi chú quan trọng.
> Bạn có thể viết nhiều dòng trong cùng một khối trích dẫn.
```

### 4.5. Chèn đường link (Liên kết)
```markdown
Bấm vào [đây để vào GitHub](https://github.com/VuVietThanhPTIT)
Hoặc để link trần: <https://vuvietthanhptit.github.io/myblog/>
```

### 4.6. Khối mã nguồn (Code snippet)
Dùng 3 dấu backtick ```` ``` ````:

````markdown
```python
def xin_chao(ten):
    print(f"Xin chào {ten} đến với blog!")

xin_chao("Thành")
```
````

### 4.7. Đường kẻ phân cách đoạn văn
Dùng 3 dấu gạch ngang liên tiếp trên một dòng riêng:
```markdown
---
```

---

## 5. Mẫu bài viết hoàn chỉnh để sao chép nhanh

Bạn có thể copy toàn bộ đoạn dưới đây dán vào `index.md` để sửa lại:

````markdown
---
title: "Hành trình bắt đầu xây dựng blog cá nhân"
description: "Chia sẻ lý do và các bước mình tạo ra trang blog cá nhân này."
date: 2026-11-15 21:00:00+0700
slug: hanh-trinh-bat-dau-blog
image: cover.jpg
categories:
    - Nhật ký
tags:
    - Blog
    - GioiThieu
---

Chào mọi người, đây là bài viết đầu tiên trên blog cá nhân của mình!

## 1. Mục tiêu của blog
Mình lập blog này nhằm mục đích:
- **Ghi lại kiến thức** trong quá trình học tập tại PTIT.
- Chia sẻ kinh nghiệm thực tế khi làm các dự án công nghệ.
- *Lưu giữ những kỷ niệm* và chuyến đi thú vị.

## 2. Một số hình ảnh gần đây
Dưới đây là vài bức ảnh mình chụp:

![Bàn làm việc](anh-1.jpg) ![Khuôn viên trường](anh-2.jpg)

> "Hành trình vạn dặm bắt đầu từ một bước chân."

Cảm ơn bạn đã ghé thăm bài viết đầu tiên này!
````

---

## 6. Đẩy bài viết lên web

Sau khi viết xong bài và lưu ảnh vào thư mục:
```bash
cd /home/thanhvv17@fsoft.fpt.vn/blog
git add -A
git commit -m "Them bai viet moi: hanh-trinh-bat-dau-blog"
git push
```
Đợi khoảng 1 phút, bài viết mới sẽ xuất hiện trên: **<https://vuvietthanhptit.github.io/myblog/>**
