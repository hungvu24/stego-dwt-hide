Hướng Dẫn Bài Lab Giấu Tin DWT
Chuẩn Bị Môi Trường

Phần mềm: VMware Workstation hoặc phần mềm ảo hóa tương tự.
Máy ảo: Labtainer VM được cấu hình kết nối internet.

Tải Bài Lab

Vào thư mục /home/student/labtainer/labtainer-student và chạy lệnh:imodule https://github.com/hungvu24/stego-dwt-hide/raw/refs/heads/main/imodule.tar



Khởi Tạo Bài Lab

Chạy lệnh:labtainer -r stego-dwt-hide


Nhập mã sinh viên làm email khi được yêu cầu để chấm điểm.

Nhiệm Vụ
Nhiệm Vụ 1: Kiểm Tra Kích Thước Thông Điệp Giấu

Liệt kê nội dung thư mục:ls


Di chuyển vào thư mục image:cd image


Xem ảnh watermark:fim watermark.jpg


Kiểm tra kích thước file:stat watermark.jpg


Câu hỏi: Kích thước ảnh là bao nhiêu?

Nhiệm Vụ 2: Kiểm Tra Dung Lượng Ảnh Gốc

Kiểm tra dung lượng file ảnh gốc:stat cover.jpg


Câu hỏi: Dung lượng ảnh gốc là bao nhiêu? Quan sát dung lượng trước khi giấu tin.

Nhiệm Vụ 3: Giấu Thông Điệp Vào Ảnh Gốc

Chạy script giấu tin:python3 main.py --origin cover.jpg --output watermarked.jpg


Chọn DWT => embedding.

Nhiệm Vụ 4: Kiểm Tra Dung Lượng Ảnh Sau Giấu Tin

Kiểm tra dung lượng file watermarked.jpg:stat watermarked.jpg


Câu hỏi: Dung lượng ảnh sau giấu tin là bao nhiêu? So sánh ảnh gốc và ảnh sau giấu.

Kết Thúc Bài Lab

Dừng bài lab:stoplab stego-dwt-hide


File zip chứa kết quả sẽ được tạo và hiển thị vị trí.

Khởi Động Lại Bài Lab

Để làm lại bài lab:labtainer -r stego-dwt-hide



