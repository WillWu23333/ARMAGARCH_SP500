# Risk Forecasting Using ARMA-GARCH Models: Value at Risk for the S&P 500 Index

This project focuses on forecasting the volatility and risk metrics of the S&P 500 index using ARMA-GARCH models. Using data from 2000 to 2024, the analysis captures time-varying volatility and accounts for linear dependencies to assess **Value at Risk (VaR)** and **Expected Shortfall (ES)**.

## Key Features & Analysis
- **Volatility Clustering:** Identification of persistent "calm" and "storm" periods in market returns.
- **Leptokurtosis Analysis:** Analysis of "heavy tails" in return distributions, indicating a higher probability of extreme outcomes.
- **Risk Metrics:** Forecasting 1% VaR and Expected Shortfall for a hypothetical $10,000 position.
- **Model Selection:** Sequential modeling using Information Criteria (AIC/BIC) to select the most parsimonious ARMA and GARCH orders.

| | |
|:---:|:---:|
| <img width="480" height="320" alt="S&P 500 Daily Close" src="https://github.com/user-attachments/assets/049244a9-0b79-4190-8f31-a8841e4be524" /> | <img width="480" height="320" alt="Returns Squared" src="https://github.com/user-attachments/assets/2814ee7b-9438-488a-ab52-eeb66a598d95" /> |



## Methodology
The analysis follows a rigorous statistical procedure:
1. **Data Cleaning:** Transforming S&P 500 daily close prices into logarithmic returns (percentage).
2. **Exploratory Data Analysis (EDA):** Visualizing volatility clustering through squared returns and ACF/PACF plots.
3. **Mean Modeling:** Using an **ARMA(2,1)** model to capture linear dependencies in the mean.
4. **Variance Modeling:** Implementing a **GARCH(1,1)** model to handle heteroskedasticity and time-varying volatility.
5. **Validation:** Conducting Engle’s ARCH, Ljung-Box, and Nyblom Stability tests to ensure model adequacy.
6. 
<img width="933" height="715" alt="image" src="https://github.com/user-attachments/assets/075f4f74-06df-455a-8074-95f1cb6b03b5" />

## Dependencies
The following R packages are required for this analysis:
- `quantmod`: Financial data acquisition (Yahoo Finance).
- `rugarch`: GARCH model specification, fitting, and forecasting.
- `forecast`: ARMA/ARIMA model selection.
- `tidyverse` & `ggplot2`: Data manipulation and visualization.
- `xts` & `timetk`: Time series handling and future series generation.
- `MASS`: Distribution fitting.

## Data Source
Market data is retrieved from [Yahoo Finance](https://finance.yahoo.com/quote/%5EGSPC/) for the S&P 500 Index (`^GSPC`).
