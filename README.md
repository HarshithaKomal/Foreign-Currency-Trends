# Forecasting Currency Trends: Analyzing Euro to USD Exchange Rates

# Introduction

This project aims to explore and forecast the exchange rates between the Euro and the US Dollar
using advanced time series methodologies. The exchange rate between these two major currencies
is influenced by a multitude of factors including economic indicators, geopolitical events, and
market sentiment. By analyzing historical trends and patterns, this study seeks to develop
predictive models capable of offering valuable insights into future currency fluctuations. The
results of this analysis have significant implications for stakeholders in financial markets, such as
traders, investors, and policymakers, who rely on accurate forecasts for informed decision-making.

# Data Description
The project utilizes two key datasets that provide a comprehensive view of the Euro to USD

exchange rate dynamics:
The first dataset, BOE-XUDLERD.csv, was sourced from the Bank of England database. This
dataset contains daily exchange rate data, capturing short-term variations and providing granular
insights. It comprises two columns: Date, representing the observation date, and Value, indicating
the daily exchange rate.

The second dataset, Foreign Exchange Rate with Prediction (Euro To USD).csv, complements
the daily data with a focus on weekly exchange rate trends and model predictions. It includes four
columns: Date, which indicates weekly intervals; Foreign Exchange Rate (weekly), representing
the observed rates; Weekly First Difference, capturing week-over-week changes in the exchange
rate; and Predicted Exchange Rate, which contains values forecasted by the ARIMA model.
Together, these datasets form the foundation for the exploratory and predictive analyses performed
in this study.

# Methodology

The methodology for this project involves several structured steps, each designed to ensure robust
analysis and reliable forecasting. The process begins with data preprocessing, where the datasets
are cleaned and prepared for analysis. Missing or inconsistent values are handled appropriately,
and the Date column is converted into a datetime format to facilitate time series operations. Initial
visualizations are created to identify overarching trends, seasonal patterns, and potential outliers
that could impact the analysis.

The exploratory data analysis (EDA) phase focuses on uncovering underlying patterns within the
data. Statistical summaries are generated, and the time series is plotted to reveal trends and periodic
fluctuations. Autocorrelation functions (ACF) and partial autocorrelation functions (PACF) are
analyzed to identify dependencies between current and lagged values, which is critical for model
development.

For modeling, the time series is decomposed into its trend, seasonality, and residual components
using the seasonal_decompose function. Stationarity, a prerequisite for effective time series
modeling, is assessed using the Augmented Dickey-Fuller (ADF) test. To build a predictive model,
an ARIMA framework is employed, capturing the autoregressive, moving average, and integrated
components of the time series. Hyperparameter tuning is automated using the
pmdarima.auto_arima function to optimize model performance.

Evaluation metrics are applied to assess the model’s accuracy and reliability. Key metrics include
the R² score, which measures the proportion of variance explained by the model; the Mean
Absolute Error (MAE) and Root Mean Squared Error (RMSE), which quantify the magnitude of
prediction errors; and the Mean Absolute Percentage Error (MAPE), which evaluates the
percentage deviation of predictions from actual values. Finally, the model is used to forecast future
exchange rates, and the results are compared against actual observations to validate its predictive
capability.

# Results

The exploratory analysis revealed distinct patterns in the Euro to USD exchange rate, reflecting
the influence of economic and geopolitical events over time. The time series exhibited significant
autocorrelation, as evidenced by the ACF and PACF plots, indicating that past values strongly
influence future trends. The decomposition analysis further highlighted the presence of
consistent seasonal components and a discernible long-term trend.

The ARIMA model demonstrated robust performance in forecasting exchange rates. Evaluation
metrics provided compelling evidence of the model’s accuracy, with an R² score of 0.91
indicating that the model explained 91% of the variance in the data. The Mean Absolute Error
(MAE) was calculated to be 0.0023, and the Root Mean Squared Error (RMSE) stood at 0.0035,
both of which confirm the model’s precision. Additionally, the Mean Absolute Percentage Error
(MAPE) of 0.31% underscored the minimal deviation of the predicted values from the actual
observations.

Visual comparisons between predicted and actual exchange rates validated the model’s
effectiveness, particularly for short-term forecasts. The predictions closely aligned with observed
trends, demonstrating the model’s ability to capture the nuanced dynamics of currency exchange.

# Conclusion

The analysis successfully leveraged time series methodologies to understand and forecast the Euro
to USD exchange rates. The ARIMA model proved to be an effective tool, delivering accurate
predictions and uncovering meaningful patterns within the data. These insights highlight the utility
of statistical modeling for financial forecasting, providing a valuable resource for stakeholders
aiming to navigate the complexities of currency markets.

# Future Scope

The project opens several avenues for further exploration. Integrating exogenous variables, such
as interest rates, inflation, and economic indicators, could enhance the predictive accuracy of the
model. Advanced machine learning techniques, including Long Short-Term Memory (LSTM)
networks, offer the potential to improve long-term forecasting capabilities. Additionally,
extending the analysis to multi-currency exchange rates could provide broader insights, benefiting
financial institutions and global investors alike.
