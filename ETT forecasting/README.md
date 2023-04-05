### LƯU Ý: README này chung cho cả ETT forecasting và forecasting full! 

- Forecasting: Time series forecasting là quá trình phân tích dữ liệu chuỗi thời gian bằng cách sử dụng số liệu thống kê và mô hình hóa để đưa ra dự đoán và cung cấp thông tin cho việc ra quyết định chiến lược. Nó không phải lúc nào cũng là một dự đoán chính xác và khả năng dự báo có thể rất khác nhau—đặc biệt là khi xử lý các biến thường dao động trong dữ liệu chuỗi thời gian cũng như các yếu tố nằm ngoài tầm kiểm soát của chúng ta. Tuy nhiên, dự báo cái nhìn chi tiết về kết quả nào có nhiều khả năng, hoặc ít có khả năng xảy ra hơn các kết quả tiềm năng khác. Thông thường, chúng ta có dữ liệu càng toàn diện thì dự báo càng chính xác. Không giống như các bài toán classification và regression, các bài toán Time series forecasting thêm vào sự phức tạp của trật tự hoặc sự phụ thuộc thời gian giữa các quan sát. Điều này có thể khó khăn vì cần phải xử lý dữ liệu chuyên biệt khi điều chỉnh và đánh giá các model.

![image](https://user-images.githubusercontent.com/87894596/230039024-de453ef8-19d2-4117-a1ef-865c2affbbfc.png)

- Thông tin tổng quan về project:
    - ETTh2 và ETTh2_full dataset: Electricity Transformer Temperature (ETT) là một chỉ số quan trọng trong việc triển khai năng lượng điện lâu dài. Chúng ta sẽ sử dụng sub datset với mỗi điểm dữ liệu bao gồm target là OT "nhiệt độ dầu" và các power load features. Khoảng thời gian giữa mỗi sample là 1 giờ và được thu thập từ 2016 đến 2018. ETTh2 dataset là tập data chỉ chứa thông tin OT để thực hiện yêu cầu sử một 1 feature và ETTh2_full là tập data có đủ 6 power load features và OT để thực hiện yêu cầu dùng nhiều hơn 1 feauture để forecast OT.
    
    ![image](https://user-images.githubusercontent.com/87894596/230040258-c4018d62-8bd6-479d-9f44-f9a6f506a5e0.png)
    
    - ETT forecast Ở đây ta sẽ thực hiện sử dụng thông tin của 48 giờ trước để dự đoán OT của 12 giờ tiếp theo. Với các yêu cầu sau:
        - Yêu cầu chỉ sử dụng OT (tập dataset ETTh2) dự đoán OT trong 12 giờ tiếp theo với việc không dùng và có dùng kỹ thuật encode date time feature
        - Yêu cầu sử dụng 5 power load features ’HUFL’, ’HULL’, ’MUFL’, ’MULL’, ’LUFL’ với ’OT’ để dự đoán OT trong 12 giờ tiếp theo với việc không dùng và có dùng kỹ thuật encode date time feature
    
          ![image](https://user-images.githubusercontent.com/87894596/230040768-314ee212-b509-41ef-9669-7df3210d34da.png)
    - ETT forecasting architecture: Các bạn sẽ xây dựng model forecasting như (Hình 14). Mô tả này không gồm chiều của batchsize (None), đầu tiên input sẽ đi qua normalization layer để thực hiện normalize và đi qua 2 layer LSTM với số lượng units tương ứng là 32, 32, và cuối cùng đi qua 2 Dense layer với số lượng units tương ứng là 16 và 12.


    ![image](https://user-images.githubusercontent.com/87894596/230040993-b0d8c06e-1158-4ddd-b0b0-8b59cc41a89f.png)
