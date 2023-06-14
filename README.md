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

## Tầng vật lý của GitLab
- Kho lưu trữ: xử lý các dự án trong Gitlab. Các sản phẩm lưu trữ (như dự án) có thể được lưu trữ tại warehouse. Nó có thể là một đĩa cứng hoặc một cái gì đó phức tạp hơn như hệ thống tập tin NFS.
- Nginx hoạt động giống như front-desk. Người sử dụng đến Nginx và yêu cầu hành động được thực hiện bởi worker trong văn phòng.
- Cơ sở dữ liệu là một loạt các file của các metal file cabinets với các thông tin:
 + Các sản phẩm trong warehouse (siêu dữ liệu, issuse, các yêu cầu merge …).
 + Người sử dụng đến front-desk (permissions).
- Redis: là phần giao tiếp một broad với cubby holes- cái mà có thể chứa các nhiệm vụ, yêu cầu cho worker.
- Sidekiq là một worker, công việc chủ yếu là xử lý việc gửi email. Nó nhận nhiệm vụ từ Redis.
- A Unicorn worker: là một nhân viên xử lý các nhiệm vụ nhanh chóng và dễ. Học làm việc với Redis. Công việc của họ gồm:
- Kiểm tra quyền truy cập bằng cách kiểm tra các session của người dùng được lưu trữ trong Redis cubby hole.
- Làm nhiệm vụ cho Sidekiq.
- Lấy công cụ từ warehouse hoặc di chuyển mọi thứ xung quanh trong đó
- Gitlab-shell: là loại thứ ba của worker, nhiệm vụ của nó là tạo các đơn đặt hàng từ một máy fax (SSH) thay vì front-desk (HTTP). Gitlab-shell giao tiếp với Sidekiq qua Redis và hỏi những câu hỏi nhanh của Unicorn worker hoặc trực tiếp hoặc qua front-desk.
- Gitlab enterprise edition (ứng dụng) là tập hợp các quy trình và hoạt động kinh doanh được điểu hành bởi ofice (văn phòng).
## System layout
- Khi đề cập đến Git trong những hình ảnh có nghĩa là thư mục home của người sử dụng Git thường là /home/git.
- Repositories bare nằm trong đường dẫn /home/git/repositories. Gitlab là một ứng dụng ruby on ralis do đó để biết rõ các hoạt động bên trong bạn có thể tìm hiểu bằng cách tìm hiểu về hoạt động của ruby on ralis.
- Để sử dụng kho dữ liệu qua SSH có một ứng dụng thêm vào được gọi là gitlab-sell cái mà được cài đặt tại /home/git/gitlab-shell.
  
## Components

![image](https://github.com/thangdtph27626/gitlab.github.io/assets/109157942/a108ef10-d22c-4324-bf17-7d7149887919)

## Cách cài đặt Gitlab 


11 Tạo dự án (mô tả riêng tư hoặc công khai):

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

bạn có thể tìm kiếm tên repository và bấm import để import project từ github của mình 

![image](https://github.com/thangdtph27626/gitlab.github.io/assets/109157942/7ff33b1b-8f04-4747-8400-88e3b538b02d)

![image](https://github.com/thangdtph27626/gitlab.github.io/assets/109157942/23886a3f-db42-4271-8135-f0e198e9d060)

chọn quay trở lại projects tại đây bạn sẽ thấy project bạn vừa import 

![image](https://github.com/thangdtph27626/gitlab.github.io/assets/109157942/bff75ea5-848b-443c-acde-76f11ed2802f)

2: Thêm thành viên trong github 

chọn một dự án  cần thêm thành viên ->  chọn members -> Invite members -> nhập gmail hoặc username của thành viên, chọn quền, và ngày hết hạn truy cập

![image](https://github.com/thangdtph27626/gitlab.github.io/assets/109157942/6ee14f11-f71b-40b0-94f4-0f205a8812f9)
![image](https://github.com/thangdtph27626/gitlab.github.io/assets/109157942/3b04f2ad-4b57-4820-8bde-88cd9b27e07f)
![Uploading image.png…]()


Bạn có thể tìm hiểu cách sử dụng gitlab thêm tại  https://docs.gitlab.com/ee/user/ 







