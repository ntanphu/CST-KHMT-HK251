# CST-KHMT-HK251
Môn học: Cơ Sở Toán cho Khoa Học Máy Tính

Học kỳ: 251
## Giảng viên hướng dẫn:
- TS. Nguyễn An Khương
- TS. Trần Tuấn Anh
- TS. Lê Hồng Trang

## Bài tập lớn:
Đề tài: Comparative Study of Optimization Algorithms: AdaDelta and Adam

Mục tiêu chung:
- Hiểu rõ nguyên lý, công thức và cơ chế cập nhật của Adadelta và Adam.
- Biết cách áp dụng chúng vào bài toán tối ưu trong học sâu (Deep Learning).
- So sánh hiệu năng, tốc độ hội tụ và độ ổn định với các phương pháp khác (SGD, RMSProp, Adagrad).

## Học viên thực hiện:
- Nguyễn Tấn Phú - 2480859
- Nguyễn Đăng Khoa - 2570431
- Phạm Hoàng Sơn - 2570315
- Nguyễn Hoàng Nam - 2570460
- Nguyễn Trần Huy Việt - 2252906
## Phân công nội dung chi tiết:
### Section 1: Tổng quan & nền tảng toán học
Responsible Person: [Nguyễn Tấn Phú]

Key Topics: Giới thiệu về thuật toán tối ưu, động cơ xuất hiện AdaDelta & Adam
- Mô tả nhược điểm của Adagrad → động cơ ra đời của Adadelta và Adam.
- Viết lại công thức cơ bản của GD và Momentum để tạo nền tảng so sánh.
- Giải thích khái niệm moving average, learning rate, adaptive methods.
- Trình bày “Lý do cần AdaDelta & Adam”.

### Section 2: Thuật toán AdaDelta (Lý thuyết)
Responsible Person: [Nguyễn Đăng Khoa]

Key Topics: AdaDelta – Nguyên lý, công thức cập nhật
- Trình bày công thức Adadelta: ước lượng trung bình bình phương gradient, cập nhật ∆x.
- Giải thích ý nghĩa các đại lượng (ρ, ε, v_t, E[∆x²], …).
- Chứng minh vì sao Adadelta khắc phục hạn chế của Adagrad.

### Section 3: AdaDelta (thực nghiệm & ví dụ)
Responsible Person: [Phạm Hoàng Sơn]

Key Topics: Cài đặt và minh họa AdaDelta
- Cài đặt AdaDelta bằng Python (NumPy hoặc PyTorch).
- Chạy thử với một bài toán nhỏ ( Cơ sở dữ liệu MNIST, Convolutional Neural Networks đơn giản (CNN)).
- File code minh họa, biểu đồ hội tụ (loss vs iteration), accuracy.

### Section 4: Thuật toán Adam (lý thuyết)
Responsible Person: [Nguyễn Hoàng Nam]

Key Topics: Adam về mặt công thức và cơ chế
- Phần lý thuyết chi tiết Adam. Trình bày công thức diễn giải toán học rõ ràng.
- Trình bày công thức từng bước (update rule).
- Giải thích tại sao Adam hội tụ nhanh và ổn định hơn.


### Section 5: Adam (thực nghiệm & ví dụ)
Responsible Person: [Nguyễn Trần Huy Việt]

Key Topics: Cài đặt và minh họa Adam
- Cài đặt Adam, chạy song song với Adadelta cùng bộ dữ liệu.
- Chạy thử với một bài toán nhỏ ( Cơ sở dữ liệu MNIST, Convolutional Neural Networks đơn giản (CNN)).
- File code minh họa, biểu đồ hội tụ (loss vs iteration), accuracy.

### Section 6: Lý thuyết, thực nghiệm [12.10.3. Yogi]
Responsible Person: [Nguyễn Tấn Phú]

Key Topics: Lý thuyết
- Mô tả vì sao Adam có thể không hội tụ trong bài toán lồi (convex).
- Giải thích sự khác biệt trong cách cập nhật v_t giữa Adam và Yogi.
- Giải thích trực quan cách nó ngăn v_{t} “phình to”.

Thực nghiệm
- Cài đặt Yogi (numpy hoặc PyTorch).
- Dùng dataset nhỏ (MNIST).
- So sánh đường loss của Yogi vs Adam vs Adadelta.
- Tổng hợp bảng so sánh 3 thuật toán (Adadelta, Adam, Yogi).
- Ghi nhận đặc điểm: tốc độ hội tụ, ổn định, độ dao động loss.
- Gợi ý khi nào nên dùng Yogi.

### Section 7: Implementation Updates – Figures, Notebook, and Report
Responsible Person: [Nguyễn Tấn Phú]
- Thực hiện tổng hợp các lý thuyết
- Thực nghiệm và Bảng so sánh các thuật toán (SGD, AdaGrad, RMSProp, AdaDelta, Adam).
- So sánh tốc độ hội tụ, độ ổn định, loss, accuracy.
- Tổng hợp bảng so sánh 2 thuật toán (ưu, nhược, khi nào dùng).

## References
[1] Zaheer, M., Reddi, S. J., Sachan, D., Kale, S., & Kumar, S. (2018). **Adaptive Methods for Nonconvex Optimization.** *Advances in Neural Information Processing Systems (NeurIPS)*.
