# Retail Sales Forecasting using ARIMA and SARIMAX

This project focuses on forecasting monthly retail sales using two classical time series models: ARIMA and SARIMAX. The goal is to predict future sales to help businesses plan inventory and handle seasonality effectively.

## Project Objective

To build a sales forecasting model that can predict future monthly sales using past data trends and seasonality patterns.

## Dataset

- Source: [Shampoo Sales Dataset by Jason Brownlee](https://raw.githubusercontent.com/jbrownlee/Datasets/master/shampoo.csv)
- Format: CSV
- Columns:
  - Month (string, format: '01-01')
  - Sales (float)
- Duration: Jan 1901 to Dec 1903

## Steps Followed

1. **Data Loading and Cleaning**  
   - Converted month column to datetime format
   - Handled missing/null values

2. **Visualization**  
   - Plotted original sales time series to observe trends

3. **Stationarity Check**  
   - Performed ADF (Augmented Dickey-Fuller) Test
   - Differenced the data to remove trends

4. **ACF and PACF Analysis**  
   - Used ACF and PACF plots to estimate p and q values for ARIMA

5. **Model Building**  
   - Built ARIMA(p,d,q) model using statsmodels
   - Evaluated model summary and residuals

6. **SARIMAX Model**  
   - Extended the ARIMA model with seasonal terms to capture repeating patterns

7. **Forecasting Future Sales**  
   - Forecasted the next 6 months of sales using both models
   - Visualized the forecast results

8. **Model Evaluation**  
   - Compared actual vs predicted values
   - Evaluated using MAE and RMSE metrics

## Results

- ARIMA and SARIMAX models were successfully used for forecasting
- SARIMAX handled seasonal variation better in the sales data
- Forecasts showed reasonable accuracy for short-term prediction

## Libraries Used

- pandas
- numpy
- matplotlib
- statsmodels
- scikit-learn

## How to Run

1. Clone the repository or download the code
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib statsmodels scikit-learn
