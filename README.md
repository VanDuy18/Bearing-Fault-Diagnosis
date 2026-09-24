# Bearing-Fault-Diagnosis
Chẩn đoán lỗi ổ bi là bài toán ánh xạ tín hiệu đo được sang trạng thái kỹ thuật của ổ bi. Trong đề tài này, đầu vào là gia tốc rung theo thời gian và đầu ra là một trong bốn lớp: Normal, Inner race, Outer race và Ball fault. Khó khăn chính nằm ở sự thay đổi biên độ và cấu trúc phổ theo tốc độ, mức độ lỗi, vị trí cảm biến, đường truyền rung và nhiễu đo.
Một quy trình chẩn đoán hoàn chỉnh cần tách rõ ba tầng: thu nhận và kiểm soát chất lượng tín hiệu; biến đổi tín hiệu thành biểu diễn có ý nghĩa; phân loại và đánh giá trên dữ liệu chưa xuất hiện trong huấn luyện. Độ chính xác cao chỉ có ý nghĩa khi cách chia dữ liệu ngăn được việc các đoạn gần như giống nhau của cùng một tệp xuất hiện ở cả tập train và test.
Đối tượng nghiên cứu là tín hiệu rung đo trên gối đỡ underhang của mô hình máy quay trong bộ dữ liệu MAFAULDA. Nghiên cứu sử dụng một kênh gia tốc hướng kính, tần số lấy mẫu 50 kHz và bốn nhãn trạng thái ổ bi. Mỗi bản ghi có 250.000 mẫu, tương ứng 5 giây đo. Đề tài tập trung vào bài toán phân loại trạng thái, chưa thực hiện ước lượng kích thước khuyết 
<img width="896" height="299" alt="image" src="https://github.com/user-attachments/assets/9c26d306-05fc-4c8b-948a-86ec548e9974" />
Xây dựng quy trình tiền xử lý tín hiệu rung và tạo ma trận phổ thời gian-tần số bằng STFT.<img width="800" height="500" alt="12288" src="https://github.com/user-attachments/assets/108b422f-b611-474d-b34a-784e87653f6e" />
<img width="945" height="472" alt="image" src="https://github.com/user-attachments/assets/c075da2c-c314-4421-aaa3-de32679529fb" />
Thiết kế mạng 2D-CNN để phân loại bốn trạng thái: bình thường, lỗi vòng trong, lỗi vòng ngoài và lỗi phần tử lăn.<img width="945" height="366" alt="image" src="https://github.com/user-attachments/assets/e673be75-f4d4-4b20-b418-9a79c7d6dc20" />

Khảo sát bốn cấu hình cửa sổ STFT, lựa chọn cấu hình bằng tập validation và đánh giá một lần trên tập test độc lập.Xếp hạng	Cấu hình STFT	N_w	H	Kích thước ảnh	Best epoch	Val Loss	Val Accuracy	Val F1	Thời gian huấn luyện (s)
1	Nw_256_H_30_129x129	256	30	129×129	27	0.000002	100.00%	100.00%	3169.75
2	Nw_1024_H_6_513x513	1024	6	513×513	19	0.000152	100.00%	100.00%	6594.69
3	Nw_512_H_14_257x257	512	14	257×257	8	0.000190	100.00%	100.00%	3335.83
4	Nw_128_H_62_65x65	128	62	65×65	10	0.001135	100.00%	100.00%	2719.44

 Đánh giá khả năng tổng quát hóa với các mức độ lỗi khi tốc độ thay đổi thông qua Accuracy, Precision, Recall, Macro-F1 và ma trận nhầm lẫn.<img width="945" height="556" alt="image" src="https://github.com/user-attachments/assets/d06e87df-ca3c-4f3a-8aaf-81aa6b3f8801" /> <img width="945" height="474" alt="image" src="https://github.com/user-<img width="589" height="543" alt="image" src="https://github.com/user-attachments/assets/03c79034-5358-460b-b222-dae9bb89ac3a" />
attachments/assets/52ee9bc4-f81a-481d-b858-23bbe4696bb2" />


