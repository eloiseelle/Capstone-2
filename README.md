
![mapping the rise 2](https://github.com/user-attachments/assets/2a6e929e-1118-4d85-b80e-b13a77e1cf83)

# Mapping the Rise: Streaming Success of Female Rappers by City

_For decades, female rappers have faced barriers in the music industry, including limited radio play, industry bias and underrepresentation in major playlists. In 2021, women accounted for [23.3% of artists](https://assets.uscannenberg.org/docs/aii-inclusion-recording-studio-2025-01-29-2.pdf) on the Billboard Hot 100 Year-End Chart, compared to 76.7% men. In 2024, their percentage rose to 37.7%, but still showing a male majority. Even though the city of origin is crucial in rap music, shaping everything from sound and style to social commentary and the trajectory of artists’ careers, there are no official city-by-city streaming statistics for female rappers published by major music platforms or industry organizations. So which cities produce successful female rap artists? Is there a connection between a city's representation and its artists' streaming numbers or hit rates? And most of all, which US cities are most likely to produce and sustain female rap talent?_



## 1. Data

•	[Billboard Hot 100 Songs](https://www.kaggle.com/datasets/dhruvildave/billboard-the-hot-100-songs): Provides historical chart performance of songs, allowing to analyze how female rappers have evolved over time in mainstream rankings.

•	[Spotify Top 10k Streamed Songs](https://www.kaggle.com/code/busetmkaya/spotify-top-10000-streamed-songs): Helps in identifying the most streamed songs, enabling a comparison of the streaming success of female rappers versus male rappers.

•	[Spotify Dataset (Popular Hip Hop Artists and Tracks)](https://www.kaggle.com/datasets/kanchana1990/spotify-datapopular-hip-hop-artists-and-tracks): Provides data about artists and songs streaming, allowing to analyze the popularity of female rap artists compared to their male counterparts.

•	[Tidal Playlist of Female Rappers](https://tidal.com/browse/playlist/83ba3531-0c3b-4668-aae0-16009d925d62): Features curated tracks from influential female rappers, offering a qualitative and quantitative look into their music styles and favorite themes.  

•	[Complex Article](https://www.complex.com/music/a/ecleen-luzmila/best-rap-cities-ranking): Best Rap Cities Ranking: Helps contextualize the geographic influence on the success of female rappers by mapping their origins to top ranked hip hop cities.


## 2. Methodology

1. **Data Cleaning**  
   Standardized artist names, merged datasets, removed non-rappers (e.g., Beyoncé, Rihanna), and filtered for female artists only.

2. **Feature Engineering**  
   Created variables such as `total_mentions` from track counts across platforms.

3. **Visualization**  
   Built key charts including:


Top Female Rappers by Total Mentions<br/><br/>
<img width="1142" height="590" alt="top 10 female rappers" src="https://github.com/user-attachments/assets/0a0ca272-4e05-4c5b-8b2b-42802293c7a7" />

   

Top Cities by Female Rapper Presence<br/><br/>
<img width="1153" height="584" alt="top 10 cities" src="https://github.com/user-attachments/assets/09e52589-cab7-40c9-ab39-53b9fd6c2365" />

   



Confusion Matrix<br/>

<img width="545" height="453" alt="confusion matrix" src="https://github.com/user-attachments/assets/9bc9705d-f47b-4f88-9bb1-8687c45d7510" />




4. **Modeling**  
   Trained a RandomForestClassifier to classify track success likelihood based on artist/city metadata.


## 3. Results

- **Nicki Minaj (NYC)** is #1 across all platforms witg the highest total track mentions.
- **NYC, Houston, and Los Angeles** emerge as the strongest cities for female rap.
- Playlist and chart presence strongly correlate with success.
- Model achieved:
  - **Accuracy**: 66%
  - **Precision**: 0.74
  - **Recall**: 0.66
  - **F1-score**: 0.63


## 4. Recommendations

- We should prioritize NYC, Houston and LA as primary talent scouting locations for female rappers. 
- As playlist inclusion rates are strongly linked to the rappers' success across cities, we should definitely use them to identify breakout artists.
- We should use geographic insights to optimize promotional strategies, focusing on areas with the highest predicted artist potential.

## 5. Future work

- It would be interesting to look at other features such as lyrics, track duration and collaborations to improve the modeling.
- We could use other algorithms and approaches to try to improve the model performance.
- We could expand the dataset and explore international cities to track global female rap growth.
