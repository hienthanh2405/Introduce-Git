# Git-Basic

## 1 Sơ đồ tổng quan về hệ thống git

![Imgur](https://i.imgur.com/QOtE7O4.png)


- **Remote repository**: Là repository để chia sẻ giữa nhiều người và bố trí trên server chuyên dụng.
- **Local repository**: Là repository bố trí trên máy của bản thân mình, dành cho một người dùng sử dụng.

Do repository phân thành 2 loại là local và remote nên với những công việc bình thường thì có thể sử dụng local repository và thực hiện trên toàn bộ máy sẵn có. Khi muốn công khai nội dung công việc mà bản thân đã làm trên local repository, thì sẽ upload lên remote repository rồi công khai. Thêm nữa, thông qua remote repository cũng có thể lấy về nội dung công việc của người khác.

**Ghi lại thay đổi vào repository: Working Tree và Index**

Trên Git, những thư mục được đặt trong sự quản lý của Git mà mọi người đang thực hiện công việc trong thực tế được gọi là working tree.

Và trên Git, giữa repository và working tree tồn tại một nơi gọi là index. Index là nơi để chuẩn bị cho việc commit lên repository.

![Imgur](https://i.imgur.com/JCho4AW.png)

Trên Git, khi đã thực hiện commit thì trạng thái sẽ không được ghi trực tiếp trong repository từ working tree, mà sẽ ghi trạng thái đã được thiết lập của index được xây dựng ở giữa đó. Vì thế, để ghi lại trạng thái của file bằng commit thì trước hết cần đăng ký file trong index.

Với việc chèn index vào giữa như thế này, bạn có thể thực hiện commit không bao gồm những file không cần thiết trong working tree, hay có thể đăng ký chỉ một phần thay đổi của file trong index rồi commit.

## 2 Cách lệnh cơ bản của git: clone, add, commit, push, pull, remote, merge, giải quyết conflict.

- Cách thông dụng nhất để copy một cái repository là sử dụng lệnh `git clone`: git clone <link repository>
- Lệnh `git add` có thể được dùng để thêm file vào index. Vi dụ: git add temp.txt
- Còn bạn muốn lưu lại những thay đổi mỗi lần bạn sửa thì lênh `git commit` : git commit  –m “Lời nhắn”
- Sau khi commit bạn sẽ đẩy nó lên repository với lệnh `git push`: git push 
- Nhưng bạn muốn đẩy lên nhánh bạn muốn bạn dùng `git push origin master`: đẩy lên nhánh master
- Khi có những thay đổi trên repository thì trước khi thao tác gì trên code bạn nên dùng lệnh: `git pull`: đưa code về máy mình để xem có những thay đổi gì ko
- `git remote`: Để có thể chia sẻ local repository của mình, bạn cần trỏ nó vào một remote repository nào đó. Việc trỏ này có thể thay đổi, thêm hoặc xóa đi khi bạn muốn.
- Merge branch sẽ được thực hiện bằng lệnh `git merge`: git merge <commit>
- Giải quyết xung đột: trường hợp đã thay đổi ở nơi giống nhau trong file trên remote repository và local repository. Trường hợp này, vì nó không thể tự phán đoán được lấy thay đổi từ bên nào nên sẽ phát sinh lỗi. Những nơi phát sinh xung đột, Git sẽ chỉnh sửa nội dung file giống như sơ đồ bên dưới, nên cần phải chỉnh sửa bằng tay.

![Imgur](https://i.imgur.com/r3o9Ubw.png)

Sau khi chỉnh sửa tất cả chỗ xung đột, nếu như tiến hành commit thì commit đã tích hợp thay đổi sẽ được tạo ra.

![Imgur](https://i.imgur.com/4tLgiOy.png)
	
## 3 Cách sử dụng .gitignore

Mục đích sử dụng gitignore: Khi phát triển một dự án phần mềm thì chắc chắn sẽ có rất nhiều file bạn không muốn đẩy lên repository, ví dụ như các file thư viện js,css (nếu đã dùng bower để quản lý) hay là những file sau khi biên dịch chương trình…..blah blah. Chính vì điều này mà Git đã cung cấp cho chúng ta một kỹ thuật để khi commit thì Git sẽ tự động bỏ nó ra khỏi repository, đó chính là 1 tệp tin có tên là .gitignore.
Có 2 loại gitignore cần chú ý:

**a. Local gitignore**: Chỉ có tác dụng trong 1 repository và nó buộc phải commit & push lên repository để share 
với các user khác

**b. Global gitignore**: Được share với tất cả các repository trong máy tính của bạn

- B1: Mở cmd trên windows lên
- B2: Tạo file .gitignore bằng lệnh: `echo "" > .gitignore` hoặc có thể down về từ trên mạng với những ngôn ngữ bạn cần.
- B3: Sau khi tạo file .gitignore xong thì bạn phải commit & push lên repository, từ nay về sau những thư mục, tệp tin mà bạn muốn ignore đã được loại bỏ hoàn toàn khỏi sự quản lý của Git.
		
## 4. Thao tác với Repository

![Imgur](https://i.imgur.com/wxWdHoA.png)

Có 2 cách tạo local repository:

- Tạo repository hoàn toàn mới
- Sao chép từ remote repository (clone)


### *Một số phương pháp tôi hay sử dụng để viết markdow:*

##### 4.1. Thẻ tiêu đề

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

##### 4.2. Chèn link, chèn ảnh

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

##### 4.3. Ký tự in đậm, in nghiêng

- Để in đậm một đoạn text bạn chỉ cần làm như sau:

`**từ cần in đậm**`

Kết quả là:

**từ cần in đậm**

- Để in nghiên một đoạn text bạn chỉ cần làm như sau:

`*từ cần in nghiêng*`

*từ cần in nghiêng*

##### 4.4. Trích dẫn, bo chữ

-  Để bo một đoạn text thì bạn chỉ cần sử dụng cú pháp sau:

`đoạn cần bo`

Kết quả là: `đoạn cần bo`

##### 5 Cách Sử dụng Source Tree

Tải về phần mềm SourceTree: https://www.sourcetreeapp.com/

Giao diện chính sẽ có hình dạng:

<img src="https://i.imgur.com/3XVx2wI.png " />
 
- B1: Clone Repository trong SourceTree

<img src="https://i.imgur.com/iwvgVOC.png " />  
 
- B2: Thực hiện cách thao tác add, commit, push, pull trên sourcetree

- Thao tác add, commit:
<img src="https://i.imgur.com/AX5E3oj.jpg" />

- Thao tác push:
<img src="https://i.imgur.com/pg9jI8g.jpg" />

- Thao tác pull:
<img src="https://i.imgur.com/iRODbm7.jpg" />

## 6 Cách phân nhánh hiệu quả trong Git 

<h4>Branch trong Git là gì?</h4>
Khi bắt đầu khởi tạo một repository hoặc clone một repository, bạn sẽ có một nhánh (branch) chính tên là master 
(bạn có thể hiểu master là một cái thân cây). Đây là branch mà sẽ chứa toàn bộ các mã nguồn chính trong repository.

Repo trung tâm sẽ chứa hai branches chính hoạt động mãi mãi:
- master
- develop
Nhánh master tại origin là nhánh quen thuộc với tất cả các Git users. Song song là nhánh develop.

Bên cạnh hai branches chính master và develop, mô hình mà tôi đang sử dụng còn có thêm rất nhiều những branches phụ để 
giúp các team members có thể phát triển song song, dễ dàng tracking theo features, chuẩn bị cho release hoặc fix nhanh 
các vấn đề production. Khác với hai branches chính kia, các branches phụ này chỉ tồn tại trong một khoảng thời gian ngắn, 
rồi sẽ bị xoá đi.
- Feature branches
- Release branches
- Hotfix branches

Feature branches (hay còn gọi là topic branches) được sử dụng để phát triển các feature mới phục vụ cho release sau này.
Khi bắt đầu phát triển một chức năng, có thể chưa rõ được thời điểm chức năng đó được tích hợp vào hệ thống và release. 
Feature branch sẽ tồn tại trong quá trình chức năng được phát triển, cuối cùng sẽ được merge lại vào develop (khi quyết định 
lần release tới bao gồm chức năng đó) hoặc bị bỏ đi (khi thấy chức năng không còn cần thiết).

-  Để tạo một nhánh và chuyển sang nhánh đó đồng thời, bạn có thể chạy lệnh git checkout với tham số -b:
	git checkout -b iss53
	Switched to a new branch "iss53"

## 7 Giới thiệu về cách tạo team, tạo pull request và phân quyền

#### Pull request

Đề đảm bảo cho việc tương tác nhóm được tốt hơn, và hạn chế tối đa conflict có thể xảy ra, cũng như dễ dàng theo dấu dự án (để khôi phục trạng thái nếu lỡ có biến cố xảy ra), hay để cộng đồng nguồn mở có thể tham gia đóng góp cho dự án được thuận tiện và blah blah lợi ích khác, `pull request` ra đời.

*Ví dụ chúng ta đã phát triển xong tính năng nào đó(nhánh tên bar)và muốn ghép nó vào với master, lúc này ta sẽ push code mình lên bar branch trên server, sau đó thực hiện yêu cầu được ghép code vào nhánh chính: yêu cầu này chính là `pull request`.*

#### Thao tác:
`$ git push gh nhanh_can_pull`

Lệnh trên sẽ đẩy bar branch của mình lên server, đồng thời tạo branch mới trên đó nếu chưa có.

##### Khác nhau giữa Pull và Pull Request trong Git?

##### Git Pull

Câu lệnh `git pull` thực ra là viết tắt của `git pull origin master`. Trong đó:

`origin` là tên của kho chứa từ xa (hay remote repository).

`master` là tên của nhánh trên kho chứa từ xa. Một kho chứa có thể có nhiều nhánh khác nhau.

Về bản chất khi chạy câu lệnh git pull origin master thực sự là bạn đang sử dụng hai câu lệnh phía sau:

> $ git fetch origin master

và:

> $ git merge origin master

Câu lệnh `git fetch origin master` sẽ truy vấn thông tin của kho chứa từ xa trên máy chủ remote và sau đó kéo về máy local những thay đổi này. Tiếp đó câu lệnh trên sẽ thực hiện việc so sánh những thay đổi mới kéo về máy local và hiển thị thông tin.

Câu lệnh `git merge orign master` sẽ gộp những thay đổi mới kéo về (dùng câu lệnh git fetch ở trên) từ máy chủ từ xa với nhánh hiện tại trên máy local.

##### Pull Request

Thông thường khi làm với Git mỗi lập trình viên sẽ tạo một branch mới khác với master để phát triển một tính năng mới. Giả sử nhánh mà lập trình viên tạo ra để phát triển tính năng có tên là `my_feature`. Trong trường hợp này sau khi đẩy commit trên nhánh này trên nhánh tương ứng `my_feature` ở kho chứa từ xa `origin `thì để các lập trình viên khác có thể kéo về được commit này thì quản trị viên trên máy chủ từ xa cần thực hiện việc gộp commit ở nhánh `my_feature` về nhánh `master`.

**Pull request** là một yêu cầu gửi tới quản trị viên kho chứa từ xa gộp commit mới được tạo ra từ nhanh `my_feature` về nhánh `master` để các lập trình viên khác có thể pull về được.

**Tạo team và phân quyền**

Để tạo một nhóm cho nhiều người cùng làm việc ta làm như sau:

Truy cập URL: https://github.com/settings/organizations, 

- Chọn New Organizations
- Đặt tên và email cho tổ chức

![Imgur](https://i.imgur.com/xt8owBv.png)

Tại mục `Choose the organization’s plan` chọn Open Source để miễn phí, nhưng lúc này các Repo trong tổ chức sẽ là public.

Mời các thành viên cho tổ chức

![Imgur](https://i.imgur.com/XPRVedO.png)

Lúc này vào trang cá nhân của bạn sẽ thấy tại mục Organizations có tổ chức mới vừa tạo. Để cấu hình tổ chức này ta click thẳng vào nó.

![Imgur](https://i.imgur.com/0yeynZG.png)

Ở đây tôi sẽ tạo một team mới như hình sau:

![Imgur](https://i.imgur.com/BUEok1Q.png)

![Imgur](https://i.imgur.com/uS5bVnV.png)

Với 3 mức: Read Access, Write Access, Admin Access Github cho phép chúng ta phân quyền tới các thành viên của nhóm.

![Imgur](https://i.imgur.com/gWV75N1.png)

Để mời một người dùng khác vào team, ta click vào team đó và search tên của người dùng cần tìm

![Imgur](https://i.imgur.com/sM2opUb.png)

Sau đó hệ thống sẽ yêu cầu bạn nhập password để xác thực, nếu thành công, một email xác nhận sẽ được gửi đến người được mời và người này sẽ xác nhận có tham gia vào tổ chức hay không.

## 8 Giới thiệu về cách sử dụng GitLab 

### Tạo Repository trong GitLab
- Tạo Project 

<img src="https://i.imgur.com/6CAJTit.png" />

- Ghi tên project và ấn nút khởi tạo

<img src="https://i.imgur.com/ylCiu60.png" />

- Tạo thành công 

<img src="https://i.imgur.com/Pkt8gz1.png" />

### Cách add những thành viên trong gitlap

<img src="https://i.imgur.com/RQUTnId.png" />

### Cách sử dụng Merge request
- B1: Trước khi bắt đầu, bạn nên có sẵn 1 nhánh và có những lần commit trên nhánh đó đên Gitlab
- B2: Đi tới project mà bạn muốn kết hợp các thay đổi của mình và nhấp vào tab Merge requests
- B3: Click on New merge request
- B4: Từ đó, bạn có tùy chọn để chọn chi nhánh nguồn và nhánh mục tiêu mà bạn muốn so sánh. 
	
<img src="https://docs.gitlab.com/ee/gitlab-basics/img/merge_request_select_branch.png" />

- B5: Khi sẵn sàng, chọn **Compare branches** and **continue** button.
- B6: Tối thiểu, thêm tiêu đề và mô tả cho yêu cầu hợp nhất của bạn. Theo tùy chọn, chọn người dùng
 để xem lại yêu cầu hợp nhất và để chấp nhận hoặc đóng nó. Bạn cũng có thể chọn mốc thời gian và nhãn.
 
<img src="https://docs.gitlab.com/ee/gitlab-basics/img/merge_request_page.png" />

- B7: Click on the Submit merge request button

### Phân Quyền 
- Nhóm có nhiều hơn 1 người thì thiết làm phần quyền

<img src="https://i.imgur.com/bW5WGmc.png" />
