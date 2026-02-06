## Flight Delay Prediction Using Machine Learning

### Project Overview

This project analyzes historical flight data to identify key factors contributing to flight delays and builds multiple classification models to predict whether a flight will be on-time or delayed. The workflow includes data cleaning, exploratory analysis, feature engineering, model training, evaluation, and prediction on new test data.

### Dataset


Each row represents a flight with attributes related to scheduling, routing, carrier, and weather.

### Target Variable

FLIGHT_STATUS: ontime or delayed

### Key Predictors Used

Scheduled departure time (CRS_DEP_TIME)

Airline carrier (CARRIER)

Origin airport (ORIGIN)

Destination airport (DEST)

Weather condition (WEATHER)

Day of the week (DAY_WEEK)

### Data Preprocessing

Removed identifier-only fields (TAIL_NUM, FL_NUM)

Dropped redundant or low-impact features (FL_DATE, DAY_OF_MONTH, DISTANCE)

Removed highly correlated variables (DEP_TIME)

Converted categorical features using one-hot encoding

Binned departure times into hourly categories

Split data into training (60%) and validation (40%) sets

### Exploratory Data Analysis

Used pivot tables and aggregations to explore:

Flight delays by day of the week

Delay proportions by airline carrier

Impact of weather at origins and destinations

Routes with the highest number of delays

These insights helped guide feature selection and model choice.

### Models Implemented

Three classification models were trained and compared:

1. Naive Bayes (MultinomialNB)

Simple probabilistic baseline model

Good performance with categorical data

2. Decision Tree (CART)

Captures non-linear relationships

High training accuracy but signs of overfitting

3. Logistic Regression

Strong generalization on validation data

Selected as the final model for predictions

### Model Evaluation

Used confusion matrices and accuracy

Generated Gains and Lift charts to evaluate ranking performance

Logistic Regression achieved the best validation accuracy (~83%)

### Test Prediction

A separate test dataset was created with new flight scenarios:

Data was preprocessed to match training features

The trained Logistic Regression model predicted flight status

Results were exported to FlightDelaysTestingData.csv

### Technologies Used

Python

Pandas, NumPy

Scikit-learn

dmba

Matplotlib

### Key Takeaways

Demonstrates end-to-end data analysis and ML workflow

Strong use of feature selection, model comparison, and evaluation

Practical application of predictive analytics in real-world aviation data
