---
layout: post
title: Tạo máy chủ kali linux để lưu trữ file
categories: general tutorial
---
Network adapter: bridged

Cài đặt Apache:
```
sudo apt update
```
```
sudo apt install apache2
```
Khởi động và kích hoạt Apache:
```
sudo systemctl start apache2
```
```
sudo systemctl enable apache2
```

Kiểm tra dịch vụ Apache đã được kích hoạt chưa:
```
Sudo service apache2 status
```
Nếu chưa sẽ hiển thị: `inactive(dead)`<br/>
Kích hoạt lại dịch vụ apche2:
```
Sudo service apache2 start
```

Kiểm tra ip kali linux: `ifconfig`

Truy cập server từ windows bằng cách nhập ip kali linux

Đưa file lên server:
```
sudo mv /home/user/file /var/www/html/
```

Cho phép file tải về:
```
sudo chmod o+r /var/www/html/file
```

tải nội dung file về winfows:
```
curl http://địa_chỉ_IP_của_máy_Kali_Linux/file
```
