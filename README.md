# gitlab.github.io

<p align="center">
 <h1 align="center">Cách sử dụng gitlab ?</h1>
</p> 

## Gitlab là gì?
- GitLab là phần mềm quản lý soruce code Git. Tính năng chủ yếu là lưu trữ code nhanh chóng, hiệu quả cho các doanh nghiệp, tổ chức cá nhân.
- Lý do nên chọn sử dụng Gitlab: 
  + Việc lưu trữ và tải code siêu nhanh, siêu dễ dàng.
  + Theo dõi sự thay đổi trong code chính xác.
  + Hỗ trợ người dùng quản lý và phân phối công việc chất lượng hơn.
  + Cho phép tất cả các thành viên trong nhóm cộng tác trong mọi giai đoạn của dự án.
  + Nó cho phép các đường ống CI/CD mạnh mẽ.
  + Nó có một sổ đăng ký tích hợp có thể được triển khai ngay lập tức mà không cần bất kỳ cấu hình nào.
  + Nó có thể được tích hợp hoàn hảo với Kubernetes.
  + Nó có thể nhập khẩu các dự án khổng lồ và cũng xuất khẩu các mã khác trong dự án.
 
## Ưu nhược điểm của Gitlab
### Ưu điểm:
- Rất dễ dàng để thiết lập.
- Giao diện người dùng và công cụ thân thiện với người dùng.
- Gitlab có không giới hạn các kho lưu trữ riêng miễn phí.
- Có thể tích hợp nhiều API và dịch vụ của bên thứ ba
- Thời gian hoạt động khá tốt.
  
### Nhược điểm: 
- Gitlab có phần giao diện khá phức tạp.
- Bản thân công cụ có một vài lỗi có thể làm cho nó hơi cẩu thả.

## Cách cài đặt Gitlab 

Mở và đăng nhập gitlab.com

Tạo dự án (mô tả riêng tư hoặc công khai):

chọn new project

![image](https://github.com/thangdtph27626/gitlab.github.io/assets/109157942/aa527fa9-d334-49e3-b597-5f1ce96f1882)

tại đây bạn có thể chọn các lựa chọn khác nhau trong bài viết này sẽ import project trên github 
          
![image](https://github.com/thangdtph27626/gitlab.github.io/assets/109157942/257caef2-4541-4dd6-be31-9eb671ba915e)

chọn github 
![image](https://github.com/thangdtph27626/gitlab.github.io/assets/109157942/069fa222-4f96-4597-8fb9-fee6096a003b)

chọn Authenticate with GitHub 
![image](https://github.com/thangdtph27626/gitlab.github.io/assets/109157942/7a276d65-ce19-4fa3-a6ac-a22400ecc2c8)


Chọn Create blank project
![image](https://github.com/thangdtph27626/gitlab.github.io/assets/109157942/a214f138-ea4a-4d90-97e0-b37a6bbc4b94)

bạn có thể tìm kiếm tên repository và bấm import để

![image](https://github.com/thangdtph27626/gitlab.github.io/assets/109157942/7ff33b1b-8f04-4747-8400-88e3b538b02d)



Mở Git Bash, chọn lệnh:  Git config –global user.name “tutorial”; Git config –global user.email ishan.gaba@simplilearn.net

Mở Git Bash, chọn lệnh

Tạo kho lưu trữ chọn lệnh:  mkdir tutorial và cd tutorial.

Tạo kho lưu trữ chọn lệnh

Sử dụng tiếp lệnh:  pwd

Sử dụng tiếp lệnh: pwd

Tạo kho lưu trữ Git sử dụng lệnh: Git init

Tạo kho lưu trữ Git sử dụng lệnh: Git init

Dẫn hướng đến cặp và tìm thư mục “.git” ẩn.

Dẫn hướng đến cặp và tìm thư mục ".git" ẩn.

Tạo một sổ lưu trữ sử dụng lệnh: touch input.txt và notepad input.txt

Tạo một sổ lưu trữ sử dụng lệnh

Notepad sẽ xuất hiện trên màn hình. Gõ bất cứ thứ gì bên trong nó, sau đó lưu và đóng lại.

Notepad sẽ xuất hiện trên màn hình

Kiểm tra trạng thái tệp: git status

Thêm tệp vào khu vực dàn dựng sử dụng lệnh: git add.

Thêm tệp vào khu vực dàn dựng sử dụng lệnh: git add.

Để cam kết sử dụng lệnh:  git commit -m “input”

Để cam kết sử dụng lệnh:  git commit -m "input"

Kiểm tra lại trạng thái của tệp: git status

Kiểm tra lại trạng thái của tệp: trạng thái git

Đẩy notepad vào kho lưu trữ GitLab: hãy truy cập GitLab của bạn và sao chép lệnh như hình dưới đây:

Đẩy notepad vào kho lưu trữ GitLab

Sau đó quay lại Git Bash của bạn và dán lệnh:

Sau đó quay lại Git Bash của bạn và dán lệnh

Bây giờ sử dụng lệnh từ xa, tiếp theo là lệnh push, để đẩy tệp đến kho lưu trữ từ xa.

Sử dụng lệnh: “git remote -v”

Sử dụng lệnh: “git remote -v”

Sử dụng lệnh: “git push -u origin master”

Sử dụng lệnh: “git push -u origin master”

Bây giờ đi đến GitLab của bạn và kiểm tra xem có bất kỳ bổ sung nào cho dự án mới mà bạn đã tạo ban đầu hay không.

Mở và kiểm tra nội dung của notepad.

Mở và kiểm tra nội dung của notepad.


