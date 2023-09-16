Rustscan là một tool có thể scan tất cả các port với tốc độ ánh séng rồi dẫn output nmap <br>
Cú pháp:

      rustscan -r <ports> -a <target_ip> -- <nmap cmds>
Dưới đây sẽ là một số cách sử dụng:<br>
# Multiple IP Scanning
Ta có thể scan nhiều IP cũng lúc bằng dấu ```,``` như này

      rustscan -a 127.0.0.1,0.0.0.0
# Host Scanning
Rustscan cũng thế scan host:

      rustscan -a www.google.com, 127.0.0.1

# Hỗ trợ CIDR (định tuyến tên miền không phân lớp)
      rustscan -a 192.168.0.0/30
Như câu lệnh, nó có thể quét nguyên một dải mạng

# Hosts file as input
Hiểu đơn giản là nó thể quét một file chứa IP bên trong

      rustscan -a 'host.txt'

# Individuel Port Scanning
      rustscan -a 127.0.0.1 -p 53

# Multiple selected port scanning
      rustscan -a 127.0.0.1 -p 53,80,121,65535

# Ranges of port
      rustscan -a 127.0.0.1 --range 1-1000

# Adjusting the Nmap arguments
Rust có thể dùng các option của nmap bằng cách điền nó sau --
VD:

      nmap -Pn -vvv -p $PORTS -A -sC 127.0.0.1
Sẽ tương tự với

      rustscan -a 127.0.0.1 -- -A -sC

# Random Port Ordering
Nếu muốn scan ports với thứ tự random (mặc dù tôi cũng chả hiểu tại sao phải làm như này :|| có vẻ làm vậy đỡ bị detect):

      rustscan -a 127.0.0.1 --range 1-1000 --scan-order "Random"

# Conclusion
Tool này ngon vđ mà giới mới biết :|| có lẽ tôi sẽ dùng tool này thay nmap luôn
