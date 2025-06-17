# Predicting Used Car Prices using Linear Regression

This project applies **Linear Regression** to predict used car prices based on various car attributes. The analysis includes data preprocessing, feature engineering, exploratory data analysis, and model evaluation using both statistical and machine learning approaches.

## Files

- `Predicting Used Car Prices - Linear Regression.ipynb`: Main notebook containing the entire workflow.
- `Used car prices.csv`: Dataset containing specifications and prices of used cars.

## Dataset Overview

The dataset contains **4345 entries** and **9 columns**, including:

| Column         | Description                                |
|----------------|--------------------------------------------|
| Brand          | Car manufacturer (e.g., BMW, Audi)         |
| Price          | Price of the used car (target variable)    |
| Body           | Type of the car body (e.g., sedan, van)    |
| Mileage        | Mileage used (in thousands of kilometers)  |
| EngineV        | Engine volume                              |
| Engine Type    | Fuel type (Petrol, Diesel, etc.)           |
| Registration   | Whether the car is registered or not       |
| Year           | Year of manufacture                        |
| Model          | Specific model of the car                  |

> Note: The dataset contains **missing values** in the `Price` and `EngineV` columns, which are handled during preprocessing.

## Technologies Used

- Python (NumPy, Pandas, Seaborn, Matplotlib)
- scikit-learn
- statsmodels

## Data Preprocessing

Steps include:
- Handling missing values
- Removing outliers (e.g., cars with unrealistic prices)
- Encoding categorical variables
- Feature scaling (where necessary)

## Exploratory Data Analysis

Visual analysis was done to understand:
- Price distribution across brands
- Correlation between mileage and price
- Trends based on year of manufacture

## Model Building

Two types of linear regression models were used:
- **OLS Regression** using `statsmodels`
- **LinearRegression** using `scikit-learn`

Performance was evaluated using **R² score**, residual analysis, and predictions on test data.

## Results

- Achieved an **R² score of ~0.75**, indicating the model performed well in predicting the target on average.
- The difference between the target and predicted values got dramatically higher during the last few observations which could be due to missing factors that could be contributing to the target value like 'Prior Damage' of the car which isn't provided or 'Model' which was dropped during the preprocessing.<br><br>
How to improve the model?
1. Use a different set of predictor variables.
2. Remove a bigger part of the outliers.
3. Use different kinds of transformations.
   
## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Predicting-used-car-prices.git
   cd Predicting-used-car-prices
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
3. Launch the Jupyter Notebook:
   ```bash
   jupyter notebook

## Future Improvements
Try polynomial regression for non-linear relationships.

Use regularization (Ridge, Lasso) to improve model generalization.

Incorporate more robust imputation techniques for missing data.
