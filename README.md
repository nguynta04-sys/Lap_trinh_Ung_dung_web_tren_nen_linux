# Lap_trinh_Ung_dung_web_tren_nen_linux
## Môn Phát triển ứng dụng trên nền web 
## Bài Làm:


- Em chọn cài đặt:
 - enable wsl: cài đặt docker desktop
 - enable wsl: cài đặt ubuntu
<img width="1920" height="1080" alt="Screenshot (40)" src="https://github.com/user-attachments/assets/0eb7e9ca-66f6-4528-98ba-47de13ab6385" />

- Sau đó em cài tiếp Ubuntu:
<img width="1920" height="1080" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/46d0fe6d-5002-43f4-b031-7f3e0ae2f2d2" />

- Đây là giao diện khi tải Docker Desktop, nhưng chưa có gì cả
<img width="1920" height="1080" alt="Screenshot (42)" src="https://github.com/user-attachments/assets/558dea70-a6c3-4041-a184-1ef2cedc5218" />

- Cài Ubuntu và đặt tên User và password
<img width="1920" height="1080" alt="Screenshot (43)" src="https://github.com/user-attachments/assets/5407cd27-2618-4bd7-91dc-4efcb375f4d3" />

- Ở bước này em cài đặt các containers (grafana, nodered, nginx, phpmyadmin, mariadb, influxdb.) 
<img width="1920" height="1080" alt="Screenshot (44)" src="https://github.com/user-attachments/assets/92b1bdc8-75d9-494f-b1b5-3ad65a2dff17" />

- Em đã cài đặt thành công các containers (grafana, nodered, nginx, phpmyadmin, mariadb, influxdb.) ở trong docker desktop 
<img width="1920" height="1080" alt="Screenshot (46)" src="https://github.com/user-attachments/assets/def3930d-7d83-43c2-bcde-1cb792b2cb51" />

- Em tạo thêm 1 file .html chỉ để test nginx.
<img width="1309" height="905" alt="image" src="https://github.com/user-attachments/assets/ab5d23e0-6b14-4588-bed1-7c5c03cbee92" />

- Đây là kết quả test:
<img width="1920" height="1080" alt="Screenshot (52)" src="https://github.com/user-attachments/assets/93719c34-8987-47eb-b6c2-92b86003227b" />

- Em truy cập phpMyAdmin tại: http://localhost:8080, vào cơ sở dữ liệu mới iot_db
<img width="1920" height="1080" alt="Screenshot (48)" src="https://github.com/user-attachments/assets/9c96aaa8-ee40-4090-8a41-455ce9b3f63f" />

- Em đã tạo thành công database nhé
<img width="1920" height="1080" alt="Screenshot (49)" src="https://github.com/user-attachments/assets/45786838-1c97-470d-b128-79148667cde4" />

- Em truy cập Node-RED tại: http://localhost:1880, và có giao diện như này
<img width="1920" height="1080" alt="Screenshot (53)" src="https://github.com/user-attachments/assets/5770c765-befc-42d0-be0d-a7a8f4a2d4ed" />

- Em install 2 cái sau:
node-red-contrib-influxdb (Để kết nối với InfluxDB)
node-red-contrib-bcrypt (Để kiểm tra mật khẩu login)
<img width="1087" height="463" alt="image" src="https://github.com/user-attachments/assets/fc2717a4-2a1b-4d52-a5cf-8edb76c72468" />

- Em Import Flow mô phỏng dữ liệu:
- Tôi đã tạo sẵn một flow (luồng) cơ bản. Flow này sẽ:

Mô phỏng: Cứ 3 giây, tự tạo ra giá trị nhiệt độ, độ ẩm.

Lưu vào MariaDB: Cập nhật giá trị mới nhất vào bảng latest_sensor_data.

Lưu vào InfluxDB: Ghi lại giá trị lịch sử vào InfluxDB (để Grafana vẽ biểu đồ).
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/756e376f-73ae-4326-8feb-a393f0d5c667" />


- Em install thêm node-red-node-mysql 
<img width="681" height="164" alt="image" src="https://github.com/user-attachments/assets/d64a452b-fb7e-4b55-8413-e47589709b2e" />

- Em cấu hình kết nối với MariaDB:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/935b3652-dccd-4768-828b-a2fbca760e63" />


