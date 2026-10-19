# Requirements

## 1. Functional requirements (bắt buộc)
- FR1: ESP32 đọc nhiệt độ và độ ẩm từ cảm biến theo chu kỳ cố định (ví dụ 5 giây).
- FR2: ESP32 kết nối Wi-Fi và publish dữ liệu dạng JSON qua MQTT.
- FR3: Mosquitto broker chạy local, nhận và phân phối message theo topic.
- FR4: Backend Python subscribe topic, kiểm tra dữ liệu hợp lệ và lưu vào database kèm timestamp.
- FR5: Dashboard hiển thị giá trị hiện tại và biểu đồ lịch sử.
- FR6: Hệ thống xử lý được message lỗi và tự kết nối lại khi mất kết nối.

## 2. Performance requirements (đo ở tuần 7)
- PR1: Đo độ trễ từ lúc ESP32 gửi đến lúc backend nhận.
- PR2: Đo tỉ lệ message gửi thành công trong một khoảng thời gian test.
- PR3: Kiểm tra hành vi khi mất Wi-Fi hoặc khởi động lại server.
- PR4: Kiểm tra ảnh hưởng khi có thêm publisher giả lập.

## 3. Constraints
- Chạy hoàn toàn local, không dùng cloud.
- Backend viết bằng Python.

## 4. Optional extensions (chỉ làm khi hệ thống chính đã chạy)
- Nhiều thiết bị, MQTT authentication/TLS, cảnh báo theo ngưỡng, so sánh QoS.