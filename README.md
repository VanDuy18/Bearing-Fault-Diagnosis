# Bearing-Fault-Diagnosis
Chẩn đoán lỗi ổ bi là bài toán ánh xạ tín hiệu đo được sang trạng thái kỹ thuật của ổ bi. Trong đề tài này, đầu vào là gia tốc rung theo thời gian và đầu ra là một trong bốn lớp: Normal, Inner race, Outer race và Ball fault. Khó khăn chính nằm ở sự thay đổi biên độ và cấu trúc phổ theo tốc độ, mức độ lỗi, vị trí cảm biến, đường truyền rung và nhiễu đo.
Một quy trình chẩn đoán hoàn chỉnh cần tách rõ ba tầng: thu nhận và kiểm soát chất lượng tín hiệu; biến đổi tín hiệu thành biểu diễn có ý nghĩa; phân loại và đánh giá trên dữ liệu chưa xuất hiện trong huấn luyện. Độ chính xác cao chỉ có ý nghĩa khi cách chia dữ liệu ngăn được việc các đoạn gần như giống nhau của cùng một tệp xuất hiện ở cả tập train và test.
Đối tượng nghiên cứu là tín hiệu rung đo trên gối đỡ underhang của mô hình máy quay trong bộ dữ liệu MAFAULDA. Nghiên cứu sử dụng một kênh gia tốc hướng kính, tần số lấy mẫu 50 kHz và bốn nhãn trạng thái ổ bi. Mỗi bản ghi có 250.000 mẫu, tương ứng 5 giây đo. Đề tài tập trung vào bài toán phân loại trạng thái, chưa thực hiện ước lượng kích thước khuyết 
<img width="896" height="299" alt="image" src="https://github.com/user-attachments/assets/9c26d306-05fc-4c8b-948a-86ec548e9974" />
Xây dựng quy trình tiền xử lý tín hiệu rung và tạo ma trận phổ thời gian-tần số bằng STFT.<img width="800" height="500" alt="12288" src="https://github.com/user-attachments/assets/108b422f-b611-474d-b34a-784e87653f6e" />
<img width="945" height="472" alt="image" src="https://github.com/user-attachments/assets/c075da2c-c314-4421-aaa3-de32679529fb" />
Thiết kế mạng 2D-CNN để phân loại bốn trạng thái: bình thường, lỗi vòng trong, lỗi vòng ngoài và lỗi phần tử lăn.<img width="945" height="366" alt="image" src="https://github.com/user-attachments/assets/e673be75-f4d4-4b20-b418-9a79c7d6dc20" />

Khảo sát bốn cấu hình cửa sổ STFT, lựa chọn cấu hình bằng tập validation và đánh giá một lần trên tập test độc lập.<img width="762" height="283" alt="image" src="https://github.com/user-attachments/assets/46f70326-e0e5-48a7-a620-cc46de8e62dc" />

 Đánh giá khả năng tổng quát hóa với các mức độ lỗi khi tốc độ thay đổi thông qua Accuracy, Precision, Recall, Macro-F1 và ma trận nhầm lẫn.<img width="945" height="556" alt="image" src="https://github.com/user-attachments/assets/d06e87df-ca3c-4f3a-8aaf-81aa6b3f8801" /> <img width="945" height="474" alt="image" src="https://github.com/user- />
attachments/assets/52ee9bc4-f81a-481d-b858-23bbe4696bb2" /> <img width="377" height="348" alt="image" src="https://github.com/user-attachments/assets/dcc0a92b-727d-404d-b529-e0f6acb420c7" />




# Bearing-Fault-Diagnosis

Bearing fault diagnosis is the process of mapping measured signals to the technical condition of a bearing. In this project, the input is time-domain vibration acceleration, and the output is one of four classes: Normal, Inner race, Outer race, and Ball fault. The main challenge lies in the variation of amplitude and spectral structure depending on motor speed, fault severity, sensor location, vibration transmission path, and measurement noise.

A complete diagnostic pipeline requires a clear separation of three layers: signal acquisition and quality control; signal transformation into a meaningful representation; and classification and evaluation on unseen data. High accuracy is only meaningful when the data splitting strategy prevents nearly identical segments of the same file from leaking into both the training and test sets.

The research object is the vibration signal measured on the underhang bearing housing of the rotating machinery model in the MAFAULDA dataset. The study utilizes one radial acceleration channel, a sampling frequency of 50 kHz, and four bearing condition labels. Each record contains 250,000 samples, corresponding to 5 seconds of measurement. This project focuses strictly on the condition classification problem and does not yet perform defect size estimation.
 
<img width="896" height="299" alt="image" src="https://github.com/user-attachments/assets/9c26d306-05fc-4c8b-948a-86ec548e9974" />

Build a vibration signal preprocessing pipeline and generate time-frequency spectrogram matrices using STFT.
<img width="800" height="500" alt="12288" src="https://github.com/user-attachments/assets/108b422f-b611-474d-b34a-784e87653f6e" />
<img width="945" height="472" alt="image" src="https://github.com/user-attachments/assets/c075da2c-c314-4421-aaa3-de32679529fb" />

Design a 2D-CNN network to classify four conditions: normal, inner race fault, outer race fault, and rolling element fault.
<img width="945" height="366" alt="image" src="https://github.com/user-attachments/assets/e673be75-f4d4-4b20-b418-9a79c7d6dc20" />

Investigate four STFT window configurations, select the optimal configuration using the validation set, and evaluate it once on an independent test set.
<img width="762" height="283" alt="image" src="https://github.com/user-attachments/assets/46f70326-e0e5-48a7-a620-cc46de8e62dc" />

Evaluate the generalization capability across different fault severities under varying speeds using Accuracy, Precision, Recall, Macro-F1 scores, and confusion matrices.
<img width="945" height="556" alt="image" src="https://github.com/user-attachments/assets/d06e87df-ca3c-4f3a-8aaf-81aa6b3f8801" /> <img width="945" height="474" alt="image" src="https://github.com/user-attachments/assets/52ee9bc4-f81a-481d-b858-23bbe4696bb2" /> <img width="377" height="348" alt="image" src="https://github.com/user-attachments/assets/dcc0a92b-727d-404d-b529-e0f6acb420c7" />

