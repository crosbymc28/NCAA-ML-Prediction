# NCAA Men's Basketball Prediction Model

This project is a machine learning model meant to predict the outcomes of NCAA men's basketball games using historical team statistics. This particular instance uses the 2022-2023 season as the historical data and the 2023-2024 season as the test data. The model uses features such as performance metircs in combination with rolling averages to make predictions. The performance metrics are scraped from https://www.sports-reference.com/cbb/. It is built in Python, utilizing Pandas, Scikit-Learn, Beautiful Soup, and NumPy.

**Link to project:** https://github.com/crosbymc28/NCAA-ML-Prediction



## How It's Made

Language: Python

Libraries: Pandas, Scikit-Learn, Beautiful Soup, NumPy

I began the project hoping that I would be able to find a suitable dataset online that I could use, but quickly found that it wasn't going to be that easy and decided it was a great opportunity to learn to scrape the data myself. I decided to use Sports Reference for they have a cohesive and extensive set of data on men's college basketball. This particular model uses the 2022-2023 basketball season as its historical data, so I got the master list of every team participating during that season. I was able to then go through each team and get their game logs of the entire season and compile that information into one large dataset. 

After obtaining the dataset, I wanted to clean it up a little bit. The way that Sports Reference formats their data on their website is that they will repeat the first column with all of the names every so often for readability. The issue with this is that you then have it repeated in the dataset as well, so I wanted to make sure that I removed that before continuing. The dataset also was left with some column naming conventions that I wanted to change so I went ahead and did that as well. After cleaning up the data a bit I went ahead and saved it as a "working" version of the csv.

For the actual machine learning part of the project, I used a radom forest classifier trained on the 2022-2023 men's basketball season. I first had to alter the datatypes of some of the columns as they were not suitable for comparing in my model. During this step, I went ahead and added code versions of some columns to make it easier to work with. I was then able to compile together the predictor columns I wanted to use and create rolling averages of those values. The dataset was then split between the two seasons and given to the random forest classifier. The results were measured in precision with a precision of 66.2%.
