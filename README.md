# Cleaned_Gold_Data

Preprocessing / Cleaning

- Added an `id` column to uniquely identify each row.
- Checked for missing values: filled gaps where possible; removed rows with insufficient data.
- Fixed formatting inconsistencies in columns.





Description

This dataset contains daily gold futures market data for the last five years, sourced from Yahoo Finance using the ticker GC=F.

It is designed specifically for time-series forecasting tasks, where the objective is to model and predict future gold prices using historical trends and technical indicators.

The dataset includes traditional OHLCV market data (Open, High, Low, Close, Volume) along with commonly used technical analysis indicators such as moving averages, volatility measures, RSI, MACD, and Bollinger Bands.

This makes it suitable for: • Financial time-series forecasting • Deep learning models (LSTM, GRU) • Statistical models (ARIMA, SARIMA) • Prophet forecasting • Feature engineering and EDA ⸻


Date Range: From 2021-06-11 too 2026-01-30


File Format

Format: CSV
Rows: 1167
Frequency: Daily
Missing values: 0 (no NULL/NaN values detected)


📊 Columns Description

date – Trading date.

open – Opening price of gold futures for the day.

high – Highest price reached during the trading session.

low – Lowest price reached during the trading session.

close – Closing price of gold futures for the day.

volume – Trading volume for gold futures contracts.

ma_7 – 7-day moving average of closing price.

ma_30 – 30-day moving average of closing price.

ma_90 – 90-day moving average of closing price.

daily_return – Percentage change in closing price from the previous day.

volatility_7 – 7-day rolling standard deviation of daily returns.

volatility_30 – 30-day rolling standard deviation of daily returns.

rsi – Relative Strength Index, a momentum indicator measuring overbought/oversold conditions.

macd – Moving Average Convergence Divergence value.

macd_signal – Signal line for MACD.

bb_upper – Upper Bollinger Band.

bb_lower – Lower Bollinger Band.

id – Identifies Individual Rows.


Render data in terminal

```python
import pandas as pd
df = pd.read_csv("gold_price_forecasting_dataset_2026.csv")
df.head()
