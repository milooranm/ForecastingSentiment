
# Forecasting average sentiment of social media posts

![License](https://img.shields.io/badge/license-CC0%201.0-brightgreen.svg) <!-- Update the license badge as needed -->

A project investigating a dataset of 1.6M Tweets made by users over a specific time period.

- An project undertaken as part of  my M.Sc.
- Was asked to find the average sentiment of the tweets over time
- Asked to forecast the sentiment for a range of different time intervals
- Tasked with creating an interactive dashboard for the forecasts using python.


The project report as submitted to my college is included [Here](Forecasting_social_media_sentiment.pdf)

---

## Table of Contents

- [Description](#description)
- [Methodology](#methodology)
- [Technologies](#technologies)
<!-- [Installation](#installation)
- [Usage](#usage)
- [Acknowledgments](#acknowledgments)
-->
---

## Description
This project focuses on analyzing the sentiment of a dataset of tweets and forecasting future sentiment trends using time series analysis. The project leverages big data storage and processing techniques, with Python as the primary programming language. Key components include sentiment analysis using the VADER library, data imputation for missing values, and time series forecasting using both Holt-Winters Exponential Smoothing.

The techniques implemented in the project could be used to:
- Analyze the sentiment of tweets to understand public opinion trends.
- Predict future sentiment trends.
- Identify social media users who contribute significantly to overall sentiment in an online space, either positively or negatively.
- Handle missing data in the time series to improve the accuracy of forecasts.

Limitations of the project:
- The tweets were selected specifically for the purposed of creating a bespoke dataset that would require additional problem solving to manage, and as such the dataset is synthetic.
- A significant portion of the data is missing, which reduces validity of forecasts.
- The method of tweet selection introduced bias, affecting the representativeness of the sentiment analysis.
- The forecasting models struggle a little with the sudden inversion of sentiment towards the end of the dataset, leading to less accurate predictions.

Potential Future Features:
- Implement real-time sentiment analysis and forecasting for dynamic datasets.
- Develop methods to identify and further correct for potential biases in the tweet selection process.
- Enhance the dashboard with additional interactive features and clearer visualizations.


 
 ## Methodology
  
- Applied sentiment analysis to each tweet
- Found out which users were disproportionally responsible for sentiment change -> Identified bot accounts that constantly posted the same tweets, skewing sentiment
- Made visualisations of the frequency of tweets as well as the average sentiment by day and by hour for visual inspection -> Identified a complete inversion of average sentiment after a certain time period, revealing that the data was actually artificially selected based on sentiment from a larger set of data.
- Developed a strategy for imputation of missing values that minimised information loss and accounted for selection bias
- Created forecasts for the average sentiment based on scenarios where the inversion of sentiment was either permanent or temporary, using Holt-Winters Exponential Smoothing
- Designed an interactive dashboard to run in a python notebook that would display forecasts made for the scenario where the inversion is temporary, for a user specified number of days.


---

## Technologies

The project uses the following technologies:

- Python
- Pandas
- NumPy
- NLTK
- Scikit-learn
- Jupyter Notebook


---
## Repository Contents
- Sentiment and imputation.ipynb - Exploratory data analysis, sentiment analysis, imputation of missing values
- TSA and forecasting.ipynb - Implementing and tuning TSA models, creating forecasts
- Dashboard.ipynb - Creation of a dashboard within jupyter notebook
- AverageDailySentiment.txt - The avergage daily sentiment as produced via sentiment analysis, ready for use in a new notebook
- README.md - This  file
- high_resolution_graph.png - an image with higher resolution than possible inside jupyter
- no space added.png - another HD image for use in examining patterns in the data.
- LICENSE - Creative Commons license
