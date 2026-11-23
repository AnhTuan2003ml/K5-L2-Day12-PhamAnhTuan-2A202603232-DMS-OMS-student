# Khai báo sử dụng AI — Pham Anh Tuan · G07

| # | Công cụ | Nội dung tôi yêu cầu | Cách tôi sử dụng kết quả | Cách tôi kiểm chứng |
|---|---|---|---|---|
| 1 | CVAT Agent và SAM3 chạy cục bộ trong Docker | Tạo prelabel cho các lớp đã chọn của task G07 | Tôi dùng dự đoán làm bản nháp, sau đó bỏ các shape sai lớp/sai dạng và sửa theo phạm vi OMS/DMS | Tôi xem lại ảnh và annotation, đối chiếu GUIDE, chạy cabin_check ở A, B và final |
| 2 | ChatGPT/Codex | Đọc yêu cầu, phân tích khác biệt với peer, rà báo cáo và hỗ trợ chỉnh annotation | Tôi dùng kết quả như nhận xét cần kiểm chứng; kết luận cuối cùng dựa trên ảnh gốc, GUIDE và CVAT | Tôi đọc lại các điểm khác, cập nhật CVAT, đọc ngược dữ liệu và chạy cabin_check |

## Phạm vi xử lý ảnh

SAM3 được chạy cục bộ trên Docker để tạo prelabel. Trong phiên rà soát này, ảnh G07 cũng được mở để đối chiếu bằng công cụ xem ảnh của Codex. Việc sử dụng AI với ảnh cabin/tài xế được ghi nhận để coach xem xét theo quy định dữ liệu của GUIDE.
