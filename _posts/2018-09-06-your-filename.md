---
layout: post
published: true
title: ''
---
---
layout: post
title: What is cache?
---

Cache là bộ nhớ đệm - là bộ nhớ có tốc độ truy xuất nhanh, lưu trữ dữ liệu thường xuyên được sử dụng, nhằm giảm độ trễ trong việc truy xuất dữ liệu từ các thiết bị nhớ có tốc độ truy xuất chập hơn. 

Khái niệm cache được gặp trong nhiều ví dụ như web cache, cache bộ nhớ, TLB () nhưng có cùng ý tưởng chung là giảm thời gian xử lý nhờ lưu lại những phần tử được truy xuất thường xuyên.

1. Cache trong bộ nhớ máy tính.
	- Bộ nhớ cache là bộ nhớ gần CPU nhất, có tốc độ truy xuất nhanh hơn rất nhiều so với RAM.
	- Hạn chế của cache là dung lượng nhỏ do cản trở về giá thành.
	- Để tăng hiệu suất sử dụng cache. Có hai cách là:
		- Chia bộ nhớ cache thành hai, một cho các câu lệnh và một cho dữ liệu. Do câu lệnh thứ nhất được thực thi được load từ bộ nhớ đệm thì khả năng là câu lệnh kế tiếp trong bộ nhớ đệm sẽ là lệnh kế tiếp thực thi. 
		- Sử dụng hệ thống bộ nhớ đệm phân cấp, bộ nhớ đệm L2, L3 có kích thước lớn hơn L1, tuy nhiên tốc độ lại chậm hơn nhưng vẫn còn tốt hơn nhiều so với truy cập từ RAM.
_Tham khảo_ tham khảo bài viết **Giải ngố về bộ nhớ đệm trên genk.vn** để hiểu hơn về tốc độ của CPU so với RAM, và cách cải thiện hiệu suất hit/miss. 
2. TLB - _Translation-Lookaside Buffer_ là cache của bảng phân trang (paging table)

**Nguyên lí locality**
	1. Spatial locality: nếu một địa chỉ được truy cập, thì địa chỉ kế nó khả năng sẽ được gọi truy cập sau đó.
	2. Temporal locality: nếu một địa chỉ được truy cập, thì địa chỉ đó khả năng sẽ được gọi truy cập lại sau đó. 

**Một số giải thuật thay thế trang**
LRU - thay thế trang ít được sử dụng nhất. 