- Time series data là một dạng dữ liệu với giá trị được đo lường tại những điểm khác nhau theo thời gian. Một số dữ liệu time series được phân bố theo tần suất nhất định, ví dụ như thời tiết trong 1 giờ, lượng truy cập website trong ngày, tổng doanh thu trong tháng... Dữ liệu time series cũng có thể phân bố với khoảng cách không đều, ví dụ như số lượng cuộc gọi khẩn cấp trong ngày hoặc nhật ký hệ thống.
![image](https://user-images.githubusercontent.com/87894596/230034442-936ea6c8-d90c-4668-96bc-43040f8caefa.png)
- Ở project này, ta thực hiện các vấn đề sau:
    1. Read dataset: Open Power Systems Data
    2. Time series data structures
    3. Time-based indexing
    4. Visualizing time series data
    5. Seasonality
    6. Frequencies
    7. Resampling
    8. Rolling windows
    9. Trends
- Trong bài này chúng ta dùng bộ dữ liệu daily time series của Open Power System Data (OPSD) ở Đức,
gồm tổng lượng tiêu thụ điện, sản xuất điện gió và sản xuất điện mặt trời trên toàn quốc trong giai
đoạn 2006-2017. Chúng ta sẽ khám phá mức tiêu thụ và sản xuất điện ở Đức thay đổi theo thời gian
như thế nào, và trả lời các câu hỏi:
    1. Khi nào mức tiêu thụ điện thường cao nhất và thấp nhất?
    2. Làm thế nào để sản xuất năng lượng gió và mặt trời thay đổi theo mùa trong năm?
    3. Xu hướng dài hạn trong tiêu thụ điện, năng lượng mặt trời và năng lượng gió là gì?
    4. Làm thế nào để sản xuất năng lượng gió và mặt trời so sánh với mức tiêu thụ điện, và tỷ lệ này đã thay đổi như thế nào theo thời gian?
