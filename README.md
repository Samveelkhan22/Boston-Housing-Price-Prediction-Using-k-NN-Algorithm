# Boston Housing Price Prediction Using k-NN Algorithm

This project predicts the median value of houses (MEDV) in Boston census tracts using the k-Nearest Neighbors (k-NN) algorithm. The dataset used in this project comes from the BostonHousing.csv file, which contains information on various factors influencing housing prices in Boston.

## Project Overview

The goal of this project is to build a k-NN model to predict the continuous variable `MEDV`, which represents the median value of houses in a census tract. We perform several analyses, including evaluating the impact of different values of `k`, making predictions for new data, and discussing the limitations of the k-NN approach.

### Key Tasks:
1. **Data Preprocessing**: Normalize and partition the data into training (60%) and validation (40%) sets.
2. **Modeling**: Train a k-NN regression model with k values from 1 to 5, using the first 12 predictors.
3. **Prediction**: Predict the MEDV for a new housing tract and determine the best k based on validation data.
4. **Error Analysis**: Calculate the training set error and explain why the validation error might be overly optimistic.
5. **Efficiency Considerations**: Discuss the limitations of using k-NN when predicting housing prices for thousands of new tracts.

## Dataset

- **BostonHousing.csv**: Contains 506 observations of 13 variables.
- **Variables**:
  - `CRIM`, `ZN`, `INDUS`, `CHAS`, `NOX`, `RM`, `AGE`, `DIS`, `RAD`, `TAX`, `PTRATIO`, `LSTAT`
  - Target variable: `MEDV` (Median value of owner-occupied homes in $1000s)
  
  **Note**: The column `CAT.MEDV` (categorical version of MEDV) is ignored for the purpose of this task.

## Model Evaluation

- We used the Mean Squared Error (MSE) to evaluate model performance.
- After testing k values from 1 to 5, we found that **k=2** provides the best result with a MSE of 9.25 on the validation set.
- We used this value of k to make predictions for a new housing tract.

## Key Results

- **Best k**: 2
- **Mean Squared Error for k=2**: 9.25

### Predictions for a New Housing Tract

For a tract with the following information:

CRIM: 0.2, ZN: 0, INDUS: 7, CHAS: 0, NOX: 0.538, RM: 6, AGE: 62, DIS: 4.7, RAD: 4, TAX: 307, PTRATIO: 21, LSTAT: 10

The predicted median value (MEDV) is approximately **$28,200**.

## Limitations of k-NN for Large-Scale Predictions

k-NN can be computationally expensive for large datasets as it computes the distance between each new observation and every point in the training set. This makes it inefficient for predicting the prices of thousands of new tracts. Alternative methods like Decision Trees or Random Forests could be considered for more efficient predictions.

## Libraries Used

- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`

## Author

- **Samveel Zaheer Khan** - Data Science Enthusiast

