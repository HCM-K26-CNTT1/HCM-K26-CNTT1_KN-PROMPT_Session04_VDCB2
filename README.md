# **BÀI TẬP: KHẮC PHỤC LỖI KHAI BÁO BIẾN SỐ TRONG PROMPT MẪU**

## **1. Phân tích lỗi**

Prompt cũ sử dụng hai cách khai báo biến không thống nhất: `[language]` và `{audience}`.

- **Khó nhận diện:** AI có thể nhầm lẫn giữa biến cần thay thế và nội dung thông thường.
- **Khó tự động hóa:** Hệ thống khó xác định chính xác vị trí cần truyền dữ liệu.
- **Khó bảo trì:** Khi mở rộng prompt, việc sử dụng nhiều quy ước khác nhau dễ gây nhầm lẫn và sai sót.

## **2. Prompt đã đồng bộ biến số**

Quy ước sử dụng biến: `[NGÔN_NGỮ]` và `[ĐỐI_TƯỢNG]`.

**Prompt sau khi sửa:**

```
Hãy viết một bài chia sẻ về chủ đề
"Kỹ thuật Prompting Nâng cao (Logic & Chuỗi)"
bằng ngôn ngữ [NGÔN_NGỮ].

Nội dung dành cho đối tượng [ĐỐI_TƯỢNG].

Yêu cầu:
- Ngôn ngữ dễ hiểu, phù hợp đối tượng.
- Nội dung ngắn gọn, rõ ràng.
- Có ví dụ minh họa thực tế.
- Trình bày theo từng ý chính.
```

## **3. Kết quả chạy thử**

**Dữ liệu thay thế biến:**

- `[NGÔN_NGỮ]` = Tiếng Việt.
- `[ĐỐI_TƯỢNG]` = Sinh viên năm nhất ngành CNTT.

**Kết quả AI phản hồi:**

**Kỹ thuật Prompting Nâng cao (Logic & Chuỗi)**

Prompting nâng cao giúp AI xử lý yêu cầu phức tạp thông qua hai kỹ thuật chính:

- **Chain-of-Thought:** Giúp AI phân tích vấn đề theo từng bước logic trước khi đưa ra kết quả.
- **Prompt Chaining:** Chia nhiệm vụ lớn thành nhiều prompt nhỏ, sử dụng kết quả bước trước làm đầu vào cho bước sau.

**Ví dụ:** Khi giải bài toán lập trình, AI có thể phân tích yêu cầu, xác định thuật toán rồi mới đề xuất code.

## **4. Kết luận**

Đồng bộ biến số giúp prompt có cấu trúc nhất quán, dễ thay thế dữ liệu và thuận tiện tự động hóa. Sử dụng `[NGÔN_NGỮ]`, `[ĐỐI_TƯỢNG]` viết hoa rõ ràng giúp hạn chế nhầm lẫn khi tái sử dụng prompt.
