# NBA Game Machine Learning Predictor
In this project, I webscraped the entirety of the 2022-2023 and 2023-2024 NBA season from Basketball Reference. I read in the data and cleaned it up with BeautifulSoup. I then used the boxscores, taking the aggregate statistics (e.g., eFG%, TS%, APG) of the entire team and saving it into a CSV file using Pandas. I then used a Ridge Regression model to determine the useful factors in order to predict the 2023-2024 season based on the 2022-2023 season's data and compared it to the actual results. Lastly, I improved accuracy by factoring in momentum and each team's Last 15 Game Performances.

With the original baseline model (just raw statistics), I achieved an accuracy of approximately 57%. However, with the factored-in momentum as well as added-in opponent information, I achieved an accuracy of approximately 64%. This marks a near 12.3% increase in accuracy.

This is a complete end-to-end project, and I used web scraping, data cleaning, and machine learning, with technologies such as JupyterNotebook, Pandas, Sci-kit learn, BeautifulSoup, and Selenium.

## File overview:
* `get_data.ipynb` - Webscraped the box scores from https://www.basketball-reference.com .
* `parse_data.ipynb` - Parse through and clean the data to get a pandas DataFrame in the form of a CSV file.
* `predict.ipynb` - Make predictions using machine learning and adapt.
