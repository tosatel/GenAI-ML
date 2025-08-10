# InvDD_Forcasting
# Sales Forecasting Project (InvDD_Forecasting)

This project implements a machine learning pipeline for sales forecasting using various regression models.

## Project Structure

1. **Data Preparation**:
   - Loads sales data with date, store, item, and sales columns
   - Performs comprehensive feature engineering
   - Handles temporal features and holidays

2. **Exploratory Data Analysis**:
   - Visualizes sales patterns
   - Identifies correlations between features
   - Examines distribution of sales

3. **Modeling**:
   - Implements multiple regression approaches
   - Evaluates model performance using MAE

## Requirements

- Python 3.x
- Libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn
  - xgboost
  - holidays (for holiday detection)

## Usage

1. Place your sales data in CSV format with columns: date, store, item, sales
2. Update the file path in the code: `pd.read_csv('/content/drive/MyDrive/Dataset/IDF.csv')`
3. Run the entire notebook/script

## Model Performance

The models are evaluated using Mean Absolute Error (MAE):

| Model            | Training MAE | Validation MAE |
|------------------|--------------|----------------|
| LinearRegression | 20.90        | 20.97          |
| XGBRegressor     | 6.92         | 6.93           |
| Lasso            | 21.02        | 21.07          |
| Ridge            | 20.90        | 20.97          |

## Key Findings

- XGBoost outperforms linear models significantly
- Temporal features (weekdays, holidays, monthly cycles) are important predictors
- Sales data shows clear patterns based on time and store/item characteristics

## Future Improvements

- Add more sophisticated feature engineering
- Implement time-series specific models (ARIMA, Prophet)
- Add hyperparameter tuning
- Implement cross-validation
