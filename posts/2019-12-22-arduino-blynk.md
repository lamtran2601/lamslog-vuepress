---
title: Các thành phần cơ bản trong hệ thống IoT - Giới thiệu thư viện Blynk
---
## Blynk là cái gì ? Ngon không ?

Bạn đang muốn làm một thiết bị IoT nhưng không biết bắt đầu từ đâu, rất nhiều vấn đề được đặt ra:

*   Làm sao để kết nối thiết bị lên Internet ?
*   Làm sao để kết nối được với Mobile ? Tự làm App hay sử dụng App nào ?
*   Làm sao để quản lý nhiều thiết bị mà không phải config IP hay cài Dyn DNS linh tinh ?
*   Làm sao để chia sẻ quyền điều khiển với mọi người ?

Và còn rất nhiều vấn đề trên trời dưới đất nữa như điều khiển thời gian thực, cập nhật lại trạng thái khi kết nối không ổn định,... Bạn có thể làm được tất cả những thứ trên nhưng mất bao nhiêu thời gian. Blynk được tạo ra để giúp ta những thứ trên mà không cần biết nhiều kiến thức cũng như công sức cài đặt. Ngoài những ưu điểm trên và còn nhiều cái khác nữa, Blynk vẫn còn một số vấn đề như security không được tốt lắm, giới hạn energy (một cách khác của point) để sử dụng trên mobile nếu sử dụng server của Blynk,... Vẫn có cách khắc phục các nhược điểm trên nhưng mình sẽ đề cập ở một bài viết khác. ![Image result for blynk](https://cdn.instructables.com/FWZ/V57G/JC6K4BQD/FWZV57GJC6K4BQD.LARGE.jpg) 

## Các thành phần cơ bản của Blynk

### Arduino

Blynk hỗ trợ rất nhiều loại board Arduino khác nhau như Uno R3 kết hợp với Module Ethernet hay NodeMCU (ESP8266). Có thể tải trên library trên Arduino IDE.

### Mobile app

Hỗ trợ điều khiển thiết bị trên điện thoại, có trên Android và iOS luôn, cứ lên store là kéo về chiến thôi.

### Server

Đây là phần trung gian giao tiếp giữa điện thoại và thiết bị.
* Một số bạn sẽ thắc mắc cần Server để làm gì ?
* Cài đặt và sử dụng như thế nào ?
Bạn cứ tưởng tượng như thế này, thiết bị của bạn kết nối lên Internet, làm sao để biết thiết bị của bạn ở đâu để truy cập đến. 
Có giải pháp là kết nối đến IP của thiết bị và sử dụng DynDNS để truy cập từ xa. Nhưng bao nhiêu thiết bị bạn đều phải cài đặt như vậy ? 
* Một vấn đề khác là bạn cần điều khiển thiết bị theo một quy luật nào đó như set một thời điểm nào đó để bật tắt thiết bị, vậy bạn sẽ làm như thế nào ? Và còn nhiều vấn đề khác nữa như lưu dữ liệu, bảo mật kết nối đến thiết bị,... 
* OK vậy có vẻ như Server cũng khá được việc, rồi cài đặt như nào đây ?
* Blynk có hỗ trợ một Server mặc định và tính phí người dùng theo số lượng widget (Button, Slider, Timer,...), nhưng có cho 2000 energy để dùng trước, được 10 Button để test thử. Sau này nếu có nhu cầu thêm thì một là có thể mua thêm, hoặc tự cài một Server Blynk cho chính mình trên PC hoặc một con Raspberry chẳng hạn. 
* Blynk có Server openSource được viết bằng Java, do đó bạn có thể tải về và tự deploy Server cho riêng mình mà không cần Code gì thêm. Server của mình nên mình thích cho bao nhiêu energy tuỳ ý. 
* Chuyện bên lề: hồi làm luận văn mình cũng có thiết kế và cài đặt nguyên một hệ thống như thế này, tất nhiên là có nhiều thứ hay ho hơn như giao tiếp P2P giữa các device mà không cần Wifi. 2 đứa làm bục mặt mấy tháng liền mới được các chức năng cơ bản, do đó nếu bạn muốn viết lại toàn bộ thì hay xem nguồn lực của mình tới đâu nhé.

* * *

Bài này mình giới thiệu sơ qua các thành phần cơ bản trong một hệ thống IoT, và một thư viện điển hình như Blynk, sẽ hỗ trợ các bạn có một project IoT nhanh chóng và đơn giản. Website chính thức của Blynk:  [https://www.blynk.cc](https://www.blynk.cc/)