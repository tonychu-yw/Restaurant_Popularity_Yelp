# Popularity Forecast with Yelp Dataset

### Note

This repo contains the final group project for IMT 575 Data Science III in SPR20 at UW, co-authored by Chiao-ya Chang, Chen Song, Tony Chu, and Xinyi Yang. 

### I. Introduction
Yelp is a public company that develops, hosts, and markets Yelp.com and Yelp mobile app, which publish crowd-sourced reviews about businesses. As a great platform choosing consumer activities, Yelp provides pages devoted to information about restaurants and stores, allowing users to use a one-to-five-star rating system to evaluate products and services and to provide meaningful and detailed reviews about their experience (Chafkin, 2010). On one hand, users can make their decisions between similar restaurants or services based on the ratings and reviews shown on the Yelp pages. On the other hand, business owners can get an overall assessment of their restaurant's performance based on the reviews and ratings on Yelp and they can also further leverage the same massive dataset to analyze users to generate business insights for wiser decisions. Our project goal is to predict the popularity of restaurants. We used several machine learning methods including logistic regression, Naive Bayes, xGBoost, CNN, and LSTM to make predictions of popularity.

##### I-1. Motivation
Consider the following scenario: you just opened a restaurant a few months ago, and luckily it already had quite an amount of customers. However, since there are still a few seats left empty during mealtime, you wonder if your restaurant will continue to grow. Therefore, it would be great for you, the restaurant owner, to know how popular the restaurant will be in the future. If the restaurant cannot increase its popularity in the future and is still not making any profit, it might be better to halt the business now. We believe such a scenario happens quite often for many local restaurant owners, and the information garnered from Yelp should help business owners make those difficult business decisions. Besides, customers can choose a restaurant that is not only popular right now but also in the future, and investors can use data from yelp as reference to know whether a restaurant is worth an investment or not. 

##### I-2. Research Question
Our main research question is: how popular will a restaurant be in the future? Please note that this question is formed with caution. The popularity of a restaurant is not an unbiased estimator for the profitability of a restaurant. However, since (1) it is almost impossible to retrieve financial data from local restaurants (they are very unlikely to have standard income statements) and (2) financial status may be affected by several other issues that have no direct link to the service that a restaurant provides, we feel that it is more appropriate to use popularity instead of profitability to estimate how well a restaurant operates. We are more interested in researching the relationship between the growth of a restaurant provided by its current services. Given our popularity forecast, restaurant owners should be able to further calculate their own profitability easily. The following lists some sub-questions that we are interested in or we must deal with during our research:
* How popular will a restaurant be in the future?
* How to define popularity? That is, what is the appropriate metric for popularity?
* What features can be used to predict popularity?
* How do different features impact the performance of predictions?