- Em đăng kí và đăng nhập bằng tài khoản admin:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/fae1ebd7-963a-4478-ad0a-0188a5f02614" />

- Đây là khi em đăng kí:
<img width="1920" height="1080" alt="Screenshot (60)" src="https://github.com/user-attachments/assets/5be150bb-2cd1-4a6a-8db5-4d862450c20a" />

- Khi đăng kí thành công sẽ nhảy luôn đến phần đăng nhập:
<img width="1920" height="1080" alt="Screenshot (61)" src="https://github.com/user-attachments/assets/67be2b55-030f-4bb6-ab6d-a1e2be001591" />

- Em đăng nhập thành công:
<img width="1920" height="1080" alt="Screenshot (62)" src="https://github.com/user-attachments/assets/257fe5dd-f022-4e8a-aedc-28fd81a976b3" />








- Tiếp theo em truy cập vào Grafana: http://localhost:3000
<img width="837" height="72" alt="image" src="https://github.com/user-attachments/assets/862a3b34-69f3-4dd0-90e3-7a1a9bf750e0" />

- Em đăng nhập vào Grafana
<img width="1920" height="1080" alt="Screenshot (56)" src="https://github.com/user-attachments/assets/c1ae42e4-1521-4a27-b0a6-0359e78d441c" />

- Em đã đăng nhập vào được Grafana
<img width="1920" height="1080" alt="Screenshot (57)" src="https://github.com/user-attachments/assets/bf9ab430-2807-4000-9b8f-98f88376f269" />

- Sau khi em đăng nhập vào được Grafana -> connections -> data sources -> influxdb:
<img width="1920" height="1080" alt="Screenshot (58)" src="https://github.com/user-attachments/assets/23a9a99a-94c3-42d3-b62f-4c9c415270af" />
<img width="1920" height="1080" alt="Screenshot (59)" src="https://github.com/user-attachments/assets/a586e9a5-7569-4df2-95a4-4805669da668" />

## Vấn Đề

- Phân Tách Dữ Liệu Chức Năng (MariaDB vs. InfluxDB): hiểu được sự khác biệt cốt lõi giữa hai loại cơ sở dữ liệu. MariaDB được dùng cho dữ liệu có cấu trúc, ít thay đổi (tài khoản người dùng) và dữ liệu trạng thái mới nhất (latest state) cần truy cập nhanh cho Dashboard SPA. Ngược lại, InfluxDB được dành riêng cho dữ liệu chuỗi thời gian (time-series) khổng lồ và liên tục, tối ưu hóa cho việc truy vấn lịch sử và vẽ biểu đồ hiệu suất cao bởi Grafana.

- Node-RED như Tầng Middleware Linh hoạt: sử dụng Node-RED không chỉ là công cụ đọc cảm biến mà còn là tầng logic nghiệp vụ trung tâm (Middleware). Node-RED chịu trách nhiệm xử lý các tác vụ phức tạp như:

  + Xác thực và mã hóa: Thực hiện logic Đăng ký/Đăng nhập (dùng SHA256) và tạo Session Token an toàn.

  + Định tuyến Dữ liệu: Đồng thời gửi dữ liệu đến cả hai loại Database (MariaDB cho trạng thái hiện tại, InfluxDB cho lịch sử).

- Triển khai SPA qua Reverse Proxy Nginx: Việc cấu hình Nginx để hoạt động như một Cổng (Gateway) duy nhất cho phép truy cập tất cả các dịch vụ (Frontend, Node-RED, Grafana) qua cùng một domain (http://nguyentuananh.local/). Điều này không chỉ đáp ứng yêu cầu kỹ thuật mà còn thể hiện sự hiểu biết về cách quản lý và định tuyến lưu lượng truy cập trong môi trường Microservice.

- Tính toàn vẹn (End-to-End Logic): Toàn bộ chuỗi vận hành được thiết lập: Frontend (SPA) → API (Node-RED) → Data Storage (MariaDB/InfluxDB) → Visualization (Grafana). Đặc biệt, việc sử dụng hàm setInterval để cập nhật dữ liệu Dashboard mỗi 3 giây thể hiện sự hiểu biết về yêu cầu giám sát thời gian thực của ứng dụng IOT.


