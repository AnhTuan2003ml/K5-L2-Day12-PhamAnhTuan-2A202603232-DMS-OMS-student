# Danh sách lớp v0 — Pham Anh Tuan · G07

Bản nháp này tổng hợp các lớp cần cho bài toán DMS và OMS trong bộ G07, cùng mục đích sử dụng và mức độ quan sát trên ảnh IR.

## DMS

| # | Lớp / thuộc tính | Giá trị | Mục đích sử dụng | Quan sát trên IR |
|---|---|---|---|---|
| 1 | person | seat=driver; seatbelt=worn_correct/worn_incorrect/not_worn/unknown | Vùng cơ thể tài xế và trạng thái dây an toàn | Hình thể thường còn; màu áo không còn tin cậy trên NIR |
| 2 | face | eye_left/eye_right; glasses; gaze_zone | Trạng thái mắt, kính và vùng nhìn của tài xế | Mặt thường thấy; phản xạ kính có thể làm mất chi tiết mắt |
| 3 | face13 | 13 điểm mốc; occluded/outside | Hình học khuôn mặt và mức tin cậy của từng landmark | Dùng được khi mặt đủ lớn; phản xạ hoặc vật che ảnh hưởng từng điểm |
| 4 | hand | whose; side; on_wheel | Vị trí tay và mức tiếp xúc với vô lăng | Hình dạng tay thấy được nếu không bị che; trái/phải xác định theo người |
| 5 | phone | held/mounted/lap | Sự hiện diện và trạng thái sử dụng điện thoại | Hình dáng thiết bị có thể nhận ra; vật khác gần tai dễ gây nhầm |
| 6 | eye_state | open/closed/unknown | Theo dõi trạng thái mắt làm đầu vào cho phân tích buồn ngủ | Có thể bị kính, phản xạ NIR hoặc góc mặt che khuất |

## OMS

| # | Lớp / thuộc tính | Giá trị | Mục đích sử dụng | Quan sát trên IR |
|---|---|---|---|---|
| 1 | person | seat=rear_left/rear_middle/rear_right; seatbelt | Số người và vị trí ghế trong cabin | Hình thể còn nhận biết; màu trang phục mất |
| 2 | face | bounding box khuôn mặt người lớn | Liên kết vùng mặt với người ngồi và đánh giá khả năng quan sát | Thấy khi đủ sáng và đủ kích thước |
| 3 | child_seat | seat; occupied=no/unknown | Nhận biết ghế trẻ em trống | Đường viền còn thấy; màu vật liệu thay đổi |
| 4 | infant_seat | seat; facing=rear/front | Nhận biết carrier và hướng đặt | Hình dáng, tay cầm thường còn nhận ra |
| 5 | object | seat; type=bag/box/cup/other | Nhận biết đồ vật trong cabin và vị trí của chúng | Hình khối thường còn; màu/chất liệu giảm tin cậy |
| 6 | frame_meta | modality=rgb/ir; light; camera_blocked | Ghi modality và điều kiện ảnh để phân tích dữ liệu | Modality xác định theo nguồn; IR-sim và real_IR được tách riêng |

## Các câu hỏi tôi ghi nhận để coach xác nhận

1. Với người có hình dáng trẻ em trong S01, S03, S05 và S08, tôi áp dụng GUIDE §3 và không gán người/ghế đang có người. Coach xác nhận quy tắc này có tiếp tục áp dụng khi nhãn OMS yêu cầu nhận diện mọi occupant không? Ví dụ: S08_rgb có một người lớn và một occupant nhỏ trong ghế bên trái ảnh.

2. Ở D04 và D06, hai bản annotation đặt hộp tay khác nhau; D04 còn khác trạng thái mắt và vùng nhìn. Coach xác nhận vị trí hộp tay theo từng bàn tay và cách phân loại mắt trong ảnh NIR xoay? Ví dụ: D04.png có hai hộp tay không trùng nhau trong bản của tôi, còn peer có hai hộp chồng lấn.
