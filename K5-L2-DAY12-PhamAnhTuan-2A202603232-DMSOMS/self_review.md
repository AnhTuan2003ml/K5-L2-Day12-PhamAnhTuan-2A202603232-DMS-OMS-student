# Tự đánh giá — Pham Anh Tuan · G07

## 1. Tự rà soát 4 cảnh

| Ảnh | Đối tượng | Loại lỗi | Ghi chú | Đã sửa? |
|---|---|---|---|---|
| S04_rgb | infant_seat | wrong_class | Tôi đổi carrier bên trái ảnh từ child_seat sang infant_seat; ghế lớn bên phải giữ là child_seat | Có |
| S02_rgb, S02_ir | face, person | extra, attribute | Tôi bỏ face box vì chỉ thấy tóc/sau đầu; dây an toàn S02_ir chuyển thành unknown vì vùng dây không rõ | Có |
| D01 | face, face13 | box, flag | Tôi mở rộng box mặt; mắt giữ unknown và các điểm mắt occluded do phản xạ NIR | Có |
| D03 | face, face13 | flag, attribute | Tôi đánh dấu điểm miệng/môi bị chai che là occluded và đặt trạng thái mắt open theo ảnh | Có |

## 2. Lỗi lặp lại trong quá trình gán nhãn

Tôi để seatbelt=unknown ở một số khung có dây nhìn thấy được, gán face box ở S02 dù chỉ thấy tóc/sau đầu, và nhầm loại carrier ở S04. Nguyên nhân là lượt rà soát đầu chưa đối chiếu từng thuộc tính, góc mặt và hình dáng ghế với GUIDE. Tôi đã sửa các nhãn trên CVAT và cập nhật export_final.zip.

## 3. Kết quả đối chiếu với Nguyen Thanh Phong

Tôi đối chiếu 56 dòng trong disagreement_log.csv với export và disagreement_log của Phong. Tôi áp dụng các kết luận có căn cứ như mắt unknown/occluded ở D01, bỏ face S02, seatbelt unknown ở S02_ir và phân loại carrier S04. Tôi không thêm infant_seat ở S03/S05 vì GUIDE định nghĩa lớp này cho ghế em bé trống; ảnh đang có occupant. Các ca trẻ em ở S01/S05/S08, kính D04 và box tay D04/D06 được giữ ở trạng thái mơ hồ để coach xác nhận.
