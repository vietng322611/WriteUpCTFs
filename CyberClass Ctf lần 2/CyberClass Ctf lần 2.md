
# Đây là writeup của CyberClass ctf lần 2

Lần này gồm có 3 challenges về 3 mảng khác nhau:
> -Steganography
> -Cryptography
> -Forensic

## Steganography challenge: POMERIAN
Đề bài:
![chall 1](pics/chall-data/pomerian.jpg)
Đề bài cho chúng ta 1 bức ảnh về chó pomerian và 1 hint
![dog](pics/chall-data/dog.jpg) ![hint-pomerian](pics/chall-data/pomerian.jpg)
Theo như hint này thì chúng ta phải dùng tool Steganography để tìm dữ liệu trong ảnh, ta cũng được cho mật khẩu là: `CCBEJSJWRQ` và 1 cái hint về `cryptography 26*26`.
Mình đã thử và có vẻ mật khẩu này là không đúng.
![fail1](pics/fail/fail1.jpg)
Khả năng cao là nó đã bị mã hóa nên mình đã tìm về cryptography 26*26 nhưng không nhận được gì!
![fail2](pics/fail/fail2.jpg)
Sau đấy thì mình nhận ra, 26*26 hay 26x26 có thể là kích thước của bảng nên mình đã search `cryptography 26x26` và nhận được cách mã hóa đúng.
![success1](pics/success/success1.jpg)
Thông qua đề bài, để ý chữ `POMERIAN` được viết in hoa, mình biết nó sẽ là pass để giải mã và mình đã giải mã thành công
Mật khẩu đúng: `NOPASSWORD`
![success2](pics/success/success2.jpg)
![success3](pics/success/success3.jpg)
![success4](pics/success/success4.jpg)
Dễ dàng nhận ra đây là base64, giải mã và ghép với dữ kiện đề, ta nhận được flag.
Flag: `CyberClass{Golden Retriever}`