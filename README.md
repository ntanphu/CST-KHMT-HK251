# CST-KHMT-HK251
Môn học: Cơ Sở Toán cho Khoa Học Máy Tính

Học kỳ: 251
## Giảng viên hướng dẫn:
- TS. Nguyễn An Khương
- TS. Trần Tuấn Anh
- PGS. TS. Lê Hồng Trang

## Bài tập lớn:
Đề tài: Comparative Study of Optimization Algorithms: AdaDelta and Adam

Mục tiêu chung:
- Hiểu rõ nguyên lý, công thức và cơ chế cập nhật của Adadelta và Adam.
- Biết cách áp dụng chúng vào bài toán tối ưu trong học sâu (Deep Learning).
- So sánh hiệu năng, tốc độ hội tụ và độ ổn định với các phương pháp khác (SGD, RMSProp, Adagrad, SGD + Momentum, SGD + Nesterov Momentum) sử dụng các mô hình Multilayer Perceptron (MLP), Convolutional Neural Networks (CNN) đơn giản, VGG16, ResNet-18.

## Học viên thực hiện:
- Nguyễn Tấn Phú - 2480859
- Nguyễn Đăng Khoa - 2570431
- Phạm Hoàng Sơn - 2570315
- Nguyễn Hoàng Nam - 2570460
- Nguyễn Trần Huy Việt - 2252906
## Phân công nội dung chi tiết:
### Section 1: Tổng quan & nền tảng toán học
Responsible Person: [Nguyễn Tấn Phú]

Key Topics: Tổng quan và kiến thức cơ sở về các thuật toán tối ưu, động cơ xuất hiện AdaDelta & Adam
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
- Làm rõ sự khác biệt trong cập nhật $v_t$ giữa Adam và Yogi, và cơ chế giúp Yogi tránh việc “phóng đại” phương sai.

Thực nghiệm
- Cài đặt Yogi (numpy hoặc PyTorch).
- Dùng dataset nhỏ (MNIST).
- So sánh đường loss của Yogi, Adam, AdaDelta, SGD, SGD + Momentum, SGD + Nesterov Momentum, Adagrad và RMSProp với mô hình Multilayer Perceptron (MLP), Convolutional Neural Networks (CNN) đơn giản, VGG16, ResNet-18.
- Tổng hợp bảng so sánh các thuật toán.
- Ghi nhận đặc điểm: tốc độ hội tụ, ổn định, độ dao động loss.
- Gợi ý khi nào nên dùng Yogi.

### Section 7: Implementation Updates – Figures, Notebook, and Report
Responsible Person: [Nguyễn Tấn Phú]
- Thực hiện tổng hợp các lý thuyết
- Thực nghiệm và Bảng so sánh các thuật toán.
- So sánh tốc độ hội tụ, độ ổn định, loss, accuracy.
- Tổng hợp bảng so sánh thuật toán (ưu, nhược, khi nào dùng).

## References
 [1] L. Bottou, “Large-scale machine learning with stochastic gradient descent,” in Proceedings of COMPSTAT’2010, pp. 177–186, Springer, 2010.
 
 [2] J. Duchi, E. Hazan, and Y. Singer, “Adaptive subgradient methods for online learning and stochastic optimization,” Journal of Machine Learning Research, vol. 12, pp. 2121–2159, 2011.
 
 [3] T. Tieleman and G. Hinton, “Lecture 6.5 — rmsprop,” tech. rep., COURSERA: Neural Networks for Machine Learning, 2012. http://www.cs. toronto.edu/~tijmen/csc321/slides/lecture_slides_lec6.pdf.
 
 [4] M. D. Zeiler, “Adadelta: An adaptive learning rate method,” arXiv preprint arXiv:1212.5701, 2012.
 
 [5] D. P. Kingma and J. Ba, “Adam: A method for stochastic optimization,” in Proceedings of the 3rd International Conference on Learning Represen tations (ICLR), 2015.
 
 [6] M. Zaheer, S. J. Reddi, D. Sachan, S. Kale, and S. Kumar, “Adaptive methods for nonconvex optimization,” in Advances in Neural Information Processing Systems (NeurIPS), 2018.
 
 [7] S. Ruder, “An overview of gradient descent optimization algorithms,” arXiv preprint arXiv:1609.04747, 2016.
 
 [8] Y. Nesterov, “A method for solving the convex programming problem with convergence rate o(1/k2),” Soviet Mathematics Doklady, vol. 27, no. 2, pp. 372–376, 1983.
 
 [9] I. Sutskever, J. Martens, G. Dahl, and G. Hinton, “On the importance of initialization and momentum in deep learning,” in International Conference on Machine Learning (ICML), pp. 1139–1147, 2013.
 
 [10] J. Pennington, R. Socher, and C. D. Manning, “Glove: Global vectors for word representation,” in Proceedings of the 2014 Conference on Empirical Methods in Natural Language Processing (EMNLP), pp. 1532–1543, 2014.
