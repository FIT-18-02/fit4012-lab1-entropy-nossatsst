# Report 1 Page – FIT4012 Lab 1

## 1. Mục tiêu
Tóm tắt ngắn gọn mục tiêu của bài lab.

## 2. Cách làm
- Đọc hiểu chương trình entropy mẫu.
- Bổ sung hàm tính redundancy.
- Hoàn thiện hàm mod_inverse().
- Chạy thử trên nhiều test case.

## 3. Kết quả chính
### 3.1 Entropy và redundancy
| Input | Entropy | Redundancy | Nhận xét |
|---|---:|---:|---|
| aaaa | 0.00 | 8.00 | Chuỗi lặp hoàn toàn, không có sự hỗn loạn, độ dư thừa tối đa. |
| abcd | 2.00 | 6.00 | Mỗi ký tự xuất hiện 1 lần, entropy tăng lên, độ dư thừa giảm xuống. |
| hello world | 2.85 | 5.15 | Chuỗi đa dạng ký tự hơn, entropy cao nhất trong 3 mẫu, độ dư thừa thấp nhất.|

### 3.2 Modulo inverse
| a | m | Kết quả mong đợi | Kết quả chương trình |
|---:|---:|---|---|
| 3 | 7 | 5 | 5 |
| 10 | 17 | 12 | 12 |
| 6 | 9 | Không tồn tại | -1 |

## 4. Kết luận
Qua bài lab, em hiểu rằng entropy càng thấp thì dữ liệu càng dễ đoán và độ dư thừa (redundancy) càng cao. Thuật toán Euclid mở rộng là công cụ hữu hiệu để tìm nghịch đảo modulo, điều kiện tiên quyết là gcd(a, m) phải bằng 1. Khó khăn lớn nhất là việc xử lý số dư âm trong lập trình C++ khi tính x mod m.
