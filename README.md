### Project overview
This project is a small analytics study implemented in a Jupyter notebook with Python. It uses daily data for the S&P 500 index, Apple (AAPL), and Tesla (TSLA) to examine risk and return characteristics, estimate Sharpe ratios, and run simple Capital Asset Pricing Model (CAPM) regressions.
The notebook shows end-to-end work:
- Importing and merging raw price series from Excel files
- Constructing daily log percentage returns
- Building a constant risk-free series
- Computing annual Sharpe ratios and then focusing on the index and the two stocks
- Estimating CAPM alpha and beta for AAPL and TSLA with ordinary least squares and with the covariance formula
- Producing visual summaries of returns, cumulative performance, volatility, and time varying beta


### Data
The notebook uses three Excel workbooks:
- S&P 500.xlsx
- AAPL.xlsx
- TSLA.xlsx

The historical price data for all three securities was sourced from Yahoo Finance and compiled in Excel for analysis.


### Interpretation of results
The project answers several standard questions from an equity analyst perspective.
- Which asset had the highest risk-adjusted performance over the sample period?
Based on the annual Sharpe ratios, TSLA delivered the highest return per unit of volatility, followed by AAPL and the market index.
- How sensitive are AAPL and TSLA to broad market movements?
Both stocks have beta greater than one, so they amplify market movements. TSLA, in particular, exhibits very high beta, which is visible in both the regression estimates and the time series plots.
- How stable are these risk measures over time?
The rolling volatility and rolling beta plots show that risk is not constant. TSLA experiences episodes of extremely high volatility and very high beta, while AAPL and the index are relatively more stable.

These findings are conditional on the sample period and on the choice of a constant risk-free rate.


### Conclusion
When you compare returns to risk, Apple actually appears better. Yes, Tesla sometimes makes more money during certain periods, but Apple gives you better returns for the amount of risk you're taking.
Both stocks move with the broader stock market, but Tesla reacts much more strongly. When the market goes up or down, Tesla tends to swing even more in that same direction. Apple is more stable and doesn't overreact as much to market changes. This relationship also changes over time, with Tesla sometimes becoming even more sensitive to market swings.
