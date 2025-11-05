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

Mô phỏng: Cứ 5 giây, tự tạo ra giá trị nhiệt độ, độ ẩm ngẫu nhiên.

Lưu vào MariaDB: Cập nhật giá trị mới nhất vào bảng latest_sensor_data.

Lưu vào InfluxDB: Ghi lại giá trị lịch sử vào InfluxDB (để Grafana vẽ biểu đồ).
<img width="1920" height="1080" alt="Screenshot (50)" src="https://github.com/user-attachments/assets/612160de-5666-433c-9576-6f5542d7b98e" />

- Em install thêm node-red-node-mysql 
<img width="681" height="164" alt="image" src="https://github.com/user-attachments/assets/d64a452b-fb7e-4b55-8413-e47589709b2e" />

- Em cấu hình kết nối với MariaDB:
<img width="1920" height="1080" alt="Screenshot (51)" src="https://github.com/user-attachments/assets/6a550cf0-9d31-49ce-bc92-33a34530fa7a" />

- Em kiểm tra dữ liệu mới nhất trong MariaDB
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ab110ab6-8009-467f-a469-2c5ac30ea962" />

- Tiếp theo em truy cập vào Grafana: http://localhost:3000
<img width="837" height="72" alt="image" src="https://github.com/user-attachments/assets/862a3b34-69f3-4dd0-90e3-7a1a9bf750e0" />

- Em đăng nhập vào Grafana
<img width="1920" height="1080" alt="Screenshot (56)" src="https://github.com/user-attachments/assets/c1ae42e4-1521-4a27-b0a6-0359e78d441c" />

- Em đã đăng nhập vào được Grafana
<img width="1920" height="1080" alt="Screenshot (57)" src="https://github.com/user-attachments/assets/bf9ab430-2807-4000-9b8f-98f88376f269" />

- Sau khi em đăng nhập vào được Grafana -> connections -> data sources -> influxdb:
<img width="1920" height="1080" alt="Screenshot (58)" src="https://github.com/user-attachments/assets/23a9a99a-94c3-42d3-b62f-4c9c415270af" />
<img width="1920" height="1080" alt="Screenshot (59)" src="https://github.com/user-attachments/assets/a586e9a5-7569-4df2-95a4-4805669da668" />





