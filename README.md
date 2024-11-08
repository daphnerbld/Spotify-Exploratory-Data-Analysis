# Exploratory Data Analysis on Spotify 2023 Dataset

In this deliverable, you will perform an exploratory data analysis (EDA) on a dataset containing information about popular tracks on Most Streamed Spotify Songs 2023

## I. Intended Learning Outcomes
1. This task aims to analyze, visualize, and interpret the data to extract meaningful insights.

## II. Materials Used
1. [Spotify 2023 Data]( https://www.kaggle.com/datasets/nelgiriyewithana/top-spotify-songs-2023)
2. Jupyter Notebook
3. ChatGPT

## III. Table of Contents
1.	Overview of Dataset
2.	Basic Descriptive Statistics
3.	Top Performers
4.	Temporal Trends
5.	Genre and Music Characteristics
6.	Platform Popularity
7.	Advanced Analysis

## IV. Performing Exploratory Data Analysis 
**Importing necessary libraries**
``` js
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```
**Loading the corresponding .csv file into a data frame named 'df' using the code:**
```
df = pd.read_csv('spotify-2023.csv')
```
> [!IMPORTANT]
> *When the code took too long to run / doesn’t execute, I added ``` encoding='latin-1'``` in the parameter d in Latin-1 to ensure that all characters are interpreted accurately.*

>**1. Overview of Dataset**

In this part, we are going to find the number of rows and columns that the dataset contains as well as the data types of each columns and its missing values. Utilizing ```df.shape``` for efficiency in retrieving dimensions, ```pd.DataFrame``` for structured and expandable storage, labeled columns for clarity, and ```style.set_table_attributes()``` for readability

![image](https://github.com/user-attachments/assets/ccdf82b2-6455-429b-b431-6e6bb5d7b451)

___Figure 1.1___ _shows the number of rows and columns_

![image](https://github.com/user-attachments/assets/903fa5d7-5013-41cd-8d37-4418ecb59ef7)

___Figure 1.2___ _shows the data types of each columns_

![image](https://github.com/user-attachments/assets/655aea69-2aef-4fc0-a59c-b4a7e26b25ff)

___Figure 1.3___ _shows the missing values_


>**2. Basic Descriptive Statistics**

This part provides the data of mean, median and standard deviation, using ```pd.to_numeric()``` to ensure all values in the ```streams``` column are numeric, converting any non-numeric values to ```NaN``` to handle inconsistencies gracefully. Next, ```dropna()``` removes any rows where streams contains ```NaN```, resulting in a clean dataset with only valid numeric values for further analysis.

Mean: 514137424.93907565

Median: 290530915.0

Standard Deviation: 566856949.0388832

Additionally, it provides a visualization of the distribution of released year and artist count.  The trend reveals a steady increase in the number of tracks released over the years, reflecting the growing popularity of music streaming on platforms like Spotify and an expanding global music market.

![image](https://github.com/user-attachments/assets/f963d984-69a0-4b3e-bbd9-aeef4f4acddc)

___Figure 2.1___ _shows the distribution of released year_

![image](https://github.com/user-attachments/assets/74bb21b7-32a0-40d6-afb0-17b30760b803)

___Figure 2.2___ _shows the distribution of artist count_


>**3. Top Performers**

This part shows which track has the highest number of streams and the top 5 most frequent artists based on the number of tracks in the dataset. Blinding Lights by The Weeknd has a total number of 3.7B streams making it the most streamed track on spotify 2023.

![image](https://github.com/user-attachments/assets/58c4ed48-4dda-4d97-a8f1-9c03716170df)

___Figure 3.1___ _shows the top 5 most streamed tracks_

![image](https://github.com/user-attachments/assets/5dd005a4-bc17-4ce4-adb2-4df6437c8664)

___Figure 3.2___ _shows the top 5 most frequent artists_

> **4. Temporal Trends**

This part allows us to analyze the trends in the number of tracks released over time and observe noticeable patterns.

![image](https://github.com/user-attachments/assets/b935fe5f-a110-405d-aea8-84a1c215d432)

___Figure 4.1___ _shows the number of tracks released per year_

In this bar chart, we see a significant increase in the number of tracks released per year, especially in recent years. The increase is gradual from the early years until around the 2010s, after which the number of releases sharply rises, particularly in 2022 and 2023. This trend could reflect the growing accessibility of music production and distribution technologies, as well as an increasing interest in music creation.

![image](https://github.com/user-attachments/assets/0f082c56-d05a-4583-a79c-0c990a72a85e)

___Figure 4.2___ _shows the number of tracks released per month_

The chart shows that January has the highest number of track releases, peaking at over 120, followed closely by May. There are moderate fluctuations throughout the year, with notable increases in October and November, while February and September have fewer releases, indicating lower activity. Overall, the data suggests a trend of high releases at the beginning of the year and some resurgence toward the year's end.

>**5. Genre and Music Characteristics**

In this part, we are to examine the correlation between streams and musical attributes like bpm, danceability_%, and energy_%.

![image](https://github.com/user-attachments/assets/bcd970d2-b788-4905-a1f2-6cf04a87efe3)

___Figure 5.1___ _shows the correlation matrix of streams and musical attributes_

![image](https://github.com/user-attachments/assets/a774fabf-f6d4-40b9-83fd-0bbd82415df1)

___Figure 5.2___ _shows the heatmap correlation matrix of streams and musical attributes_

Through this, we found out that:

Correlation between Danceability and Energy: 0.20

Correlation between Valence and Acousticness: -0.08

These low correlation values imply that danceability, energy, valence, and acousticness are largely independent attributes in this dataset, with only minor relationships between them.

>**6. Platform Popularity**

This part compares the numbers of tracks in spotify_playlists, spotify_charts, and apple_playlists and which platform seems to favor the most popular tracks.

![image](https://github.com/user-attachments/assets/12c31988-8981-4392-9b1b-f6cf37616c08)

___Figure 6.1___ _shows number of tracks in different platforms_

![image](https://github.com/user-attachments/assets/82c7c06a-a573-4f5b-bf76-d7ebdbc8a89f)

___Figure 6.2___ _shows number of tracks in different platforms_

The chart indicates that Spotify Playlists overwhelmingly dominate with nearly 5 million tracks, whereas Spotify Charts and Apple Playlists have significantly fewer tracks, almost negligible in comparison. This suggests that Spotify Playlists have a vastly larger catalog or user engagement, making it the platform that likely favors the widest variety of tracks.

>**7. Advanced Analysis**

And lastly, this part shows patterns among tracks with the same key or mode and allows us to compare the most frequently appearing artists in playlists or charts. 

![image](https://github.com/user-attachments/assets/91dddb71-cae6-4f68-8f04-4e230c2ebed3)

___Figure 7___ _shows the average streams by key_


## V. Author

Daphne P. Robleado

2ECE-A
