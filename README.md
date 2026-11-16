# HCM-KS26-CNTT1_KNPromtingAl_Session03_BTTH5
# BÀI THỰC HÀNH 5: PHÂN LOẠI PHẢN HỒI CỦA KHÁCH HÀNG

**Họ và tên:** Phạm Thành Đạo  
**Lớp:** HCM-KS26-CNTT1

## 1. Mục tiêu

Sử dụng hai kỹ thuật Prompt Engineering là Zero-shot và Few-shot để phân loại phản hồi của khách hàng trên Facebook thành ba nhóm: Tích cực, Tiêu cực và Yêu cầu hỗ trợ.

Qua đó, so sánh kết quả của hai phương pháp về độ chính xác và tính nhất quán.

## 2. Prompt 1: Sử dụng kỹ thuật Zero-shot

### Nội dung Prompt

Bạn là nhân viên chăm sóc khách hàng của một cửa hàng bán đồ công nghệ. Hãy phân loại các phản hồi của khách hàng thành một trong ba nhãn sau:

- **Tích cực:** Khách hàng hài lòng, khen ngợi sản phẩm hoặc dịch vụ.
- **Tiêu cực:** Khách hàng phàn nàn, thể hiện sự không hài lòng.
- **Yêu cầu hỗ trợ:** Khách hàng gặp vấn đề cụ thể và cần cửa hàng kiểm tra hoặc giải quyết.

**Quy tắc phân loại:** Nếu phản hồi đề cập đến một vấn đề cụ thể cần cửa hàng can thiệp hoặc giải quyết, hãy ưu tiên nhãn "Yêu cầu hỗ trợ". Nếu chỉ thể hiện sự không hài lòng mà không có yêu cầu xử lý cụ thể, phân loại là "Tiêu cực".

Hãy phân loại 5 phản hồi sau:

1. "Sản phẩm đẹp, giao hàng nhanh, rất hài lòng."
2. "Tôi đã đặt hàng 5 ngày nhưng chưa nhận được."
3. "Tai nghe không kết nối được Bluetooth."
4. "Nhân viên tư vấn rất nhiệt tình."
5. "Tôi muốn hoàn tiền vì sản phẩm bị lỗi."

Yêu cầu đầu ra: Trình bày dưới dạng bảng Markdown gồm các cột STT, Phản hồi, Nhãn phân loại và Lý do. Không thêm nội dung ngoài bảng.

### Kết quả Prompt 1

| STT | Phản hồi | Nhãn phân loại | Lý do |
|---|---|---|---|
| 1 | Sản phẩm đẹp, giao hàng nhanh, rất hài lòng. | Tích cực | Khách hàng khen sản phẩm và hài lòng với dịch vụ giao hàng. |
| 2 | Tôi đã đặt hàng 5 ngày nhưng chưa nhận được. | Tiêu cực | Khách hàng phàn nàn về việc giao hàng chậm. |
| 3 | Tai nghe không kết nối được Bluetooth. | Yêu cầu hỗ trợ | Sản phẩm gặp lỗi kỹ thuật cần được kiểm tra. |
| 4 | Nhân viên tư vấn rất nhiệt tình. | Tích cực | Khách hàng đánh giá tốt thái độ phục vụ. |
| 5 | Tôi muốn hoàn tiền vì sản phẩm bị lỗi. | Yêu cầu hỗ trợ | Khách hàng đưa ra yêu cầu hoàn tiền cụ thể. |

## 3. Prompt 2: Sử dụng kỹ thuật Few-shot

### Nội dung Prompt

Bạn là nhân viên chăm sóc khách hàng chuyên nghiệp của một cửa hàng bán đồ công nghệ. Nhiệm vụ của bạn là phân loại phản hồi khách hàng thành ba nhóm: Tích cực, Tiêu cực và Yêu cầu hỗ trợ.

Hãy tham khảo các ví dụ sau trước khi thực hiện:

**Ví dụ 1:**

- Phản hồi: "Điện thoại rất đẹp, sử dụng mượt mà, tôi rất thích."
- Nhãn: Tích cực.
- Lý do: Khách hàng hài lòng và khen ngợi sản phẩm.

**Ví dụ 2:**

- Phản hồi: "Tôi phải chờ quá lâu nhưng đơn hàng vẫn chưa được giao."
- Nhãn: Tiêu cực.
- Lý do: Khách hàng phàn nàn về chất lượng dịch vụ giao hàng.

**Ví dụ 3:**

- Phản hồi: "Máy tính của tôi không khởi động được, cửa hàng có thể hỗ trợ kiểm tra không?"
- Nhãn: Yêu cầu hỗ trợ.
- Lý do: Khách hàng gặp sự cố cụ thể và cần cửa hàng giải quyết.

**Quy tắc phân loại:**

