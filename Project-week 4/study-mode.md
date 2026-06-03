# 1. Thiết kế Không gian Ôn tập (Study Mode UI)

## 1.1 Mục tiêu

Study Mode là giao diện học tập cốt lõi của ứng dụng, được xây dựng dựa trên phương pháp **Active Recall (Ghi nhớ chủ động)**. Mục tiêu của giao diện là tạo ra một môi trường học tập tập trung cao độ, giúp người dùng chủ động nhớ lại kiến thức trước khi xem đáp án và tự đánh giá mức độ ghi nhớ sau mỗi lần ôn tập.

---

## 1.2 Thiết kế màn hình học Flashcard

### Mô tả chức năng

Khu vực trung tâm của màn hình là **Flashcard**, nơi hiển thị nội dung câu hỏi hoặc đáp án. Người dùng sẽ đọc câu hỏi, suy nghĩ và cố gắng nhớ lại kiến thức trước khi nhấn nút **Lật thẻ** để xem đáp án. Sau khi xem đáp án, người dùng tự đánh giá khả năng ghi nhớ của mình thông qua các nút đánh giá được bố trí phía dưới.

### Bố cục giao diện

```text
┌─────────────────────────────────┐
│ Card 15/50            25 phút   │
├─────────────────────────────────┤
│                                 │
│                                 │
│            CÂU HỎI              │
│                                 │
│         Giải tích là gì?        │
│                                 │
│                                 │
├─────────────────────────────────┤
│            Lật thẻ              │
└─────────────────────────────────┘
```

Sau khi lật thẻ:

```text
┌─────────────────────────────────┐
│            ĐÁP ÁN               │
│                                 │
│ Giải tích là một phân nhánh     │
│ của toán học, chuyên nghiên cứu │
│ về sự thay đổi, tốc độ biến     │
│ thiên và các quá trình liên tục.│
└─────────────────────────────────┘

[ Quên ] [ Khó ] [ Tốt ] [ Dễ ]

                           [ NEXT ]
```

### Ý nghĩa các nút đánh giá

| Nút  | Ý nghĩa                 |
| ---- | ----------------------- |
| Quên | Không nhớ được nội dung |
| Khó  | Chỉ nhớ được một phần   |
| Tốt  | Ghi nhớ tương đối tốt   |
| Dễ   | Đã ghi nhớ và hiểu rõ   |

---

## 1.3 Nguyên tắc thiết kế

### Bố cục tập trung cao độ

Giao diện được thiết kế theo nguyên tắc tối giản nhằm giảm thiểu sự phân tâm trong quá trình học tập.

* Flashcard chiếm phần lớn diện tích màn hình.
* Hạn chế các menu và chức năng phụ không cần thiết.
* Giảm thiểu các yếu tố gây nhiễu thị giác.
* Tập trung sự chú ý của người dùng vào các thành phần chính:

  * Câu hỏi
  * Đáp án
  * Các nút đánh giá mức độ ghi nhớ

Thiết kế này giúp người dùng tập trung hoàn toàn vào quá trình ghi nhớ và tự đánh giá kiến thức, phù hợp với phương pháp học tập Active Recall.
