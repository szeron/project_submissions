# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)

# Project 3: Creating a NLP Classification Model
This project explores using PushShift's API to scrape Reddit posts and create a classification model to predict which subreddit a post belongs to. The two subreddits chosen are r/HBO and r/Netflix.
---

## Problem Statement

As part of the data team at HBO, my goal is to explore how I can utilise NLP techniques to gain insights on our audience preferences, and how they compare to those at Netflix. I also wish to identify topics that generate the most engagement and discussion among viewers. These insights will be crucial in future decisions on content development, marketing, and overall strategy.

---

## Methodology

1. Web Scraping
    - Use PushShift's API to scrape Reddit posts from r/HBO and r/Netflix
    - Create a dataframe with the following columns: subreddit, title, selftext
2. Data Cleaning
3. Exploratory Data Analysis
    - Visualise the most common words in the posts from both subreddits
    - Post length distribution
4. Model data
    - Create a baseline model
    - Create a logistic regression model
    - Create a Naive Bayes model
    - Create a Random Forest model
    - Create a Gradient Boosting model
    - Create a Linear SVC model
5. Hyperparameter Tuning
    - Use GridSearchCV to find the optimal hyperparameters for the best performing model

## Limitations

Limitations of our model include:
- Limited training data, if the model was trained on more data, it would be able to learn more about the data and make better predictions.
- Limited resources, if the model was trained on more resources, it would be able to learn more about the data and make better predictions.
- The inherent variability of the data, if the data was more consistent, the model would be able to learn more about the data and make better predictions.

## Conclusions & Recommendations

I will select the Random Forest model with Count Vectorizer as the best model for this project. It has a test accuracy score of 76% and lowest delta between the train and test scores 
This is less detrimental compared to all the other significantly overfitting models.