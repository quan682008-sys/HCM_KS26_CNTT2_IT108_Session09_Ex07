## Phần 1: Phân tích lỗi

### Lỗi 1: Dòng 1 – Sai cú pháp Heading
- **Viết:** `\## Hướng Dẫn Nộp Bài Tập - Session 08`
- **Lỗi:** Có dấu `\` trước `##`.
- **Hậu quả:** Tiêu đề có thể hiển thị ký tự `##` thay vì được render thành tiêu đề H1.

### Lỗi 2: Thiếu khoảng trắng sau dấu `#`
- **Hậu quả:** Không được nhận diện đúng là tiêu đề Markdown H3.
- `###Lưu ý quan trọng` phải có dấu cách giữa `#` và lưu

### Lỗi 3: Dòng 5–8 Sai cú pháp
- Thiếu khoảng trắng “`-Bước1`”
- **Hậu quả:** Các bước có thể hiển thị thành văn bản thường thay vì danh sách có dấu chấm.

### Lỗi 4: Dòng 5 – Sai cú pháp đường dẫn
- **Viết:** `[GitHub]\([[github.com](http://github.com)](http://github.com))`
- **Lỗi:** Cú pháp liên kết bị lồng sai và có dấu `\` không cần thiết.
- **Hậu quả:** Đường dẫn có thể hiển thị sai hoặc không tạo được liên kết như mong muốn.
- **Cách sửa:** `[GitHub](https://github.com)`

### Lỗi 5: Dòng 6 – Thiếu dấu đóng Bold
- **Viết:** `**HNKS25CNTT1_IT101_Session08`
- **Lỗi:** Có dấu mở `**` nhưng không có dấu đóng.
- **Hậu quả:** Phần chữ in đậm có thể không hiển thị đúng, thậm chí ảnh hưởng đến định dạng phần phía sau.

### Lỗi 6: Dòng 8 – Thiếu dấu đóng Italic
- **Viết:** `*Portal`
- **Lỗi:** Có dấu mở `*` nhưng thiếu dấu đóng.
- **Hậu quả:** Chữ Portal không được in nghiêng đúng cách hoặc làm ảnh hưởng đến định dạng văn bản tiếp theo.

### Lỗi 7: Dòng 10 – Sai cú pháp Blockquote và Bold
- **Viết:** `*> Deadline: Chủ nhật 23:59 —&#x20;*\*Nộp muộn sẽ bị trừ 50% điểm!\*\*`
- **Lỗi:** Ký hiệu `>` bị đặt sau `*`, dấu in nghiêng không đóng đúng và ký hiệu Bold bị thêm dấu `\` không cần thiết.
- **Hậu quả:** Nội dung Deadline có thể không hiển thị thành trích dẫn và phần cảnh báo không được in đậm như mong muốn.

### Lỗi 8: Các dòng trống bị thêm dấu `\`
- **Lỗi:** Dùng dấu `\` riêng trên dòng trống không cần thiết.
- **Hậu quả:** Có thể xuất hiện ký tự không mong muốn hoặc gây khó đọc mã nguồn Markdown.

---

## Phần 2: Sửa

```markdown
# Hướng Dẫn Nộp Bài Tập - Session 08
### Lưu ý quan trọng
Các bước nộp bài:
- Bước 1: Tạo tài khoản GitHub tại [GitHub](https://github.com)
- Bước 2: Tạo repository mới đặt tên theo định dạng **HNKS25CNTT1_IT101_Session08**
- Bước 3: Upload file .md của bài làm lên repository
- Bước 4: Copy đường dẫn và nộp lên *Portal*
> **Deadline:** Chủ nhật 23:59  
> **Nộp muộn sẽ bị trừ 50% điểm!**
```

---

## Phần 3: Nếu quên `https://` thì sao?

Nếu sinh viên viết `[GitHub](github.com)` thì Markdown vẫn tạo liên kết, nhưng trình duyệt có thể hiểu `github.com` là đường dẫn tương đối của trang hiện tại thay vì website GitHub.
