# Nslookup
- Tìm địa chỉ IP của domain bằng nslookup (Name server lookup)
- Bạn cần dùng lệnh ```nslookup <DOMAIN_NAME>```, hoặc có thể chi tiết hơn bằng ```nslookup OPTIONS DOMAIN_NAME SERVER```
  - OPTION gồm cái định dạng sẽ được hiển thị ở bảng. Ta có thể dùng ```A``` cho IPv4 và ```AAAA``` cho IPv6
    - ![image](https://github.com/Myozz/THM/assets/94811005/e6fe0320-19f6-4cd3-84cd-2f486c72242a)

  - DOMAIN_NAME thì là tên miền
  - SERVER là DNS server mà ta muốn truy vấn. Bạn có thể chọn local hay public DNS để truy vấn (hay dùng các DNS của Google, CLoudflare, Quad9)
    
