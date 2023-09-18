# XSS (Cross-Site Scripting) 
- XSS là một lỗ hổng bảo mật được tìm thấy trong web app. Có thể sử dụng để thực thi mã đọc trên mục tiêu.
- Có nhiều loại tấn công khi nói về XSS, đây là một số trong đó:
  - Key logging (log lại quá trình dùng bàn phím)
    - Một **Keylogger** được sử dụng bởi set up một event listener trên bàn phím của mục tiêu, nó ghi theo dõi keystroke và lưuu vàp server tấn công
  - Stealing Cookies (Chôm Cookies)
    - Khi attacker chôm được **cookies** của mục tiêu, họ có thể sử dụng thông tin để login vào user mà không cần xác thực hoặc thâm chí có thể dùng thông tin trong đó play sạch đống account lưu trong trình duyệt :|| sợ thật
  - Phising (Lừa đảo)
    - Phishing (Fishing à :||) là một loại khai thác lỗ hỗng thú vị :||, một attacker có thể cloe website mà bạn đăng nhập vào, rồi từ đấy lấy thông tin của bạn thôi :|| (clone thì tên miền như nào tôi không rõ, chứ mà nó fake cả tên miền giống hệt web gốc thì hết cứu, nên chắc là không giống đâu). Một hình thức phishing khác là attaker có thể nhét code trực tiếp vào webpage để làm thay đổi form nhằm thu thập thông tin bạn nhập vào

# Các loại XSS
- Có 3 loại XSS phổ biến là DOM-Based XSS (type-0 XSS), Reflected XSS (Non-Persistent XSS), và Stored XSS (Persistent XSS)

## DOM-Based XSS
- Là khi một attack payload được thực thi bằng cách thao tác DOM (Document Object Model) trên trình duyệt mục tiêu. Loại này sử dụng client-side code, không phải server-side code

## Reflected XSS
- Là khi một tập mã độc từ một website khác nhảy vào web app hay website của mục tiêu. Thông thường, chúng được được chuyển vào URL dưới dạng một truy vấn (query) và rất dễ để khiến mục tiêu click vào link. Loại này thao tác trên Request của mục tiêu

## Store XSS
- Là khi một mã độc được trực tiếp nhét thẳng vào mồm webpage hay web app. Loại này thao tác trên database của web

