# Analysis of Yelp Review Data

In this project, we will be analyzing Yelp's business, reviews, and user data. This dataset was downloaded from [Kaggle](https://www.kaggle.com/yelp-dataset/yelp-dataset) and pulled into a public S3 bucket to use: `s3://aws-logs-468088799092-us-east-2/elasticmapreduce/`

This analysis answers two questions: 1) Do Yelp Review Skew Negative? and 2) Should the Elite be Trusted?

To analyze whether Yelp reviews skew negative, we load review and business data from S3. Then we combine the two to create a new dataset that contains both business and review information. We create a new column with the average rating of each business, and calculate the skew from each review for the business. When we graph our results, we can see that there is a normal distribution, meaning that there is no skew between reviews and average business ratings. 

To analyze how accurate Yelp Elite user ratings are the average business rating, we load in user data from S3. For this analysis, we're only looking at users who were Yelp Elite in 2019. We combine this data with the previous review and business dataframes and calculate the skew between the Yelp Elite user's rating and the average rating for each business. When we graph our results, we can see that there is a negative skew, meaning that Yelp Elite users tend to rate business lower than the average user. 
