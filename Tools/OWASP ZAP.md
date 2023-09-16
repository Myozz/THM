# Giới thiệu
- Là công cụ quét lỗi bảo mật của ứng dụng web, mã nguồn mở tương tự Burp Suite

![image](https://github.com/Myozz/THM_DOC/assets/94811005/840e7fdf-cbda-4d5f-a3c3-19d6e24ab4a7)

# Automated scan
- Dùng lệnh ```zaproxy``` để mở tool
- Chọn automated scan

![image](https://github.com/Myozz/THM_DOC/assets/94811005/11ed8c74-12ba-4cef-8004-61d31e566e75)
- Có 2 options gọi là "traditional spider" hay "ajax spider"
  - **traditional spider** là một kiểu scan bị động, nó liệt kê các liên kết và dir của web. Nó sẽ build một web index mà không cần brute-force. Cho nên nó sẽ "yên tĩnh" hơn so với brute-force mà vẫn lấy được một số thông tin ngon nghẻ (đương nhiên là không thể đầy đủ như brute-force)
  - **Ajax spider** là một add-on được tích hợp trong ZAP. Ta có thể dùng nó với traditional để có kết quả tốt hơn. Chúng sử dụng web-browser và proxy của chúng ta
- Cách dễ nhất để sử dụng Ajax Spider là với HTMLUnits:

      sudo apt install libjenkins-htmlunit-core-js-java
Sau đó chọn HTMLUnits ở chỗ này<br>
![image](https://github.com/Myozz/THM_DOC/assets/94811005/d607a74e-a503-485a-a63a-ca1aa86eb4cb)
- Thế là set up scan xong

# Manual scan
- Để thực hiện, ra nên setup proxy giữa Zap và trình duyệt
- Các bước setup Proxy:

![image](https://github.com/Myozz/THM_DOC/assets/94811005/85c44aae-7a54-4c9c-894c-5e0c79916df1)
![image](https://github.com/Myozz/THM_DOC/assets/94811005/ccc8b752-4fc2-452c-a476-a3b9baf84cb6)
- Import ZAP Certìicates: (Nếu không làm bước này thì ZAP sẽ không thể thực hiện việc chuyển tiếp và chặn request từ web)
![image](https://github.com/Myozz/THM_DOC/assets/94811005/25437502-5425-4e28-a23e-9ca64a0abb9b)
![image](https://github.com/Myozz/THM_DOC/assets/94811005/f315bd20-c7fd-4547-973e-16bc9369f281)
Tiếp tục set up certificates trên firefox
![image](https://github.com/Myozz/THM_DOC/assets/94811005/3c52b885-86fb-42db-a88a-d3628958e9fb)
![image](https://github.com/Myozz/THM_DOC/assets/94811005/308cee62-835c-4a18-b015-532311b17003)
![image](https://github.com/Myozz/THM_DOC/assets/94811005/2f21b4dd-3446-4b5c-80c8-f42e45cb328b)
- Set up proxy cho firefox:
![image](https://github.com/Myozz/THM_DOC/assets/94811005/d2653f86-b1fd-4b55-ae96-b0c1863cb724)
![image](https://github.com/Myozz/THM_DOC/assets/94811005/06ff8ff8-ce15-4fa9-8b37-6cc18279f961)

Learn more [here](https://tryhackme.com/room/learnowaspzap)
