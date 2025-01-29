### 1. Giới thiệu về công cụ quản lý phiên bản

### 1.1 Khái niệm về công cụ quản lý phiên bản

Công cụ quản lý phiên bản là một hệ thống dùng để ghi lại các thay đổi của một hoặc nhiều file theo thời gian, giúp ta xem lại từng phiên bản khi cần.

### 1.2 Lợi ích của công cụ quản lý phiên bản

- Khôi phục file trước đây hoặc tại một thời điểm mong muốn.
- Giải quyết hạn chế của quản lý phiên bản thủ công (dễ quên, ghi đè nhầm file, copy nhầm file không cần thiết).

### 1.3 Hạn chế của cách quản lý phiên bản thủ công

- Dễ gây nhầm lẫn và lạm lộn file.
- Không theo dõi được các thay đổi một cách chặt chẽ.

---

### 2. Các loại hệ thống quản lý phiên bản

### 2.1 Hệ thống quản lý phiên bản tập trung (CVCSs)

### 2.1.1 Đặc điểm

- Chỉ có một máy chủ trung tâm chứa các file và lịch sử thay đổi.
- Các máy khách kết nối và làm việc trực tiếp với máy chủ.

![{18C884DE-E1B9-4A8C-944D-09679194C4B2}.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/d69efadf-94a7-4e98-9253-b2453d844694/d8ab1947-47bf-492d-afc2-4b04196d61e7/18C884DE-E1B9-4A8C-944D-09679194C4B2.png)

### 2.1.2 Ưu điểm

- Các thành viên cùng biết được tiến độ và công việc của nhầm.
- Quản trị viên quản lý quyền truy cập.

### 2.1.3 Nhược điểm

- Khi máy chủ hỏng, các thành viên không thể tiếp tục làm việc.
- Nguy cơ mất dữ liệu nếu không có bản sao lưu.

### 2.2 Hệ thống quản lý phiên bản phân tán (DVCSs)

### 2.2.1 Đặc điểm

- Mỗi thành viên có bản sao đầy đủ của dữ liệu.
- Hỗ trợ nhiều remote repository để các nhóm làm việc song song.

### 2.2.2 Lợi ích của DVCS so với CVCS

- Phòng tránh mất dữ liệu khi một máy hỏng.
- Hỗ trợ nhiều luồng công việc linh hoạt.

---

### 3. Các đặc trưng của Git

### 3.1 Lịch sử và nguồn gốc của Git

- Git ra đời vào năm 2005, tiền thân là project BitKeeper.

### 3.2 Cách Git lưu trữ dữ liệu: Chuỗi các bản chụp nhanh (Snapshots)

- Lưu trữ những bức ảnh chụp nhanh thay vì danh sách thay đổi.
- File không thay đổi sẽ liên kết tới phiên bản trước.

![{CCF356D2-11F6-4A90-B51F-4E09BB37BD5D}.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/d69efadf-94a7-4e98-9253-b2453d844694/3f82e0e8-790e-47d8-9415-8804098c5c11/CCF356D2-11F6-4A90-B51F-4E09BB37BD5D.png)

### 3.3 Hoạt động chủ yếu trên local

- Các thao tác được xử lý nhanh chóng, không phụ thuộc vào máy chủ.

### 3.4 Tính toàn vẹn của dữ liệu trong Git

- Mã checksum SHA-1 bảo đảm không thể thay đổi dữ liệu mà không bị phát hiện.

### 3.5 Git chỉ thêm dữ liệu, không thay đổi dữ liệu đã lưu

- Sau khi commit, rất khó mất dữ liệu.
- Khuyến khích thử nghiệm mà không lo lắng.

---

### 4. Trạng thái của file trong Git

### 4.1 Các trạng thái của file

- **Modified (sửa đổi):** File đã thay đổi nhưng chưa commit.
- **Staged (theo dõi):** File được chọn để commit.
- **Committed (commit):** File đã được lưu trong database cục bộ.

![{0772D2A8-5C0C-4BD0-BD01-5A032694767B}.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/d69efadf-94a7-4e98-9253-b2453d844694/92fab917-0ffc-4493-b8f9-e9bc1dd7120c/0772D2A8-5C0C-4BD0-BD01-5A032694767B.png)

### 4.2 Các phần chính trong project Git

### 4.2.1 Cây công việc (Working Tree)

- Chứa file đang làm việc, được checkout từ database.

### 4.2.2 Vùng đang theo dõi (Staging Area)

- File lưu thông tin cho commit tiếp theo.

### 4.2.3 Thư mục Git (Git Directory)

- Lưu trữ siêu dữ liệu và database của project.

### 4.3 Quy trình làm việc cơ bản trong Git

1. Sửa đổi file trong Working Tree.
2. Thêm thay đổi vào Staging Area.
3. Commit thay đổi vào database.

---

### 5. Tóm tắt và kết luận

### 5.1 So sánh Git với các hệ thống quản lý phiên bản khác

- Git linh hoạt, bền vững và toàn vẹn hơn nhờ cơ chế lưu trữ snapshot.

### 5.2 Lợi ích của việc sử dụng Git trong quản lý dự án

- Hiệu quả cao khi quản lý project.
- Dễ dàng phục hồi và theo dõi lịch sử thay đổi.

### 5.3 Kết luận

Git không chỉ là một công cụ quản lý phiên bản mạnh mẽ mà còn là một phần không thể thiếu trong quy trình phát triển phần mềm hiện đại. Hiểu và sử dụng tốt Git sẽ giúp bạn tối ưu hóa năng suất và quản lý dự án một cách chuyên nghiệp.
