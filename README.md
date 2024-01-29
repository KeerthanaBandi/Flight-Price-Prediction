# Flight Price Prediction

# Abstract: 
Air travel has evolved into a popular, necessary, and quick mode of transportation owing to the ever-increasing connectivity of air routes around the globe. For airlines, predicting prices is a crucial yet difficult task because prices are always fluctuating and are known to depend on a wide range of factors. In this project, we employ a machine learning regression approach to forecast flight fares by using simple information such as the airline name, source, destination, number of stops, and departure and arrival times.

# Dataset:
The Flight Price Prediction dataset have been extracted from Kaggle. The dataset contains 3,00,153 records about flight details between the 6 top metro cities in India which were taken from the website Easemytrip. Our dataset contains 12 attributes among which 8 are categorical and 4 are numerical.
Among the 12 attributes, price is our target attribute.

# Regression:
The performance metric used are R Squared Score (R2 Score) and Root Mean Square Error (RMSE) to evaluate the performance of the regression models. R2 Score indicates what percentage of the variability in the dependent variables (price) can be explained by the model.

# Regression Models:
We have chosen 3 Regression models, to predict the price of the Flight. They are,
1. Linear Regression
2. Bagging Regression and 
3. Random Forest Regression 

# HyperParameter Tuning:
We have performed HyperParameter Tuning using GridSearchCV, and found the best parameters which will improve the R2 score value and decrease the root mean square of the basemodels. These parameters are max features and n estimators, which provide the maximum number of features to be taken into account when dividing the node and the number of trees in the forest. The bootstrap hyperparameter, determines whether the data points are sampled with or without replacement, is also tuned along with max features and n estimators. 
1. n_estimators = [75,100,125,150]
2. max_features = [2,4,6,8,10]
3. Bootstrap = True/ False

On Perfoming gridsearch, the value of R2 score is slightly improved and the value of RMSE is decreased when compared with the base models.

# Conclusion:
In comparison to the hyperparameter tuned Random Forest Regressors, the baseline model is the least effective because it only accounts for 98.66% (R2 Score) of the variation in flight price. 
Hence, we can infer that out of all the models, Random Forest Regressor gives a high R2 score with 125 estimators and 10 features (Hyperparameter tuning). However, if we consider the fitting time of the models, the Bagging regressor with 13.36 seconds is far better than the Random Forest model with 133.79 seconds. Also, there is only a difference of 0.003956 in the R2 scores of both the regressors and the RMSE is slightly higher for Bagging Regressor. If we want a model that fits fast and makes predictions similar to the best model, we can choose Bagging or else tuned Random Forest model is preferred.

