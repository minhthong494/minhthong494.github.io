---
layout: post
published: false
title: ''
---
## Phân biệt Cookies và Sessions

Vì giao thức HTTP là giao thức "_stateless_", nghĩa là server không lưu lại bất kì thông tin gì từ client request trước đó. Tuy nhiên, Website thông thường có nhu cầu nhận diện người dùng. HTTP sử dụng **_Cookies_**, cho phép sites theo vết user. 

**Session** khái niệm session dùng để chỉ khoảng thời gian tương tác giữa client và server. 
**Cookie** là đoạn text lưu trữ ID của browser phục vụ cho việc tracking.

**Điểm khác nhau giữa PHP Cookie & Session**
Trong PHP, session và cookie đều có mục đích chung là keep track user. Điểm khác biệt lớn nhất giữa cookie và session là thông tin được lưu trữ trong cookie nằm ở user computer, trong khi thông tin được lưu trữ trong một session lại nằm ở web server. Chính điểm khác biệt này xác định những ứng dụng phù hợp cho session và cookie. 



**_Cookie_** được lưu trữ trên user computer. Những thông tin có thể lưu trữ trong cookie là username, password, cookie ID, .. Những ứng dụng phổ biến của cookie là xác thực người dùng, lưu trữ preferences, and shopping cart items. Nhược điểm của cookie là nó nằm trên máy người dùng nên có thể bị xóa, bị thay đổi bất cứ lúc nào. Do đó không sử dụng cookie để lưu trữ những thông tin nhạy cảm. Cookie có thể bị vô hiệu hóa bởi user. 

**_Session_** thông tin được lưu trữ phía server, duy nhất unique ID lưu trữ phía client. Unique ID này được gửi đến server thông qua HTTP header. Unique ID này dùng để truy xuất thông tin user trong database của server. Khi user đóng website, session kết thúc. Session bị ràng buộc về mặt thời gian chặt chẽ hơn cookie.  

Session không thể bị vô hiệu hóa hay chỉnh sửa bởi visitor. 

Nếu bạn làm biếng đăng nhập mỗi lần truy cập vào website, hay là tín đồ mua sắm online, cookie có thể là một lựa chọn tốt. Nếu bạn ưu tiên sự an toàn, session là lựa chọn tốt nhất. 

**Q&A**
1. Khi thực hiện đăng nhập, cookie lưu lại username & password, thì ở lần truy cập kế tiếp, username & password được gửi đến server bằng giao thức gì? 
For instance, Unique ID được gửi kèm trong HTTP header. 
2. _Cookieless_ là gì? 
*Hint:* khi browser không hỗ trợ cookie hoặc disable cookie, cookieless sẽ được sử dụng. 


**Source**
- [https://www.thoughtco.com/the-difference-between-cookies-and-sessions-2693956](https://www.thoughtco.com/the-difference-between-cookies-and-sessions-2693956)