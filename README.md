# Car Price Prediction

This repository contains a machine learning project aimed at predicting the selling prices of used cars. The project leverages various data preprocessing techniques and machine learning algorithms to provide accurate price predictions based on multiple features of the cars. The following sections provide an overview of the project structure, data exploration, preprocessing steps, model building, and evaluation.

## Project Overview

The goal of this project is to develop a predictive model that estimates the selling price of a car based on its features such as year of manufacture, kilometers driven, fuel type, seller type, transmission type, number of previous owners, and car brand. This project uses a dataset from Car Dekho, which contains detailed information about various cars.

## Dependencies

The following Python libraries are required to run the code:

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn

You can install the required libraries using pip:

```sh
pip install numpy pandas matplotlib seaborn scikit-learn
```

## Data Exploration

The dataset is loaded and basic exploratory data analysis (EDA) is performed to understand its structure and contents. The EDA includes:
- Checking the shape of the dataset.
- Displaying column names and basic dataset info.
- Descriptive statistics.
- Checking for null values.

## Data Visualization

A histogram is plotted to visualize the distribution of car prices.

## Feature Engineering

A new feature, `brand`, is extracted from the `name` column. Categorical features such as `fuel`, `seller_type`, `transmission`, `owner`, and `brand` are identified for further processing.

## Data Preprocessing

Data preprocessing steps include:
- Handling missing values using `SimpleImputer`.
- Standardizing numerical features using `StandardScaler`.
- One-hot encoding categorical features using `OneHotEncoder`.
- Converting categorical values to numerical using `LabelEncoder`.
- Detecting and handling outliers in numerical features.

## Model Building

Two machine learning models are implemented:
- Random Forest Regressor
- Gradient Boosting Regressor

Each model is evaluated using cross-validation and trained on the preprocessed data. Model performance is measured using Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R^2 score.

## Model Evaluation

The best-performing model (Random Forest) is used to predict car prices on the test set. A scatter plot is generated to compare the actual prices with the predicted prices.

## Predicting Car Prices for User Inputs

A function `predict_car_price` is defined to allow users to input car features and get a predicted price using the trained model.

## Example Usage

An example usage of the `predict_car_price` function is provided, demonstrating how to predict the price for a specific car based on user-defined inputs.

## How to Run

To run the code, execute the following steps:
1. Ensure all dependencies are installed.
2. Load the dataset (`CAR DETAILS FROM CAR DEKHO.csv`) into the same directory as the script.
3. Run the script to train the models and make predictions.
