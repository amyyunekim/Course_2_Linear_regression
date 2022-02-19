

## Predicting WNBA Salaries

### Abstract:
The goal of this project was to predict Women's National Basketball Association (WNBA) players salaries and in turn their potential value in the league.
Data was acquired through webscraping including salary data from Spotrac and player statistics from basketball-reference.com. A linear regression model was fitted on player statistics with salary as the target. Training and testing data sets were used with KFolds used for cross validation. A R squared value of xxx was achieved.

### Design: 

The analysis was conducted in a two part phase.

<i> 1. Correlations </i>

Investigated whether we can observe a relationship between precipitation and entries via a correlation calculation for daily precipitation vs overall daily entries/exits for 2021. 


<i> 2. Interday Movement </i> 

A deep dive into two storm days was conducted: 9/1/2021 when Hurricane Ida passed over NYC which had the highest daily precipitation (172.7mm), and 10/26/2021 which had the second highest daily precipitation (63mm). 

Both storm days were preceded by a day with no precipitation so the no precipitation day was used as a baseline for comparison. 

### Data:
WNBA data is sparse compared to the NBA and only has salary data from 2016 on the Spotrac [website](https://www.spotrac.com/wnba/rankings/2021/base/). Salary data from 2016 to the most recently finished season 2021 was extracted using Selenium and player statistics were pulled for the same time period 2016 - 2021 seasons from basketball-reference.com for [Total Stats](https://www.basketball-reference.com/wnba/years/2021_totals.html), [Per Game Stats](https://www.basketball-reference.com/wnba/years/2021_per_game.html) and [Advance Stats](https://www.basketball-reference.com/wnba/years/2021_advanced.html) using BeautifulSoup. 



### Algorithms:

As per the two part phase described above.

<i> 1. Correlations</i>

- The total entries/exits were grouped and summed for each day and a correlation was run against daily precipitation.

- Correlations were also calculated on a more granular station level by grouping entries/exits by station and day and then running a correlation against daily precipitation. 

<br>

<i> 2. Interday Movement </i>

- Total daily entry/exits were calculated per station and then difference between total daily entry/exits from one day to the next was calculated for each station.  

- The top 10 stations which were most impacted by passenger movement from the previous day were found. These stations were analysed further on an hourly basis by looking at the movement between the same time stamp from the previous day. e.g. the difference between 8/31 8pm and 9/1 8pm was calculated. 

- These movements were graphed on top of precipitation using Matplotlib and Seaborn as a timeseries to visualise any pattern in movements. 



<br>


### Tools:
- Selenium and Beautiful Soup for webscraping
- Pandas and NumPy for data manipulation  
- Matplotlib and Seaborn for plotting
- StatsModels and skLearn for linear regression