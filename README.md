# Project-2
# Title that recommends an action
## Subtitle describing the analysis 

**Author**: 

### Business problem:

Choosing the best fit Machine Learning model that will predict the price per night of the rental based on the rental's features.

### Model Approach
In this Project, I used 3 regression models to find the best fit model for prediction.

Linear (Standard)
Random Tree
KNN
Metrics for evaluating the Model:

MAE: Mean absolute error measures the average of the absolute values of all of the errors our model makes.

MSE: Mean squared error is similar to mean absolute error, but it penalizes large errors more.

RMSE: Root mean squared error is the square root of the mean squared error. Like the previous two metrics, a lower RMSE is better.

R^2: This score can be interpreted as saying that our model can account for about XX% of the variation in y_test using the features in X_test. (Not really a high priority measurement in this use case)

### Data:
The dataset has the following columns:
 1   id              2222 non-null   int64  
 2   latitude        2222 non-null   float64
 3   longitude       2222 non-null   float64
 4   property_type   2222 non-null   object 
 5   room_type       2222 non-null   object 
 6   bathrooms       2211 non-null   float64
 7   bedrooms        2221 non-null   float64
 8   minimum_nights  2222 non-null   int64  
 9   price           2222 non-null   object 

#### Visuals


## Recommendations:

Based on the model scores, I've decided to choose KNeighbors as my chosen regressor model. Across the three models, KNeighbors model yielded the lowest MAE score as well as the lowest RMSE score. The reason I prioritized MAE and RMSE is because this is a price prediction and the lower the difference between prediction than the actual target the better. In the case of KNeighbors model, the score was less than 100. I've also tested the model with reduced feature to see if the score had improved. However, since there weren't a lot of features to in the dataset to begin with, it appears that reducing the number of features made the model less effective.

Chosen Model Hyperparameter: n_neighbors = 23, p = 1, weights = 'uniform'

###Model Results:

![Screen Shot 2022-07-27 at 11 17 39 PM](https://user-images.githubusercontent.com/76888532/181413006-32665dcf-3490-41c4-ada2-8d70882fe7a5.png)
![Screen Shot 2022-07-27 at 11 16 27 PM](https://user-images.githubusercontent.com/76888532/181412918-ede7a470-33eb-4cc9-b84b-52e93d5fd9c9.png)
![Screen Shot 2022-07-27 at 11 17 52 PM](https://user-images.githubusercontent.com/76888532/181413036-b1d76119-38ed-4a7d-8d86-5b2f7af65288.png)
