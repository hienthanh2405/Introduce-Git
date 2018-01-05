# Git-Basic

## 1 Sơ đồ tổng quan về hệ thống git

<img src="https://i2.wp.com/hocarm.org/wp-content/uploads/2017/02/VersionControl-Server.png?w=700&ssl=1" />
	
Git thì nó sẽ giúp ta lưu lại các phiên bản mỗi khi có sự thay đổi mã nguồn, đo đó nếu có làm sai ở 
đâu đó trong phiên bản mới thì ta vẫn có thể dễ dàng khắc phục bằng cách khôi phục lại phiên bản cũ 
ổn định hơn.


## 2 Cách lệnh cơ bản của git: clone, add, commit, push, pull, remote

- Cách thông dụng nhất để copy một cái repo là sử dụng lệnh **git clone**:
		Git clone <link repository>
- Lệnh Git add có thể được dùng để thêm file vào index. Vi dụ:
		Git add temp.txt
- Còn bạn muốn lưu lại những thay đổi mỗi lần bạn sửa thì lênh git commit :
		Git commit  –m “Lời nhắn”
- Sau khi commit bạn sẽ đẩy nó len repository với lệnh git push:
		Git push : nó sẽ đẩy lên nhanh ở mặc đinh
- Nhưng bạn muốn đẩy lênh nhánh bạn muốn bạn dùng 
			Git push origin master : đẩy lên nhánh master
- Khi có những thay đổi trên repository thì trước khi thao tác gì trên code bạn nên dùng lệnh:
		Git pull : đưa code về máy mình để xem có những thay đổi gì ko
- Git remote :
	
## 3 Cách sử dụng .gitignore

Mục đích sử dụng gitignore: Khi phát triển một dự án phần mềm thì chắc chắn sẽ có rất nhiều file bạn không 
muốn đẩy lên repository, ví dụ như các file thư viện js,css (nếu đã dùng bower để quản lý) hay là những file 
sau khi biên dịch chương trình…..blah blah. Chính vì điều này mà Git đã cung cấp cho chúng ta một kỹ thuật 
để khi commit thì Git sẽ tự động bỏ nó ra khỏi repository, đó chính là 1 tệp tin có tên là .gitignore.
Có 2 loại gitignore cần chú ý:
a> Local gitignore : Chỉ có tác dụng trong 1 repository và nó buộc phải commit & push lên repository để share 
với các user khác
b> Global gitignore : Được share với tất cả các repository trong máy tính của bạn
- B1: Tạo file .gitignore : echo "" > .gitignore hoặc có thể down về từ trên mạng với những ngôn ngữ bạn cần.
- B2: Sau khi tạo file .gitignore xong thì bạn phải commit & push lên repository, từ nay về sau những thư mục, tệp 
		tin mà bạn muốn ignore đã được loại bỏ hoàn toàn khỏi sự quản lý của Git.
		
## 4. Thao tác với Repository

Tạo một repository mới trên trang github.com

![Imgur](https://i.imgur.com/INNS2fv.png)

Một số phương pháp tôi hay sử dụng để viết:

## 4.1. Thẻ tiêu đề

Markdown sử dụng kí tự # để bắt đầu cho các thẻ tiêu đề, có thể dùng từ 1 đến 6 ký tự # liên 

tiếp. Mức độ riêu đề giảm dần từ 1 đến 6

- Tùy mục đích và ý thích bạn có thể sử dụng cách này để thể hiện các chỉ mục khác nhau.

Ví dụ:

#1.Tiêu đề cấp 1

# 1.Tiêu đề cấp 1

##2.Tiêu đề cấp 2

## 2.Tiêu đề cấp 2


######6.Tiêu đề cấp 6

###### 6.Tiêu đề cấp 6

## 4.2. Chèn link, chèn ảnh

- Để chèn hyperlink bạn chỉ cần paste luôn linh đó vào file .md

https://github.com

https://github.com

Hoặc bạn cũng có thể sử dụng cú pháp sau để thu ngắn đường dẫn của link

`[Github](https://github.com)`

Kết quả là:

[Github](https://github.com)

- Để chèn ảnh thì bạn hãy sử dụng cú pháp sau:

'![tieu_de](link_hinh)'

up hình lên trang http://i.imgur.com/ để lấy đường dẫn ảnh đưa vào Github

## 4.3. Ký tự in đậm, in nghiêng

- Để in đậm một đoạn text bạn chỉ cần làm như sau:

`**từ cần in đậm**`

Kết quả là:

**từ cần in đậm**

- Để in nghiên một đoạn text bạn chỉ cần làm như sau:

`*từ cần in nghiêng*`

*từ cần in nghiêng*

## 4.4. Trích dẫn, bo chữ

-  Để bo một đoạn text thì bạn chỉ cần sử dụng cú pháp sau:

`đoạn cần bo`

Kết quả là: `đoạn cần bo`

## 5 Cách Sử dụng Source Tree

Tải về phần mềm SourceTree: https://www.sourcetreeapp.com/

Giao diện chính sẽ có hình dạng:

 !(https://i.imgur.com/3XVx2wI.png)
 
- B1: Clone Repository trong SourceTree

 !(https://imgur.com/a/sHixQ)
 
- B2: Thực hiện cách thao tác add, commit, push, pull trên sourcetree

 !(https://imgur.com/a/M6x7v)
