# Báo cáo kiểm thử hiệu năng bằng JMeter

## Thông tin sinh viên

- Họ tên: Phạm Gia Nam
- MSSV: BIT220114
- Website được kiểm thử: https://www.example.com

## Mô tả kịch bản kiểm thử

1. **Kịch bản 1: Cơ bản**

   - Users: 14
   - Hành vi: Gửi yêu cầu GET đến https://www.example.com
   - Loop Count: 5 lần

2. **Kịch bản 2: Tải nặng**

   - User: 64
   - Ramp-up Period: 30 giây
   - Hành vi: GET đến https://www.example.com và trang https://www.example.com/index.html

3. **Kịch bản 3: Tùy chỉnh**
   - User: 34
   - Duration: 60 giây
   - Hành vi: GET đến https://www.example.com và trang https://www.example.com/index.html

> **Lưu ý**: Website `https://www.example.com` là một tên miền mẫu được IANA cấp cho mục đích minh họa và không có nội dung thực tế hay trang con cụ thể. Các URL như `/index.html` được thêm vào nhằm mô phỏng tình huống kiểm thử.

## Kết quả kiểm thử

### Kịch bản 1: Cơ bản

- Response Time trung bình: 58 ms
- Throughput: 59,42 requests/sec
- Error Rate: 0,000%

### Kịch bản 2: Tải nặng

- Response Time trung bình: 69 ms
- Throughput: 4,31 requests/sec
- Error Rate: 0,000%

### Kịch bản 3: Tùy chỉnh

- Response Time trung bình: 31 ms
- Throughput: 1047,62 requests/sec
- Error Rate: 0,000%

## Nhận xét

- Website phản hồi nhanh và ổn định ở kịch bản cơ bản.
- Trong kịch bản tải nặng, độ trễ tăng lên đáng kể do số lượng người dùng cao và ramp-up nhanh.
- Kịch bản tùy chỉnh cho thấy hệ thống vẫn duy trì throughput cao và không xuất hiện lỗi.
- Website chịu tải tốt trong môi trường mô phỏng, tuy nhiên do giới hạn nội dung của tên miền `example.com`, kết quả chỉ mang tính tham khảo.
