# Project 1 [Fed Funds Interest Rates]
This code performs modeling and analysis on the Effective Federal Funds Rate, a key interest rate used in financial markets. The goal is to understand the factors influencing the rate and build accurate prediction models. Let's walk through the code step by step:

- Data preprocessing: The code begins by removing unnecessary columns such as Year, Month, and Day from the dataset. These columns may not directly contribute to the prediction of the Effective Federal Funds Rate.

- Feature scaling: To ensure that all input features are on a similar scale and prevent any particular feature from dominating the model training process, the data is scaled using the StandardScaler from the scikit-learn library. Scaling the data helps in achieving better model performance.

- Train-test split: The scaled data is split into train, test, and validation sets using the train_test_split function from the scikit-learn library. This division allows for evaluating the model's performance on unseen data and helps in assessing its generalization capabilities.

- Feature importance analysis: The code employs the Random Forest Regressor, a popular ensemble learning algorithm, to determine the most important factors impacting the Effective Federal Funds Rate. The feature_importances_ attribute of the Random Forest model provides a measure of the relative importance of each feature. The code calculates the feature importances and displays them in descending order, indicating the variables that have the most significant influence on the Effective Federal Funds Rate.

- Regression analysis: The code uses the Ordinary Least Squares (OLS) method from the statsmodels library to perform a regression analysis. It focuses on four key variables: Inflation Rate, Federal Funds Target Rate, Unemployment Rate, and Real GDP (Percent Change). These variables are included in the model as predictors, while the Effective Federal Funds Rate serves as the target variable. The regression analysis provides insights into the relationships between the predictors and the target variable, including coefficient values, statistical significance, and other statistics.

- Model evaluation: To assess the performance of different regression models, the code trains and evaluates several popular algorithms using the train, test, and validation sets. The models considered are Support Vector Regressor (SVR), Decision Tree Regressor, K-Nearest Neighbors Regressor, Random Forest Regressor, Multi-Layer Perceptron Regressor, AdaBoost Regressor, and Gradient Boosting Regressor. The evaluation metric used is the R-squared score, which measures the proportion of the target variable's variance explained by the model. Higher R-squared scores indicate better model performance.

- Model tuning: The Decision Tree Regressor, Random Forest Regressor, Gradient Boosting Regressor, and Multi-Layer Perceptron Regressor models are tuned using grid search and cross-validation. This process involves systematically testing different combinations of hyperparameters and selecting the ones that yield the best performance. The best hyperparameters for each model are displayed, along with their corresponding R-squared scores.

- Best model selection: The code selects the models with the highest R-squared scores on the validation set as the best models for predicting the Effective Federal Funds Rate. These models demonstrate the strongest performance and are deemed most suitable for accurate predictions.

# Project 2 [renewable energy Project]
### Problem Statement
I am an in-house data scientist for a renewable energy firm focussing on wind and solar power. I have been tasked with analyzing the latest field data with various measurements for their wind turbines. In addition to the analysis, i must build a model that predicts the power, in kW/h, the turbines generate.
### Objectives
The following objectives need were met:
• Performed appropriate data cleaning and preparation to ensure good model performance.
• Built a machine learning model that predicts the power generated.
• Evaluated and tuned the model.
