# Regression-Projects
Prediction of Sub Surface Temperature using five different Linear Regression Model
**This Project is to predict temperature in the subsurface for geothermal energy applications. The bottomhole temperature at the bottom of an existing wellbore drilled for oil and gas application can be used to map the subsurface temperatures, which can then be used for creating geothermal heat maps**

**Model Training and Evaluation:**

The "AASG_Geothermal.xlsx" dataset is used to train regression models for predicting the Bottom-hole temperature (BHT).
The regressors are trained using the following four features: the measured depth of the bottomhole, surface temperature at the wellbore location, and the latitude and longitude of the wellbore.
Data preprocessing is implemented, including the following steps:
a. Outliers are detected using Isolation Forest.
b. Scaling is applied using a standard scaler.
c. It is ensured that all preprocessing is learned from the training data, and the same preprocessor is applied to both training and testing data.
The hyperparameters of the regression models are tuned.
The best-performing regression model for each of the five regression techniques is identified based on their generalization performance in terms of Mean Absolute Error (MAE).
The five models are ranked based on their MAE performance.

**Performance Evaluation:**

The RMSE, R-squared (R2), MAE, and MAPE for each of the five best-performing models are presented in four subplots. The models are arranged according to their assigned ranks in terms of MAE, with the highest rank model on the left and the lowest rank model on the right along the x-axis.

**Model Download**

The five best-performing models along with the preprocessors used for predicting BHT are saved.
**Deployment Preparation:**

The saved preprocessors and the five best-performing regression models are deployed on the deployment data provided in "Deploy.xlsx" to predict BHT. 
The predictions are displayed as the mean of the predictions generated by the five models, with the uncertainty in prediction represented as the range of prediction (max-min).
"Deploy_Results.xlsx" is created to record the four features and their corresponding mean BHT predictions, along with the range of BHT predictions.
