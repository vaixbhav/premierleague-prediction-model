# Premier League Prediction Model

As of January, 2024 half of the 2023/2024 season has been played. Utilizing match statistics of all matches played so far in the season, I constructed a prediction model for the remaining matches in the season. Match outcomes were predicted utilizing match statistics scraped from the open-source website: [https://fbref.com/en/comps/9/Premier-League-Stats](https://fbref.com/en/comps/9/Premier-League-Stats).

## Data Collection Through Web Scraping
Match data was scraped in `scrapingfbref.ipynb` using the main Python libraries: requests, BeautifulSoup and Pandas. Each Premier League team's data was stored in a Pandas DataFrame and merged. Scraped data was concised to include essential information and converted to a CSV file `matchstats.csv` in preparation for predictive modelling. 

## Prediction Model
Machine learning library scikit-learn was used in `predictionmodel.ipynb` for data analysis of `matchstats.csv`. Elements that were considered for match outcome prediction included goals for/against, shooting stats, freekick/penalty percentages, home/away outcomes, and expected goals.  Random Forest algorithm was applied to assess training data, providing an accuracy outcome of 55.4% based on the 317 matches played up to date. Rolling average statistical method was also used to compare accuracy, resulting in a 50% outcome. Another iteration of results will be updated as the season moves further on, allowing for additional data points and thus a more accurate prediction outcome.
