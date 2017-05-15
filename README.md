# Review-Rating-Prediction

The task is to predict the ratings based on the 5-core [dataset](http://jmcauley.ucsd.edu/data/amazon/) of reviews for movies and TV on Amazon, in which all users and items have at least 5 reviews. When I first saw the dataset, two different types of models come to my mind. The first type is matrix factorization model based on the reviewer-item ratings, which is widely used in recommender system. The second type is a text classifier based purely on the review text content. It is essentially sentiment analysis for this kind of rating problem. I  first tried both type of models independently, and then checked if combination of two models can lead to better performance. 

I found that the logistic regression model based on review (including summary) text is most effective to predict the class correctly (highest accuracy). The matrix factorization model alone has worse accuracy and worse root mean square error (RMSE) than logistic regression, but combining matrix factorization prediction into logistic regression prediction can leads to a better RMSE score while keeping the accuracy at the highest level.

Please see the [ipython notebook](https://github.com/seedlingfl/Review-Rating-Prediction/RatingPrediction_YuheZhang.ipynb) for details.
