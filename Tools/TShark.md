# Giới Thiệu
- Bạn chán việc extract packets bằng tay? Cần lấy thông tin từ một pcap file việc mà WireShark làm như puồi (thực ra tôi chưa dùng wireshark :||)
- Install: ```sudo apt install tshark```

# Đọc PCAP file
- Để độc file với TShark, ta dùng ```-r```. VD: ```tshark -r dns.cap```
- Khi kết hợp với ```wc -l```. ta có thể nhanh chóng xác định được có bao nhiêu packets

      tshark -r dns.cap | wc -l
- Ta có thể sử dụng Wireshark display filters để thu hẹp lại packet được hiển thị. Nếu ta chỉ muốn DNS A record thì có thể dùng ```dns.qry.type == 1``` display filter để thu hẹp packet. Display filter được thêm bởi sử dụng ```-Y```

      tshark -r dns.cap -Y "dns.qry.type == 1"
- Để extract A records trong pcap, ta sử dụng ```-T fields -e dns.qry.name``` ở cuối tshark cmd. Nó giúp extract field nhất định trực tiếp từ pcap

      tshark -r dns.cap -Y "dns.qry.type == 1" -T fields -e dns.qry.name
