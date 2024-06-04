<h1> Ứng dụng Auto Scaling Group và Application Load Balancer </h1>
<h2> Tổng quan dự án </h2>
Trong bài tập này, chúng ta sẽ xây dựng ứng dụng chịu tải khi tài nguyên đột ngột tăng cao. Các bạn hãy dùng Service Application Load Balancer để cân bằng tải với Auto Scaling Group trên 2 Availability Zones như sau:

<ul>
<li> Tạo Application Load Balancer </li> 
<li>Tạo Auto Scaling Group </li>
<li>Tạo Launch Configuration</li>
<li>Đợi Instance running</li>
<li>Tăng tải hệ thống</li>
<li>Chờ trong 5 phút và xem các hoạt động Scaling có đang diễn ra hay không</li>
</ul>

<h2> Yêu cầu chi tiết</h2>
<ul>
<li>Học viên tự tạo tài khoản AWS</li>
<li>Tạo IAM User và Group</li>
 <li> Tạo VPC và Security Group</li>
<li>  Tạo Target Group</li>
<li>Tạo Application Load Balancer</li>
<li>Tạo target group nhưng không thêm bất kỳ instance nào</li>
<li>Tạo Auto Scaling group</li>
<li>Cấu hình tối thiểu 2, tối đa 4, mong muốn 2</li>
<li>Tạo launch configuration. Chắc chắn rằng bạn thêm userdata để tải xuống và cài đặt website</li>
<li>Liên kết target group với Auto Scaling group</li>
<li>Liên kết ELB health check</li>
<li>Cấu hình Auto Scaling policy với Average CPU > 20%. Cấu hình thông báo email. Xác nhận email subscription</li>
<li>Đợi cho instance chạy xong. Kiểm tra nếu bạn có thể truy cập vào Web Application sử dụng Load Balancer DNS</li>
<li>Tăng độ tải trên web servers</li>
<li>Tiến hành ssh đến bất kỳ EC2 nào (chắc chắn port 22 đã được mở)</li>
<li>Cài đặt stress: sudo yum install stress -y</li>
<li>Tăng tải: stress --cpu 2 --timeout 300</li>
<li>Chờ 5 phút và xem hoạt động scale</li>
</ul>
