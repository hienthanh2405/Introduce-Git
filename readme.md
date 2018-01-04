1 Sơ đồ tổng quan về hệ thống git


2 Cách lệnh cơ bản của git: clone, add, commit, push, pull, remote

	Cách thông dụng nhất để copy một cái repo là sử dụng lệnh git clone:
		Git clone <link repository>
	Lệnh Git add có thể được dùng để thêm file vào index. Vi dụ:
		Git add temp.txt
	Còn bạn muốn lưu lại những thay đổi mỗi lần bạn sửa thì lênh git commit :
		Git commit  –m “Lời nhắn”
	Sau khi commit bạn sẽ đẩy nó len repository với lệnh git push:
		Git push : nó sẽ đẩy lên nhanh ở mặc đinh
	Nhưng bạn muốn đẩy lênh nhánh bạn muốn bạn dùng 
	Git push origin master : đẩy lên nhánh master
	Khi có những thay đổi trên repository thì trước khi thao tác gì trên code bạn nên dùng lệnh:
		Git pull : đưa code về máy mình để xem có những thay đổi gì ko
	Git remote :
	
3 Cách sử dụng .gitignore

	Mục đích sử dụng gitignore: Khi phát triển một dự án phần mềm thì chắc chắn sẽ có rất nhiều file bạn không 
	muốn đẩy lên repository, ví dụ như các file thư viện js,css (nếu đã dùng bower để quản lý) hay là những file 
	sau khi biên dịch chương trình…..blah blah. Chính vì điều này mà Git đã cung cấp cho chúng ta một kỹ thuật 
	để khi commit thì Git sẽ tự động bỏ nó ra khỏi repository, đó chính là 1 tệp tin có tên là .gitignore.
	Có 2 loại gitignore cần chú ý:
	a> Local gitignore : Chỉ có tác dụng trong 1 repository và nó buộc phải commit & push lên repository để share 
	với các user khác
	b> Global gitignore : Được share với tất cả các repository trong máy tính của bạn
	Tạo file .gitignore : echo "" > .gitignore hoặc có thể down về từ trên mạng với những ngôn ngữ bạn cần.
	Sau khi tạo file .gitignore xong thì bạn phải commit & push lên repository, từ nay về sau những thư mục, tệp 
	tin mà bạn muốn ignore đã được loại bỏ hoàn toàn khỏi sự quản lý của Git.
