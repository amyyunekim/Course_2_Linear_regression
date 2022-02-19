
## Question/Need:

What is the question behind your analysis or model and what practical impact will your work have?

- Predicting WNBA players salaries to value players. 

Who is your client and how will that client benefits from exploring this question or building this model/system?

- The WNBA is my client. The WNBA enters contract negotiations every year so it would be useful to predict the value of players based on statistics.

## Data Description:

What dataset(s) do you plan to use, and how will you obtain the data? Please include a link! (The link can be to the dataset you’re downloading, the site you’re scraping, etc.)

- WNBA Player Stats for 2017 - 2021:
https://www.basketball-reference.com/wnba/years/2021_totals.html

- Active WNBA contract data:
https://www.spotrac.com/wnba/rankings/2021/base/ 

-  If there is time I would like to compare to NBA salary drivers to compare and contrast which statistics are more valued in each league.

What is an individual sample/unit of analysis in this project? In other words, what does one row or observation of the data represent?
- one player's season statistics + salary

What characteristics/features do you expect to work with? In other words, what are your columns of interest?
- Player stats. e.g. minutes played, field goals made, field goal %... etc. 

If modeling, what will you predict as your target?
- WNBA player salary for 2022

## Tools:

How do you intend to meet the tools requirement of the project?
- Beautiful Soup for webscraping
- Statsmodels for regression analysis 
- Seaborn for inspection and visualization of data

Are you planning in advance to need or use additional tools beyond those required?
- not at this point