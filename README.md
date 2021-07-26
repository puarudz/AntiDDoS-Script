# AntiDDoS-Script

Chúng tôi muốn giới thiệu đến các bạn một giải pháp khẩn cấp tạm thời, dựa vào Iptables để có thể ngăn chặn ngay các cuộc tấn công trên.

Trước tiên stop và tạo các rules mới cho Iptables:
```
service apf stop
iptables -F
```
Sau đó tải về và chạy file script để cấu hình các rules chống lại tấn công DOS/DDOS:

```
wget https://raw.githubusercontent.com/puarudz/AntiDDoS-Script/main/anti-ddos.sh
chmod u+x anti-ddos.sh
./anti-ddos.sh
```
Đây là đọan mã do tác giả *Ruslan Abuzant ruslan@abuzant.com* biên soạn, phiên bản 2.0 phát hành theo giấy phép GNU GPL. Điều đó có nghĩa là bạn hoàn toàn có thể soạn lại các nội dung rules trong script để cho phù hợp với thực tế máy chủ bạn gặp phải.

Ngoài ra, bạn có thể dùng các lệnh sau để thống kê các cuộc tấn công, rất hữu ích:
```
netstat -antp | grep ESTABLISHED
netstat -antp | grep -i sync
netstat --help
```
