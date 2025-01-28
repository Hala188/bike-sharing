# Bike Sharing Demand Prediction using Linear Regression

This repository contains a Python project that predicts bike sharing demand using linear regression.  The project utilizes the Capital Bikeshare dataset, combining historical usage patterns with weather data to forecast bike rental demand in Washington, D.C.



## Project Overview

Bike-sharing systems provide a convenient and sustainable mode of transportation.  Accurate prediction of bike rental demand is crucial for optimizing resource allocation and ensuring efficient operation of these systems. This project demonstrates the application of linear regression to forecast bike rental demand based on historical data and weather conditions.

## Dataset

The dataset used in this project is the Capital Bikeshare dataset, available in the file. It contains hourly data on bike rentals, including information about the date and time, season, weather conditions, temperature, humidity, windspeed, and the number of casual and registered user rentals.

## Methodology

The project follows a typical machine learning workflow:

1. **Data Loading and Preprocessing:** The data is loaded using pandas, and the 'datetime' column is converted to datetime objects. Categorical features (season, weather) are initially converted to strings for EDA and then one-hot encoded for model training.
2. **Exploratory Data Analysis (EDA):**  EDA is performed to understand the relationships between the features and the target variable ('count').  Histograms, box plots, scatter plots, and correlation heatmaps are used for visualization.
3. **Feature Engineering:** New features, such as 'hour', 'hour_sin', 'hour_cos', 'windspeed_squared', and 'Temp_atemp' (temperature difference) are created to potentially improve model performance.
4. **Feature Selection:** Lasso regression is employed to select the most relevant features for the model.  This helps to reduce dimensionality and improve model interpretability.
5. **Model Training:** A linear regression model is trained on the training data.
6. **Model Evaluation:** The model's performance is evaluated using metrics such as Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared (R²) score.
7. **Residual Analysis:** Residual plots are used to check the assumptions of linear regression.

## Requirements

The project requires the following Python libraries:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

You can install these libraries using pip:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
