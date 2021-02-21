# INVESTMENT DASHBOARD

## Applying machine learning into the stock market

### Team Members: Syed Naqvi, Minh Tran, Rodrigo Guazzelli, Hsuan Liu, Abdullah Mamun

*The project is for study propose only*

[Project Presentation](https://github.com/Minhtran18/Project_2/tree/master/Presentation)

### Summary

1.	Overview
2.	Data Sources
3.	Python Library
4.	Approach
5.	Dashboard Visualization
6.	Understanding the Theory
7.	Room for Improvement
8.	Q&A Session

---


### 1. Overview
The purpose of the dashboard is to present a detailed visualization of company insight with historical performance, technical indicators and predict the upcoming volatility applying machine learning. 
    
Target clients: Experienced investors.

### 2. Data Source

Yahoo Finance

### 3. Python Library

Existing Libraries: Matplotlib, Pandas, Numpy, Plotly, Sklearn, Stats model.

New Libraries: Dash, Tkinter, Quantstats.

### 4. Approach

* Imported various libraries for visualization of stock performances.

* Imported Ticker and created a selection window for all the tickers available at Yfinance.

* Identified the trend and visualized the historical prices for the selected tickers (for coding refer Jupyter Notebook).

* Applied   multiple models to predict future Price and volatility.

### 5. Dashboard Visualization

![Dashboard](/Images/DemoDashboard-AAPL.mp4)
![Dashboard_pic](/Images/dashboard_picture.jpg)

### 6. Understanding the Theory

Based on those models we prepared a dashboard consisting of 4 tabs:
    
### 6.1. Stock Overview

Composed by: 

* Last closing price;

* Industry;

* Sector;

* Business Summary.

* You can also select your desired period of Stock Performance:
1mo, 3mo, 6mo, 1y, 2y, 5y, 10y, ytd, max.

### 6.2. Return and Volatility matrix

### 6.2.1. Cumulative Return

A cumulative return is the aggregate daily return that the stock has gained or lost over time. The cumulative return is expressed as a percentage based on the stock closing price.

### 6.2.2. Sharpe Ratio

Sharpe ratio is a well-known and well-reputed measure of risk-adjusted return on an investment or portfolio. It can be used to evaluate the performance of an individual stock. 

The Sharpe ratio indicates how well an equity investment performs in comparison to the rate of the S&P 500 index and NASDAQ.

### 6.2.3. Rolling Standard Deviation

Standard deviation is the statistical measure of market volatility, measuring how widely prices are dispersed from the average price. If prices trade in a narrow trading range, the standard deviation will return a low value that indicates low volatility. A volatile stock has a high standard deviation, while the deviation of a stable blue-chip stock is usually rather low. 

Rolling Standard Deviation is a metric calculated over the range of a shifting (rolling) window. The Annualized Standard Deviation is the standard deviation multiplied by the square root of the number of periods in one year (252 trading days).


### 6.2.4. Rolling EWM

A weighted average is an average that has multiplying factors to give different weights to data at different positions in the sample window.

### 6.3. Algo Trading Strategy 

### 6.3.1. Algo Trading

It is usually applied for short term strategies because this is a high-risk strategy where the idea is to maximize gain and/or minimize losses.

Using Moving Average of Stock closing price as a Criteria, the graph shows points of BUY / SELL (Entry / Exit) recommendations when the 50-day moving average stock price goes below/under the 100-day moving average.
    
### 6.3.2.	Exponential Moving Average

The exponential weighted moving average reacts more significantly to recent price changes than a simple moving average (SMA), which applies an equal weight to all observations in the period. 

It is used to highlight trends and illustrate the price trajectory of a stock.

    
### 6.3.3.	Bollinger Banda

It is a technical analysis tool for generating oversold or overbought signals composed with three lines: A simple moving average low, middle and upper band.
    
It can tell you how closer the price moves to the upper band (more overbought the market), and the closer the price moves to the lower band (the more oversold the market)

### 6.3.4.	Random Forest Model

A random forest is a meta estimator that fits a number of decision tree classifiers on various sub-samples of the dataset and uses averaging to improve the predictive accuracy and control over-fitting. The sub-sample size is controlled with the max_samples parameter if bootstrap=True (default), otherwise the whole dataset is used to build each tree.

### 6.4.	Predictions with Machine Learning Techniques

### 6.4.1.	LSTM RNN Predicted vs Actual Stock Price with Bollinger 

Long Short-Term Memory (LSTM) Model to Predict Stock Prices are powerful in sequence prediction problems because they're able to store past information. 

### 6.4.2.	Predicted vs Actual Return

Actual daily return (%) vs. predicted return.

The graph is to visualize how the model is accurately with the actual daily return over the period.


### 6.4.3.	ARMA Forecast

The Auto Regressive Moving Average (ARMA) model consists of two parts, an autoregressive (AR) part and a moving average (MA) part. The Auto Regressive part involves regressing the variable on its own lagging(past) values.

The ARMA model uses past values to predict future stock price.

### 6.4.4.	ARIMA Forecast

The Auto Regressive Integrated Moving Average (ARIMA) model is a famous and widely used forecasting method for time-series prediction. ARIMA models can capture a suite of different standard temporal structures in time-series data. The model is a measure of how many non-seasonal differences are needed to achieve stationarity. 

The ARIMA model uses past values and error to predict future stock price.

If no differencing is involved in the model, then it becomes simply an ARMA.

### 6.4.5.	Volatility Forecast.

GARCH model is used to predict volatility of the stock price, based on the variance across the period. 

Remember: HIGHER VOLATILITY = MORE RISK

### 7. Room for Improvement:

* Adding more parameters to build better prediction model.

* Adding more modelling options.

* Improve the Dashboard running speed.

### 8. Q&A Session 

Q: What stock was used as an example?

*A*: We used VISA Inc. (Ticker: V), but before you run the code you can choose a different ticker in the drop drown menu, according to YAHOO FINANCE.

Q: How many models (algorithms) did the group use?

*A*: we used 5 models: Random Forest, LSTM RNN, ARMA, ARIMA and GARCH.

Q: What kind of problems did you get during the project?

*A*: Our first attempt to plot the graph failed due to the fact that it has different scales, which we fixed using DASH app. This is how we later decided to present our dashboard.

*DASH App is a data visualization software that transforms data from custom and standard objects into an interactive system of clickable charts that show real-time information.

Q: Who is our target?

*A*: This is a platform for Advanced (experienced) investors and/or portfolio managers, where the main idea is to decrease human judgment when trading. So it’s essentially a tool to help the trader to interpret data in order to maximize gain and minimize losses.
