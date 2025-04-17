# Capstone Project: Mapping the Rise: Streaming Success of Female Rappers by City

## Objective

This project analyzes multiple music datasets to identify the most streamed and culturally impactful female rappers by US city. 
By combining data from Spotify, Billboard, TIDAL, and other sources, the goal is to highlight regional hubs of female rap and spotlight key artists leading the genre. The ultimate goal is to use these insights as the foundation for building a machine learning model that can predict future hits by female rappers, based on trends in city representation, streaming behavior, playlist inclusion, and historical performance metrics.

## Datasets used

- 'tidal_female_rappers_with_city.csv' – Manually curated playlist of female rap tracks, compiled from a TIDAL playlist.
- 'spotify_top_hiphop_artists_tracks_cities.csv' – Spotify hip hop tracks (ChatGPT added 'gender' and 'city' columns).
- 'spotify_top_10k_streamed_songs.csv' – Most streamed songs on Spotify (ChatGPT added 'gender' and 'city' columns).
- 'complex_best_rap_cities.csv' – Manually built dataset based on Complex's editorial ranking of best rap cities.
- 'billboard_hot_100_with_city.csv' – Billboard Hot 100 data with artist 'gender' and 'city' information.

## Step-by step process 

1. Loaded and cleaned all datasets, adding different separators after dealing with formastting issues.
2. Standardized city names (merging "Brooklyn" and "Queens" into "NYC").
3. Filtered for female artists (using the 'gender'column).
4. Grouped by 'artist' and 'city_clean' to count how often each female rapper appeared in each dataset.
5. Merged all datasets into one.
6. Cleaned artist names:
- Stripped whitespace and standardized capitalization.
- Corrected mislabeled entries ("j": "doja cat").
- Removed non-female rappers (singers like Beyoncé, Rihanna and male rappers wrongly classified as female).
7. Calculated total mentions per artist per city.
8. Sorted and visualized the final ranking of top female rappers.

## Final results

- Nicki Minaj (NYC) is #1 across all platforms with the highest total track presence.
- Cardi B (NYC), Doja Cat (Los Angeles), and Megan Thee Stallion (Houston) are in the top 4.
- NYC emerges as the strongest city for female rap, followed by Houston and Los Angeles. 

## Output files

- 'top_female_rappers_by_city_cleaned.csv': final dataset with the results. 
- Visualization available in the notebook.
