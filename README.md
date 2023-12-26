# PROGRAMMING FOR DATA SCIENCE - FIT - HCMUS
## Final Project - Thu thập, phân tích cho trả lời câu hỏi về bộ dữ liệu Spotify Tracks Dataset
### I. Group infomation:

Class ID: 21KHDL1

|Student ID|Full Name|
|---|---|
|21127616|Lê Phước Quang Huy|
|21127229|Dương Trường Bình|



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
- **Question 1: How do different genre-related characteristics affect the popularity of songs? (This is an open-ended question)** 
- **Benefits:**
    - **Understanding Audience Trends**: This can be useful in creating music content or events that resonate with the audience.
    - **Planning for Events/Programs**: Knowing which genre is most popular can help you plan your event or program to attract the widest audience.
    - **Supporting Advertising and Marketing**: Optimizing advertising and marketing strategies.
    - **Artist Development Strategy**: For music artists, understanding the current trends and characteristics of different genres can support the development of their strategy, from genre selection to building an image that appeals to the target audience.
- **How to answer this question:**
    - **Analyzing genre has the highest frequency of songs**
![genre has the highest frequency of songs](./image/Q1-1.png)
    > This is the characteristic of the dataset, the author has collected about 1000 songs of each genre to create this dataset.

    - **Top 10 Genres with Highest Average Popularity**
![Top 10 Genres with Highest Average Popularity](./image/Q1-2.png)
    > - Based on the chart, we observe that the highest average popularity score for a genre is approximately 60, not significantly higher than the rest in the top 10.
    > - We also see diversity within each genre, with notable genres including `pop-film`, `k-pop`, `chill`, and `sad`. 
    - **Genres with Highest Average Explicit Ratio**
![Top 10 Genres with Highest Average Explicit Ratio](./image/Q1-3.png)
    > - Based on the chart, the `comedy` genre has the highest `Explicit` ratio by a significant margin.
    > - Genres with a high explicit ratio may attract listeners seeking music with edginess and linguistic freedom.
    - **Genres has the highest number of songs in the top 0.001% (~110) most popular songs**
![Top 10 Genres has the highest number of songs in the top 0.001% (~110) most popular songs ](./image/Q1-4.png)
    > - Based on the chart, in the top `0.001%` of popular songs, there is a large diversity of genres.
    > - The `pop` genre is one of the most popular music genres worldwide.
    - **Genres has the highest ratio of live songs**
![Top 10 Genres with Highest Average Explicit Ratio](./image/Q1-5.png)
    > - Based on the chart, the `comedy` genre has the highest `live` ratio
    > - A high ratio of live songs may reflect the audience's preference for live recordings, with their passion for the lively atmosphere and direct interaction.
    > - Artists and bands often have higher creative freedom during live performances. This can help create unique and more intimate performance versions that resonate closely with the audience.
    - **Correlation between `loudness` and `energy` in the top 3 genres with the highest average popularity**
![Top 10 Genres with Highest Average Explicit Ratio](./image/Q1-6.png)
    > - According to the chart, the correlation between `loudness` and `energy` in the selected top 3 music genres is quite significant. This may imply that songs with high `loudness` also tend to have high `energy` in these genres.

> **Result:** There's no single correct answer to the question posed by our group. Answering this question requires looking at it from various perspectives. Each viewpoint provides different responses suitable for that particular aspect. After this analysis, we hope artists can create hits that become even more widely popular.

- Question 2:

- **Question 3: How can we suggest songs based on a user's current listening preferences?**
- **Benefits:**
    - The goal is to recommend songs to users based on the similarity between songs, helping listeners discover music they might enjoy based on their preferences.
- **How to answer this question:**
    - Utilize Euclidean distance to measure the similarity between songs. The smaller the Euclidean distance, the more similar two songs are from the perspective of the selected features.
    ![Euclidean Distance](./image/Q3-1.png)
    - Select K songs with the smallest distances. These are the songs that the system highly rates in similarity to the user's liked song.
    - Extract information such as song names and artists from the selected songs and return this information as recommendations for the user.

![Recommend](./image/Q3.png)

> **Result:** Recommend the top 5 tracks for the user in descending order of similarity, based on the calculated Euclidean distances.

- Câu hỏi 4:


#### **_04. More Information:_**
- [Github](https://github.com/duongtruongbinh/Prog4DS_FinalProject)
- [Trello](https://trello.com/b/TL2hTrzA/prog4dsfinalproject)
![Trello](./image/trello.png)

#### **_05. Planning:_**
- [Planning](https://docs.google.com/spreadsheets/d/1C74QGwhZZZx5uv8j9Z5kSmUOsvY673bq0KFGbLohAOI/edit?usp=sharing
)
