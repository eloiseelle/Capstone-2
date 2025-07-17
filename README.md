
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

### 1. Data wrangling  
Used a mix of manual review and AI tagging to add missing gender and city info. Normalized cities (Harlem and Brooklyn → NYC) and removed non-rap artists like Beyoncé and Rihanna.

### 2. Exploratory data analysis (EDA)  
Explored distributions, top cities, and artist frequency across platforms using histograms and bar charts. 

### 3. Preprocessing  
Grouped artists by city and platform and labeled artists as "hit = 1" if they had 5+ mentions. Applied one-hot encoding, scaling, and handled missing values.

### 4. Modeling  
Trained a Random Forest Classifier to predict hits from city and platform features. 

### 5. Visualization  
Created visual summaries such as:

   - Top female rappers by total mentions
     
      <img width="1120" height="589" alt="top female rappers" src="https://github.com/user-attachments/assets/a024ba8b-db10-4b3a-a90a-fb6f536888a9" />


   - Leading cities for female rapper success
     
     <img width="1151" height="561" alt="hits by city" src="https://github.com/user-attachments/assets/fae52c7b-c3d6-4341-9648-2a01be01abbe" />


   - Confusion Matrix for model results
     
     <img width="565" height="463" alt="confusion matrix" src="https://github.com/user-attachments/assets/b20cf6ff-d31f-46ff-825f-d8b363ce6cff" />


   - Duration of female rap tracks
     
     <img width="965" height="552" alt="track duration" src="https://github.com/user-attachments/assets/1aa42eb5-24d7-4825-adc2-6bb4517997b8" />



## 3. Results

- **Nicki Minaj (NYC)** had the highest total mentions across all platforms.  
- **NYC, Houston, and LA** were the top cities for female rapper success.  
- **Billboard and Spotify Top 10k** were most strongly correlated with hit status.  
- **TIDAL and Complex** offered qualitative insights but less predictive value.  
- Model results show promise, though further validation on larger samples is recommended.

## 4. Recommendations

- **Scout where it counts**: Focus A&R efforts on NYC, Houston, LA, and Atlanta.  
- **Watch early platform momentum**: Use Spotify 10k and Billboard as early breakout signals.  
- **Use predictive tools**: Combine city and platform data for scalable artist discovery.

## 5. Future work

- Add features like lyrics, mood, collaborations, and tempo.
- Explore international scenes (e.g., the UK, France, Brazil, South Africa).
- Incorporate TikTok and social media virality metrics.
- Use advanced ML models (e.g., XGBoost) for better prediction.
- Build a dashboard for label teams to explore artist metadata and predictions.
