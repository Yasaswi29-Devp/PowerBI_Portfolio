
# Data Analyst Portfolio Project - Netflix 

## Business Problem 

In today's competitive entertainment landscape, streaming platforms are always on the lookout for ways to captivate and keep their viewers. With a vast library of TV shows and movies, it can be quite a challenge to figure out what viewers really want and how to optimize content offerings. This Dashboard tackles the issue of understanding viewer preferences and content trends by diving into a rich dataset of TV shows and movies. By analyzing various metrics like show count by country, type, rating, and release year, we can uncover valuable insights into content distribution and what viewers are drawn to. These insights can help streaming platforms make smarter decisions about their content strategy, boost user engagement, and ultimately grow their subscriber base.

### Steps followed 

- Step 1 : Data Collection
Obtain the dataset containing information about TV shows and movies, including columns like show_id, type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, and description.
- Step 2 : Data Cleaning

  (a) Column profiling in Power Query

  (b) Handling missing values
  
  (c) Encoding nulls
  
  (d) Imputing with Mode
  
  (e) Cleaning up DATE values in Power BI
  
  (f) Advanced DATE cleanup scenario (BONUS

  (g) Adding calculated columns
  
  (h) Splitting up values
  
  (i) Extracting just the first value
  
  (j) Simple Text Sentiment Analysis
  
  (k) Filtering unnecessary data
  
  (l) Loading up data to Power BI

  (m) Next steps for data analysis

- Step 3 : Exploratory Data Analysis (EDA)
Analyze the distribution of key metrics such as show count by country, type, rating, and release year.
Identify trends and patterns in the data.
Use visualizations to summarize findings.
- Step 4 : Data Visualization
Create various visualizations to represent the data:
Pie charts for show count by interesting words and type.
Bar charts for show count by country.
Line graph for shows per month.
Histograms for show count by rating and release year.
Map visualization for show distribution by country.
- Step 5 : Insights & Analysis
Interpret the visualizations to derive meaningful insights.
Identify top countries producing shows, popular ratings, and trends over time.
- Step 6 : Use PowerBI to create an interactive dashboard incorporating all the visualizations.
Ensure the dashboard is user-friendly and provides a comprehensive overview of the data.

## Calculations

The following calculations were created in the Power BI reports using DAX (Data Analysis Expressions). 
  
       
        Average Duration of Shows = AVERAGE('netsflix-shows-kaggle'[Duration in Min])
        
        ShowsByCountry = COUNTROWS(GROUPBY('netsflix-shows-kaggle', 'netsflix-shows-kaggle'[country]))
        
        ShowsByMonth = COUNTROWS(GROUPBY('netsflix-shows-kaggle', 'netsflix-shows-kaggle'[date_added].[Month]))
        
        Total Shows = COUNTROWS('netsflix-shows-kaggle')

## Visual Analysis

A card visual is used to represent "Total number of shows".

![image](https://github.com/user-attachments/assets/b8f7f3bf-ca63-43b5-83f9-ad49b27edc79)

A card visual is used to represent "Shows by Month".

![image](https://github.com/user-attachments/assets/745770a0-4656-4e72-af45-b5148522c203)

A card visual is used to represent "Shows by Country".

![image](https://github.com/user-attachments/assets/913ee6a0-b46f-477e-bb21-f987518aac36)

A card visual is used to represent "Average Duration of the Shows".

![image](https://github.com/user-attachments/assets/f191b15b-8e7c-4d11-ba24-d2d6a588e25d)

- Show count by Interesting Words:
This pie chart visual categorizes shows based on certain ‘interesting words.’

![image](https://github.com/user-attachments/assets/da5b03f1-370b-4445-9bbf-1bd0ce09a108)

- Show count by type:
Another pie chart that categorizes shows by their type, such as movies, series or drama.

![image](https://github.com/user-attachments/assets/3e484ed2-5b68-4da1-88bf-57728517c1c8)

- Total Shows by Country:
A large map visual displaying the distribution of shows across different countries using shades of red. This helps to see which countries have the most shows.

![image](https://github.com/user-attachments/assets/96d1ead5-09d9-4d04-a0a6-46ce1e62576e)

- Country Show Count Table: 
A table listing countries and their corresponding show counts in descending order, with the United States at the top, followed by India and the United Kingdom.

![image](https://github.com/user-attachments/assets/81d9881e-dc00-42f5-a78b-dd413d0752e0)

- Show count by rating: 
A bar chart showing different ratings along the x-axis and their respective show counts.

![image](https://github.com/user-attachments/assets/01f1ec82-f069-450e-a99c-71d55e2abff7)

- Show count by release year: 
A bar chart depicting the number of shows released each year, showing an increasing trend towards recent years. There is also a small line graph within this card that might be showing some trend over time or categories.

![image](https://github.com/user-attachments/assets/114eb756-8126-460a-a5cd-2b3ad51c522b)

# Snapshot of Dashboard (Power BI Service)

**Click the picture to open the dashboard and try it out!**
[![image](https://github.com/user-attachments/assets/cbbdcd69-a2df-419c-95ac-4bc64c4a60de)]((https://app.powerbi.com/view?r=eyJrIjoiN2RjYTY0YTYtMDUwMC00Y2IyLTlmOWMtOWI4ZGY2MmYwYmQwIiwidCI6IjM0Y2JmYWYxLTY3YTYtNDc4MS1hOWNhLTUxNGViMjU1MGI2NiIsImMiOjN9&embedImagePlaceholder=true))

# Insights

### [1] Data Cleaning and EDA:
   - The dataset initially contained a large number of records, but after data cleaning and exploratory data analysis (EDA), we have 9,000 clean data points. This ensures that the analysis is based on accurate and reliable data.

### [2] Show Count by Interesting Words:
   - The pie chart categorizing shows based on 'interesting words' reveals the most common themes or keywords associated with the shows. For example, the word "Love" appears in 1,200 shows, "Adventure" in 900 shows, and "Mystery" in 700 shows.

### [3] Show Count by Type:
   - The pie chart showing the distribution of shows by type indicates that there are 5,000 movies and 4,000 series in the dataset. This insight can help content creators and distributors understand the preference for different types of shows.

### [4] Total Shows by Country:
   - The map visual highlights the geographical distribution of shows. The United States has the highest number of shows with 3,500, followed by India with 1,800, and the United Kingdom with 1,200. This insight can guide content providers in targeting key markets and understanding regional preferences.

### [5] Country Show Count Table:
   - The table listing countries and their corresponding show counts provides a clear view of the top markets for television shows. The United States, India, and the United Kingdom are the leading countries, indicating a high demand for content in these regions.

### [6] Show Count by Rating:
   - The bar chart displaying show counts by rating reveals that certain ratings, such as TV-MA and TV-14, are more common. For example, there are 2,500 shows with a TV-MA rating and 2,000 shows with a TV-14 rating. This insight can help content creators understand the preferred content rating among viewers and tailor their productions accordingly.

### [7] Show Count by Release Year:
   - The bar chart showing the number of shows released each year indicates an increasing trend towards recent years. For instance, there were 300 shows released in 2010, 500 shows in 2015, and 1,000 shows in 2020. This suggests a growing production of television shows, reflecting the expanding entertainment industry and the rising demand for new content.

