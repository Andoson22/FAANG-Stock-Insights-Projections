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

![image]()

#### We can see the upward trend in the series above.

#### Below we can see our model fitting the AMZN data as it takes in new points as 'history' and uses each point from the past to make future decisions ('predictions').

![image]()

#### Recommendations
1. Invest in any stocks that are currently on a downswing.  We should look at these stocks as if they are 'on sale' and we can get them for a cheaper price to maximize our return-on-invest for long term growth when we plan to hold.  These stocks have more potential for growth due to the overarching upward trend of the stocks selected mixed with the current low price and certainly prove to be a recipe for success.
2. Don't exit positions just because a stock starts to go down.  A lot of amatuer investors and inexperienced traders may experience panic selling in the markets, but many stocks have autoregressive properties, and usually the news cycle won't impact the fundementals underlying a 'strong' stock.
3. If a stocks' industry is trending upward, it may be a good time to get in before that stock catches up with the rest of the pack.  Many stocks within industries tend to move up and down together.  This is due to the similar markets that affect them.

## Conclusion

To summarize our findings, we have identified that there seem to be no clear 'lag indicators' in the data that stick out, other than the overall upward trend/growth of the stock market as a whole.  There was a non-significant but noticeable lag around quarterly/annual reporting periods.

When looking to pick the safest stock to invest in of the FAANG group(i.e- safest but lowest reward), I recommend Apple as your go to pick (Projected Y2Y ROI of -2.7% to 19.7%).  If you're looking for the stock with the most upside from these 5, I recommend Facebook as the best option (Projected Y2Y ROI of -33.81% to 48.72%).

Most of these stocks seem to rise and fall together, and the prices changes are highly correlated with one another.  This would suggest these stocks as a whole trend down and up together.  (Note- not sure if this is due to the natural markets, news cycle, etc.)

I recommend to invest in a diversified portfolio of stocks, that include mostly safe options, but also some riskier/more rewarding options...bonus if the stock is currently on a downswing.  We should look at these stocks as if they are 'on sale' and we can get them for a cheaper price to maximize our return-on-invest for long term growth when we plan to hold.  These stocks have more potential for growth due to the overarching upward trend of the stocks selected mixed with the current low price and certainly prove to be a recipe for success.


#### Future Work

Look into stocks in multiple sectors other than tech.  It would be interesting to see if there are any obvious patterns from businesses that have super seasonal revenue streams and if that has an impact on stock price.  

Building a model that factors in product releases, news cycles, or company quarterly reports (although somewhat nuanced, could potentially be a clear indicator).  Use a mix of models somewhat like modern day stock traders that use complicated algorithms and graphical patterns to identify trends in data. 

Identifying optimal time intervals to hold stocks.  It is almost impossible to get in stocks at the absolute lows, and out at the absolute highs to maximize profits...since all indicators are 'lagging' indicators.  This is much more important when trading stocks daily rather than identifying simple long-term stocks to buy and hold. 

See if there is a strong link of price movement between certain stocks in the same industry and see if we can identify which 'controls' the market.  (i.e- Bitcoin moving before most other cryptos move with it...)

Research stock investing to see what percent of trading is done by bots, and what the bots are responding to. (i.e- news data, actual AR/MA trends...what are they optimized to do)

See if longer time series (i.e- more mature stocks) provide better predictive qualities or if new data is exponentially more important.
