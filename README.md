# Stego-DWT-Hide

## Giới thiệu
Dự án này là một bài lab thực hành về kỹ thuật giấu tin (steganography) sử dụng phương pháp DWT (Discrete Wavelet Transform). Mục tiêu là giấu thông điệp vào ảnh mà không làm thay đổi đáng kể dung lượng hoặc chất lượng hình ảnh.

## Yêu cầu hệ thống
- **Phần mềm ảo hóa**: VMware Workstation hoặc tương tự.
- **Máy ảo**: Labtainer VM với kết nối internet.

## Cài đặt và cấu hình
1. Tải bài lab:
   - Vào thư mục `/home/student/labtainer/labtainer-student` và chạy:
     ```bash
     imodule https://github.com/hungvu24/stego-dwt-hide/raw/refs/heads/main/imodule.tar
     ```
2. Khởi tạo bài lab:
   - Chạy lệnh:
     ```bash
     labtainer -r stego-dwt-hide
     ```
   - Nhập mã sinh viên làm email khi được yêu cầu để chấm điểm.

## Hướng dẫn thực hiện

### Nhiệm vụ 1: Kiểm tra kích thước thông điệp giấu
- Liệt kê nội dung thư mục:
  ```bash
  ls
  ```
- Di chuyển vào thư mục `image`:
  ```bash
  cd image
  ```
- Xem ảnh watermark:
  ```bash
  fim watermark.jpg
  ```
- Kiểm tra kích thước file:
  ```bash
  stat watermark.jpg
  ```

### Nhiệm vụ 2: Kiểm tra dung lượng ảnh gốc
- Kiểm tra dung lượng file ảnh gốc:
  ```bash
  stat cover.jpg
  ```

### Nhiệm vụ 3: Giấu thông điệp vào ảnh gốc
- Chạy script giấu tin:
  ```bash
  python3 main.py --origin cover.jpg --output watermarked.jpg
  ```
- Chọn **DWT => embedding**.

### Nhiệm vụ 4: Kiểm tra dung lượng ảnh sau giấu tin
- Kiểm tra dung lượng file `watermarked.jpg`:
  ```bash
  stat watermarked.jpg
  ```
- So sánh dung lượng ảnh gốc và ảnh sau giấu.

## Kết thúc bài lab
- Dừng bài lab:
  ```bash
  stoplab stego-dwt-hide
  ```
- File zip chứa kết quả sẽ được tạo và hiển thị vị trí.

## Khởi động lại bài lab
- Chạy lại:
  ```bash
  labtainer -r stego-dwt-hide
  ```

## Tác giả
- [hungvu24](https://github.com/hungvu24)

## Giấy phép
[MIT License](LICENSE)
