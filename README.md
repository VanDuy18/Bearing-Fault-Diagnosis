# Bearing-Fault-Diagnosis
Chẩn đoán lỗi ổ bi là bài toán ánh xạ tín hiệu đo được sang trạng thái kỹ thuật của ổ bi. Trong đề tài này, đầu vào là gia tốc rung theo thời gian và đầu ra là một trong bốn lớp: Normal, Inner race, Outer race và Ball fault. Khó khăn chính nằm ở sự thay đổi biên độ và cấu trúc phổ theo tốc độ, mức độ lỗi, vị trí cảm biến, đường truyền rung và nhiễu đo.
Một quy trình chẩn đoán hoàn chỉnh cần tách rõ ba tầng: thu nhận và kiểm soát chất lượng tín hiệu; biến đổi tín hiệu thành biểu diễn có ý nghĩa; phân loại và đánh giá trên dữ liệu chưa xuất hiện trong huấn luyện. Độ chính xác cao chỉ có ý nghĩa khi cách chia dữ liệu ngăn được việc các đoạn gần như giống nhau của cùng một tệp xuất hiện ở cả tập train và test.
Đối tượng nghiên cứu là tín hiệu rung đo trên gối đỡ underhang của mô hình máy quay trong bộ dữ liệu MAFAULDA. Nghiên cứu sử dụng một kênh gia tốc hướng kính, tần số lấy mẫu 50 kHz và bốn nhãn trạng thái ổ bi. Mỗi bản ghi có 250.000 mẫu, tương ứng 5 giây đo. Đề tài tập trung vào bài toán phân loại trạng thái, chưa thực hiện ước lượng kích thước khuyết <img width="945" height="472" alt="image" src="https://github.com/user-attachments/assets/038eba70-96c3-40ab-bca7-86e0a9c4f193" />

Xây dựng quy trình tiền xử lý tín hiệu rung và tạo ma trận phổ thời gian-tần số bằng STFT.
Thiết kế mạng 2D-CNN để phân loại bốn trạng thái: bình thường, lỗi vòng trong, lỗi vòng ngoài và lỗi phần tử lăn.
Khảo sát bốn cấu hình cửa sổ STFT, lựa chọn cấu hình bằng tập validation và đánh giá một lần trên tập test độc lập.
 Đánh giá khả năng tổng quát hóa với các mức độ lỗi khi tốc độ thay đổi thông qua Accuracy, Precision, Recall, Macro-F1 và ma trận nhầm lẫn.
