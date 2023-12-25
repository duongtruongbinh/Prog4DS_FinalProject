# PROGRAMMING FOR DATA SCIENCE - FIT - HCMUS
## Final Project - Thu thập, phân tích cho trả lời câu hỏi về bộ dữ liệu MyAnimeList
### I. Group infomation:
- Class ID: 21KHDL1

#|Họ tên
-|-
21127616|Lê Phước Quang Huy
21127229|Dương Trường Bình

### II. Project Information:
#### **_01. Dataset:_**
- **Link:** [Spotify Tracks Dataset](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset).
- **Description:**
    - [Spotify Tracks Dataset](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset) is a dataset of **Spotify** tracks over a range of 125 different genres.  
    - Each track is identified by its Spotify ID and accompanied by metadata such as artist names, album name, track name, and popularity.
    - The dataset provides a rich set of audio features, offering insights into the musical characteristics of each track.
    - These features include `acousticness`, `danceability`, `energy`, 
    `instrumentalness`, `liveness`, `loudness`, `speechiness`, ...etc.
- **License:** `Database: Open Database, Contents: © Original Authors`. The combined license structure of the `Spotify Tracks Dataset`, comprising the ODbL and the acknowledgment of the original authors' copyright, permits its usage for non-commercial endeavors like learning and research. Consequently, the dataset's utilization in this project adheres to the license terms and does not compromise the intellectual property rights of its creators 


#### **_02. Data exploring and preprocessing:_**
- **Understand basic information and Preprocessing dataset:**
    - Handle duplicated rows, missing values, abnormal values and outliers
- **Data distribution:**
    - Numerical columns
    - Categorical columns
- **Visualize data**

#### **_03. Meaningful questions:_**
- Câu hỏi 1:
  - Đầu tiên là tìm thể loại (`genres`) phổ biến nhất với từng đối tượng.
  - Sử dụng hồi quy tuyến tính dựa vào 3 đầu vào là `scored_by`, `members`, `favorites` để dự đoán `score`.
  - Đưa ra ngưỡng `score` khuyến nghị kết hợp với thể loại đã tìm được ở trên để recommend những manga mang tính khuyến nghị cao cho từng đối tượng.

> **Kết quả:** Ta có thể thấy những bộ nổi tiếng đều có tên trong danh sách này, vì vậy hệ thống khuyến nghị là tốt.

![Q1](./Images/Q1.png)

- Câu hỏi 2:
  - Đếm số manga bắt đầu mỗi năm dựa vào `real_start_date`, thời điểm bùng nổ là những vùng xung quanh cực đại.
  - Phân tích đặc điểm:
    - Thứ nhât: Thể loại genres và chủ đề themes phổ biến nhất ở thời kì bùng nổ và so sánh với tất cả thời điểm.
    - Thứ hai: Xem xét mean score của từng năm và so sánh với thời kì bùng nổ.
    - Thứ ba: Xem xét có bao nhiêu (%) manga ở thời kì này thành công đến thời điểm hiện tại (score >= 7.0).

> **Kết quả:**
> - Manga vẫn phát triển mạnh đến ngày nay, tuy vậy thời điểm số lượng bộ manga được bắt đầu nhiều nhất là vào thời điểm 2012-17.
> - Đồng thời cũng có sự tương quan dương giữa điểm trung bình (500 manga thuộc top cao nhất của từng thời kì) với số manga được xuất bản.
> - Có 2857 manga đã thành công và chiếm 12.74% trong tổng số manga ở thời kì bùng nổ.

![Q2](./Images/Q2.png)

- Câu hỏi 3:
  - Tính số manga mà mỗi tác giả đã tham gia.
  - Mỗi mangaka sẽ có hai chỉ số:
    - Chỉ số thứ nhất: tính bằng trung bình cộng `score` của 2 manga cao nhất mà mangaka đó tham gia.
    - Chỉ số thứ hai: là số manga mà tác giả đó tham gia và đặt giá trị trần là 10, nếu mangaka tham gia nhiều hơn 10 bộ thì chỉ tính là 10.
  - Scale hai chỉ số về dạng thích hợp.
  - Tính tổng của tích chỉ số với trọng số (mỗi chỉ số sẽ có trọng số tương ứng để thể hiện mức độ ảnh hưởng), output sẽ là mức độ cống hiến, thành công của một mangaka.
  - Sau đó ta sẽ lấy ra những mangaka có output cao nhất.

> **Kết quả:** Output là chỉ số thuộc (0, 1], mangaka có output cao hơn sẽ có ranking cao hơn. Rank không chỉ phụ thuộc vào một bộ manga có ảnh hưởng lớn, mà còn phụ thuộc vào mangaka đó có bao nhiêu tác phẩm với score cao.

> - Mangaka top1

![Q3-top1](./Images/Q3-top1.png)

> - Mangaka top2

![Q3-top2](./Images/Q3-top2.png)

> - Mangaka Eiichiro Oda

![Q3-eiichiro-oda](./Images/Q3-eiichiro-oda.png)

> - Mangaka Masashi Kishimoto

![Q3-masashi-kishimoto](./Images/Q3-masashi-kishimoto.png)

- Câu hỏi 4:
  - Đặt ra các điều kiện để xét các manga cho từng thể loại (`genres`), nếu như thể loại nào có quá ít manga đạt điều kiện (thiếu dữ liệu) thì sẽ không đưa vào xử lý.
  - Với mỗi thể loại đạt đủ dữ liệu, chia số manga thuộc thể loại đó ra làm 2 phần bằng median của thời gian kết thúc (`real_end_date`).
  - Tính trung bình mỗi phần rồi so sánh, output sẽ là list những manga được yêu thích gần đây hơn và list những manga được yêu thích ở thời gian trước kia hơn.

> **Kết quả:**

![Q4](./Images/Q4.png)

![Q4-bar](./Images/Q4-bar.png)

#### **_04. More Information:_**
- [Github](https://github.com/duongtruongbinh/Prog4DS_FinalProject)
- [Trello](https://trello.com/b/TL2hTrzA/prog4dsfinalproject)

#### **_05. Planning:_**
- [Planning](https://docs.google.com/spreadsheets/d/1C74QGwhZZZx5uv8j9Z5kSmUOsvY673bq0KFGbLohAOI/edit?usp=sharing
)
