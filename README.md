### PREDICTING FLIGHT DELAYS THROUGH MACHINE LEARNING


#### PROJECT DESCRIPTION:

This project aims to explore various supervised machine learning models which can be reliably used to predict target variables. The dataset that has been used is obtained from a non-public database and contains flight data from 376 United States airports and comprises of different statistics related to flight timings, operational delays, fuel consumption and passengers of domestic flights. The data pertains to calendar year 2018 and 2019 and the end-goal is to create a model which can predict the flight delays one week in advance. Since the target, Arrival Delay, is a continuous variable, regression models will be used to achieve the goal.

#### WORKFLOW:

1. [Exploratory Analysis](#l1) - The whole database was used to do the exploration. SQL queries were made directly through jupyter notebook and pandas and other libraries f python were used to explore the dataset.
2. [Data Sampling & Wrangling](#l2) - Since the primary dataset was very large, 10% of the dataset was used as a sample and sampling was not random. Data from       January 1-31, 2018 and December 21, 2018 to January 31, 2019 was taken as a sample to do the modeling.
3. [Feature Engineering & Dimensionality Reduction] (#l3) -  To add strengh to the primary dataset some additional features like averages of delays, payloads, passengers and seats data were added to it. The features were increased from 16 to 24. On the other hand, feautures with low variance and high correlation were removed from the model and the features reduced to 20 again. Principal Component Analysis was also tried to see if conversion to principal components increases the predictability. However, it didn't gave the desired outcome.
4. [Testing Regression Models](#l4) - Various basic regression models like linear regresssion, ridge regression were used and scored against advanced ensemble models like Random Forest and XG Boost.
5. [Model Selection & Hyperparameter Tuning](#l5) - A comparative study of the R2 scores and Mean Absolute Error of all the models tried was done and the model with the highest R2 score and lowest Mean Absolute Error was chosen. XGB Regressor turned out to be the winner, though with only about .105 R2 score. Then various hyperparameters were fed to the GridSearch to determine the best model.
6. [Predicting Flight Delays](#l6) - The fine-tuned model developed above was used on a different dataset and results saved and submitted for evaluation.
