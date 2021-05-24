## Project Description

For this project, we're looking to identify patterns/seasonality/trends in raw stock data inputs as well as accurately predict future stock prices in order to provide profitable investing advice to investors to obtain a strong ROI (minimizing their MAPE). Accurately determine the best performing stocks over specific time periods and locate best potential times to enter mid to long to positions (holding for weeks-to-years rather than day trading). (As MAPE decreases, ROI naturally increases)

### The Data

The data used comes from :

Amazon, Apple, Facebook, Google, Netflix stock market data

This data is found in the Data folder

### Key Findings

Which stocks are the most profitable for long-term investors?

Are there any obvious entry/exit points for stock positions?

Do we see any trends in the data that we can use to maximize ROI and minimize risk?

![image](https://raw.githubusercontent.com/Andoson22/FAANG-Stock-Insights-Projections/main/Images/AMZN%20szn_decomp.png)

#### Above is the seasonal_decompose of the AMZN stock closing price data.  There seems to be a cyclical trend in the data.  This must be removed in order to perform our desired modeling with ARIMA. (Data is assumed to be stationary.)

![image](https://raw.githubusercontent.com/Andoson22/FAANG-Stock-Insights-Projections/main/Images/rollingmeanstd.png)

#### We can see the upward trend in the series above.

#### Below we can see our model fitting the AMZN data as it takes in new points as 'history' and uses each point from the past to make future decisions ('predictions').

![image](https://raw.githubusercontent.com/Andoson22/FAANG-Stock-Insights-Projections/main/Images/ConfIntwithExpected.png)

## Conclusion

To summarize the findings, we have identified that there seem to be no clear 'lag indicators' in the data that stick out.  There is a clear upward trend/growth for these stocks as a whole.  This makes sense, as over time the stock market as a whole has shown historical growth.  There was a non-significant but noticeable lag around quarterly/annual reporting periods. Apple stock had the safest ROI (highest floor, projected year-to-year ROI of -2.7% to 19.7%).  Facebook stock had the riskiest ROI (lowest floor, projected year-to-year ROI of -33.81% to 48.72%). Most of these stocks seem to rise and fall together, and the prices changes are highly correlated with one another.  This would suggest these stocks as a whole trend down and up together.  (Note- can't be sure if this is due to the stocks being within the same industry, natural markets, news cycle, etc.)

#### Recommendations
1. Diversify your portfolio.  Include a mix of stocks that have limited upside but low risk, with stocks that provide higher risk but also higher potential return on investment.  This will protect your investments from any huge swings an individual stock can suffer from, however, it will cap potential profits but this trade-off is recommended.  

2. Invest in Netflix.  Netflix is the clear-cut safest pick of these stocks according to the models.  Given the 95% confidence interval that Netflix will have an ROI between -15.3% and 64.3%, NFLX stock is the strongest candidate as a 'pick-one' stock if we had to choose just one; this is because they have the highest floor of the group as well as the highest ceiling.

3. Buy stocks "on-sale".  Based on the autoregressive features and cyclical nature of how the stock market operates, buying stocks that are currently on a downswing can provide better potential for high returns on investment.


#### Future Work

- Look into stocks in multiple sectors other than tech.  It would be interesting to see if there are any obvious patterns from businesses that have super seasonal revenue streams and if that has an impact on stock price.  

- Building a model that factors in product releases, news cycles, or company quarterly reports (although somewhat nuanced, could potentially be a clear indicator).  Use a mix of models somewhat like modern day stock traders that use complicated algorithms and graphical patterns to identify trends in data. 

- Identifying optimal time intervals to hold stocks.  It is almost impossible to get in stocks at the absolute lows, and out at the absolute highs to maximize profits...since all indicators are 'lagging' indicators.  This is much more important when trading stocks daily rather than identifying simple long-term stocks to buy and hold. 

- See if there is a strong link of price movement between certain stocks in the same industry and see if we can identify which 'controls' the market.  (i.e- Bitcoin moving before most other cryptos move with it...)

- Research stock investing to see what percent of trading is done by bots, and what the bots are responding to. (i.e- news data, actual AR/MA trends...what are they optimized to do)

- See if longer time series (i.e- more mature stocks) provide better predictive qualities or if new data is exponentially more important.