- Tích cực: Khách hàng hài lòng, khen ngợi.
- Tiêu cực: Khách hàng phàn nàn, không hài lòng nhưng không đưa ra yêu cầu xử lý cụ thể.
- Yêu cầu hỗ trợ: Khách hàng gặp vấn đề cụ thể cần cửa hàng kiểm tra, hỗ trợ hoặc giải quyết.
- Nếu phản hồi vừa thể hiện sự không hài lòng vừa yêu cầu xử lý một vấn đề cụ thể, ưu tiên nhãn Yêu cầu hỗ trợ.

**Dữ liệu cần phân loại:**

1. "Sản phẩm đẹp, giao hàng nhanh, rất hài lòng."
2. "Tôi đã đặt hàng 5 ngày nhưng chưa nhận được."
3. "Tai nghe không kết nối được Bluetooth."
4. "Nhân viên tư vấn rất nhiệt tình."
5. "Tôi muốn hoàn tiền vì sản phẩm bị lỗi."

**Yêu cầu đầu ra:** Trình bày bằng bảng Markdown gồm các cột STT, Phản hồi, Nhãn phân loại và Lý do. Đảm bảo cách phân loại nhất quán với các ví dụ mẫu.

### Kết quả Prompt 2

| STT | Phản hồi | Nhãn phân loại | Lý do |
|---|---|---|---|
| 1 | Sản phẩm đẹp, giao hàng nhanh, rất hài lòng. | Tích cực | Khách hàng thể hiện sự hài lòng với sản phẩm và dịch vụ. |
| 2 | Tôi đã đặt hàng 5 ngày nhưng chưa nhận được. | Tiêu cực | Khách hàng phàn nàn về thời gian giao hàng nhưng chưa đưa ra yêu cầu xử lý cụ thể. |
| 3 | Tai nghe không kết nối được Bluetooth. | Yêu cầu hỗ trợ | Tai nghe gặp vấn đề kỹ thuật cần được kiểm tra và khắc phục. |
| 4 | Nhân viên tư vấn rất nhiệt tình. | Tích cực | Khách hàng khen ngợi thái độ phục vụ của nhân viên. |
| 5 | Tôi muốn hoàn tiền vì sản phẩm bị lỗi. | Yêu cầu hỗ trợ | Khách hàng yêu cầu hoàn tiền do sản phẩm bị lỗi. |

## 4. So sánh kết quả Zero-shot và Few-shot

| Tiêu chí | Zero-shot | Few-shot |
|---|---|---|
| Cách hoạt động | Phân loại dựa trên yêu cầu và quy tắc được cung cấp. | Phân loại dựa trên yêu cầu kết hợp các ví dụ mẫu. |
| Số lượng ví dụ | Không cần ví dụ mẫu. | Có ít nhất 3 ví dụ mẫu. |
| Độ chính xác | Có thể phân loại đúng nhưng dễ nhầm lẫn với phản hồi có nhiều ý nghĩa. | Có định hướng rõ hơn nhờ các ví dụ minh họa. |
| Tính nhất quán | Có thể thay đổi cách phân loại khi gặp tình huống tương tự. | Thường nhất quán hơn khi các ví dụ và quy tắc rõ ràng. |
| Ưu điểm | Prompt ngắn gọn, dễ sử dụng, tiết kiệm thời gian chuẩn bị. | Giúp AI hiểu rõ cách phân loại và áp dụng theo mẫu. |
| Hạn chế | AI phải tự diễn giải quy tắc mà không có ví dụ tham khảo. | Cần thời gian xây dựng ví dụ phù hợp, ví dụ không tốt có thể gây sai lệch. |

### Nhận xét

- Cả hai phương pháp đều phân loại được 5 phản hồi theo ba nhóm yêu cầu.
- Zero-shot phù hợp với những nhiệm vụ đơn giản, có quy tắc phân loại rõ ràng.
- Few-shot cung cấp ví dụ cụ thể giúp AI hiểu rõ hơn cách áp dụng từng nhãn, đặc biệt với những phản hồi dễ gây nhầm lẫn.
- Trong bài thực hành này, hai phương pháp cho kết quả giống nhau. Tuy nhiên, Few-shot có lợi thế về tính nhất quán khi xử lý nhiều phản hồi phức tạp hoặc có cách diễn đạt khác nhau.

## 5. Kết luận

Kỹ thuật Zero-shot và Few-shot đều có thể được sử dụng để phân loại phản hồi khách hàng. Zero-shot phù hợp khi cần xử lý nhanh và yêu cầu đơn giản. Trong khi đó, Few-shot phù hợp hơn với những nhiệm vụ cần hướng dẫn cụ thể và duy trì cách phân loại nhất quán. Đối với cửa hàng bán đồ công nghệ, có thể sử dụng Few-shot để hỗ trợ nhân viên phân loại phản hồi và xác định mức độ ưu tiên xử lý.
