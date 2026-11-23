# Tự đánh giá — Pham Anh Tuan · G07

## 1. Tự rà soát 4 cảnh

| Ảnh | Đối tượng | Loại lỗi | Ghi chú | Đã sửa? |
|---|---|---|---|---|
| S04_rgb | infant_seat | wrong_class | Tôi đã đổi carrier bên trái ảnh từ child_seat sang infant_seat; ghế lớn bên phải vẫn là child_seat | Có |
| S08_rgb | person, face | attribute | Tôi giữ nhãn người lớn, sửa seatbelt=not_worn và glasses=none; occupant trẻ em và ghế có người không được gán theo GUIDE §3 | Có |
| D01 | face, face13 | box, flag | Tôi mở rộng box mặt để bao phủ phần mặt nhìn thấy; mắt giữ unknown và các điểm mắt occluded do phản xạ NIR | Có |
| D03 | face, face13 | flag, attribute | Tôi đánh dấu điểm miệng/môi bị chai che là occluded và đặt trạng thái mắt open theo ảnh | Có |

## 2. Lỗi lặp lại trong quá trình gán nhãn

Tôi để seatbelt=unknown ở một số khung hình dù dây an toàn nhìn thấy được, đồng thời nhầm carrier ở S04 thành child_seat. Nguyên nhân là lượt rà soát đầu chưa đối chiếu đầy đủ từng thuộc tính với ảnh gốc và chưa phân biệt rõ hình dáng hai loại ghế. Tôi đã sửa các nhãn này trên CVAT và cập nhật export cuối.

## 3. Kết quả đối chiếu với Nguyen Thanh Phong

Tôi xử lý 56 điểm khác biệt trong disagreement_log.csv. Tôi áp dụng các bất đồng được ảnh và guideline hỗ trợ, gồm loại ghế S04 và trạng thái dây an toàn. Tôi giữ các ca còn mơ hồ ở D04/D06 để coach xác nhận. Các nhãn người/ghế liên quan đến hình dáng trẻ em ở S01/S03/S05/S08 được xử lý theo GUIDE §3 và ghi rõ trong log.
