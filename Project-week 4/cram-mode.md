# 2. Thiết kế Chế độ Ôn thi Cấp tốc (Cram Mode UI)

## 2.1 Mục tiêu

Cram Mode là chế độ hỗ trợ người dùng ôn tập cường độ cao trong giai đoạn cận kề kỳ thi. Khi được kích hoạt, giao diện sẽ chuyển sang trạng thái **Red Zone (Vùng đỏ)** nhằm tạo cảm giác khẩn cấp và thúc đẩy người dùng tập trung hơn vào việc ôn tập.

---

## 2.2 Điều kiện kích hoạt

Chế độ Cram Mode được sử dụng khi:

* Người dùng chủ động bật chế độ Ôn thi Cấp tốc.
* Ngày thi dự kiến còn dưới 7 ngày.

Khi kích hoạt, hệ thống sẽ tăng tần suất xuất hiện của các Flashcard để người dùng có thể ôn tập nhiều lần trong thời gian ngắn.

---

## 2.3 Thiết kế Red Zone

### Mô tả

Red Zone là trạng thái giao diện đặc biệt dành cho giai đoạn nước rút trước kỳ thi. Giao diện sử dụng các màu sắc mang tính cảnh báo nhằm nhấn mạnh áp lực thời gian và tăng khả năng tập trung.

### Banner cảnh báo

```text
┌─────────────────────────────────┐
│ 🚨 RED ZONE ACTIVATED           │
│ Kỳ thi còn 5 ngày               │
└─────────────────────────────────┘
```

Banner được đặt ở đầu màn hình và luôn hiển thị trong suốt quá trình sử dụng Cram Mode.

---

## 2.4 Thay đổi màu sắc giao diện

### Study Mode

* Màu chủ đạo: Xanh dương
* Nền sáng, tạo cảm giác thoải mái
* Phù hợp cho việc học tập hằng ngày

### Cram Mode

* Màu chủ đạo: Đỏ
* Màu phụ: Cam cảnh báo
* Thanh tiến trình chuyển sang màu đỏ
* Banner Red Zone được hiển thị nổi bật

### Bảng màu đề xuất

| Thành phần     | Mã màu  |
| -------------- | ------- |
| Danger Red     | #DC2626 |
| Dark Red       | #991B1B |
| Warning Orange | #F97316 |
| Background     | #FFF5F5 |

---

## 2.5 Hệ thống cảnh báo

### Đếm ngược đến kỳ thi

Hiển thị thời gian còn lại để giúp người dùng quản lý việc ôn tập.

```text
🔥 Còn 5 ngày 12 giờ đến kỳ thi
```

### Cảnh báo số lượng thẻ cần ôn tập

```text
⚠ 35 thẻ cần ôn lại
⚠ 12 thẻ chưa ghi nhớ tốt
```

### Thông báo kích hoạt chế độ

```text
🚨 Chế độ Ôn thi Cấp tốc đang hoạt động
Chu kỳ ôn tập đã được tăng cường.
```

---

## 2.6 Bố cục giao diện

```text
┌─────────────────────────────────┐
│ 🚨 RED ZONE                     │
│ Còn 5 ngày đến kỳ thi           │
├─────────────────────────────────┤
│                                 │
│          FLASHCARD              │
│                                 │
├─────────────────────────────────┤
│ ⚠ 35 thẻ cần ôn lại             │
├─────────────────────────────────┤
│ [Quên] [Khó] [Tốt] [Dễ]         │
└─────────────────────────────────┘
```

---

## 2.7 Nguyên tắc thiết kế

* Tạo cảm giác khẩn cấp nhưng không gây áp lực quá mức.
* Sử dụng màu sắc cảnh báo để thu hút sự chú ý.
* Hiển thị rõ thời gian còn lại trước kỳ thi.
* Nhấn mạnh các nội dung cần ôn tập.
* Giữ nguyên trải nghiệm Flashcard của Study Mode để người dùng không cần làm quen lại giao diện.

Thiết kế Cram Mode giúp người dùng nhận biết mình đang ở giai đoạn ôn thi cấp tốc, từ đó tăng mức độ tập trung và tối ưu hiệu quả ôn tập trong thời gian ngắn.
