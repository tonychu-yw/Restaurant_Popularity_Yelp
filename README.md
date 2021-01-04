# Restaurant Popularity Forecast with Yelp Dataset

### Preface



### I. Restaurant Popularity
Consider the following scenario: you just started a restaurant a few months ago, and luckily it already had quite an amount of customers. However, since there are still a few seats left empty during mealtime, you wonder if your restaurant will continue to grow. Therefore, it would be great for you, the restaurant owner, to know how popular the restaurant will be in the future. If the restaurant cannot increase its popularity in the future and is still not making any profit, it might be better to halt the business now. We believe such a scenario happens quite often for many local restaurant owners, and the information garnered from Yelp should help business owners make those difficult business decisions. Besides, customers can choose a restaurant that is not only popular right now but also in the future, and investors can use data from yelp as reference to know whether a restaurant is worth an investment or not. 

We hope to answer the quesiton: *how popular will a restaurant be in the future?* Please note that this question is formed with caution. The popularity of a restaurant is not an unbiased estimator for the profitability of a restaurant. However, since (1) it is almost impossible to retrieve financial data from local restaurants (they are very unlikely to have standard income statements) and (2) financial status may be affected by several other issues that have no direct link to the service that a restaurant provides, we feel that it is more appropriate to use popularity instead of profitability to estimate how well a restaurant operates. We are more interested in researching the relationship between the growth of a restaurant provided by its current services. Given our popularity forecast, restaurant owners should be able to further calculate their own profitability easily. The following lists some sub-questions that we are interested in or we must deal with during our research:
* How popular will a restaurant be in the future?
* How to define popularity? That is, what is the appropriate metric for popularity?
* What features can be used to predict popularity?
* How do different features impact the performance of predictions?

### II. Popularity Definition
To define popularity, we use the following variables: average stars and the number of restaurant reviews. We subtract average stars by three for normalization and take natural log to reduce the effect of the high number of reviews and to minimize computational complexity. Thus, the formula of our popularity definition is: *popularity = (average star − 3) × log (number of reviews)*. In this project, we calculate the popularity of restaurants in 2019 on a yearly basis. That is, we use data in 2018 to predict how popular a restaurant will be in the year of 2019 (in a time interval manner). The following figure shows the distribution of restaurant popularity, which follows Gaussian distribution.

Please note that we further converted continuous popularity scores to 5-class ordinal labels to help us make predictions easier since we faced major failures while predicting continuous outcomes. Our cut points are 20-quantiles, 40-quantiles, 60-quantiles, and 80-quantiles. We ranked 5 as the highest popularity (i.e., greater than 80 quantiles) and 1 as the lowest popularity (i.e., less than 20 quantiles).
