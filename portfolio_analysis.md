# *Portfolio Analysis*

## *Description* 
  The analysis focuses on an account statement obtained from an Excel file, dissecting various aspects such as closed positions, dividends, financial summary, account activity, and portfolio equity. Utilizing Pandas, Plotly, and Altair, this project aims to give comprehensive visualizations and insights into the data provided for an informed decision by the portfolio managers and a comprehensive visualization to the account owner.

## *Code Summary*

### *Importing and Organizing Data:* 
  Loaded financial data from an Excel file and organized it into different DataFrames for easy analysis using pandas read_csv function. For the different sheets in the excell file it was split into different data frames for easier manipulation and understanding. 

Reading:
```    df = pd.read_excel(file_path, sheet_name=None) ```

Spliting into different Data Frames:
```
account_summary =df['Account Summary']
closed_positions=df['Closed Positions']
account_activity=df['Account Activity']
dividends=df['Dividends']
financial_summary=df['Financial Summary']
portfolio_equity=df['Portfolio Equity'] 
```
### *Exploratory Analysis* 
  Explored each sheet's data, checked for null values, and filled missing values appropriately. Also provided analysis on dividends received, deposits made over the years. On the positions closed over time it was possible to calculate profit/losses made, fees paid, and most profit and losses made by asset. Analysing the Portfolio Equity it was possible to identify the growth of the portfolio, cummulative returns and drawdown over time.

#### *Key findings:*
1. Through the exploration of the dividend sheet it was possible to identify which dates dividends are mora abundant. That's good for an investor to have a more predictability on the cashflow provided by his investments. It was also possible to see how much dividends where paid during the period analysed along with a visualisation on the top 10 dividend payers of the portfolio.

<img src="images/top_ten_div.png?raw=true"/>

2. It is visible that the most profit was made through selling of crypto assets followed by CFDs and, the stocks purchased during the period weren't profitable, being the only asset class that made a loss.

<img src="images/amount_by_asset.png?raw=true"/>


  That is also represented on the most profitable assets seen in the picture:

<img src="images/profit_by_asset.png?raw=true"/>


  This could be a reflection of the asset volatility or a portfolio more aligned towards crypto assets. 

3. The account activity displayed a constant deposit over time of an average of $700.00, having just one big outlier in october 2020 with an unusual ammount deposited of more than $6000.00. It was possible to determine the total accumulated deposits over the period, an important metric to define it the portfolio was profitable over time.

<img src="images/deposits.png?raw=true"/>

It was possible to determine the total accumulated deposits over the period, an important metric to define it the portfolio was profitable over time.

<img src="images/total_deposits.png?raw=true"/>

4. It's possible to see that the portfolio holds $1763.00 on average of it's capital in cash. For a portfolio manager it is important to keep a portion of it's capital allocated to make any further allocations without having to realize other positions. It shows that the portfolio is active and have an active approach buying and selling assets.

5. The portfolio value over time accounts for the deposits and for that reason it is necessary to take that factor in. The picture shows the difference between them where on the top the deposits covers the losses made. Prudence is advised when analysing a portfolio appreciation over time and improper understanding of it's metrics can lead to an unrealistic performance values. In this case the net growth is 471.36% opposed to 4024.47% without taking the deposits from the total portfolio value.

<img src="images/comparison_portfolio_value.png?raw=true"/>

6. The drawdown metric is used to determine how much the portfolio dropped in a particular period of time. This is important to measure the potential loss of a portflolio and how much an investor can expect to lose. The portfolio shows a drawndown of 8.07% on a monthly average and maximum of 31.22% on a single month. 

<img src="images/drawdown.png?raw=true"/>

### *Benchmarking with SPY* 
  Compared portfolio equity with SPY (S&P 500 ETF) prices to gauge performance including an insight on what it would be discounted the deposits made over time for a more precise understanding of the performance. Other instrument could be used for comparisson such as gold, inflation, and others. Considering composition of the portfolio having more volatile assets from the US stock market S&P 500 was chosen as the main comparison. To do that it was needed to import data from an outside data source (Yahoo Finance) using the code:

```
import yfinance as yf

ticker_symbol = 'SPY'
start_date = '2020-01-02'
end_date = '2024-01-01'

spy_data = yf.download(ticker_symbol, start=start_date, end=end_date)
spy_data = spy_data.reset_index()
```
#### *Key findings:*
1. There was a clear upward trend in the fees for the first two months of activity that stabilized after that. Changes in trading strategy or larger fees associated with deposits could the the cause. More data needed to support the hypothesis.

<img src="images/fees.png?raw=true"/>

3. The total profit of the portfolio in the period was $4579.

4. The profit over time has a mean of  1.37, indicating a very low profit in majority of the positions, having the maximum loss of $-595 and maximum profit at $740. Could sugest a fast trading strategy focused on quantity of trades more than long term investing strategy. This is evidenced by the ammount of trades made and how long for the position to be closed. I found out that 34 trades were made with a duration of 39 days being the largest by far from other position durations.

<img src="images/longest_positions.JPG?raw=true"/>

5. The benchmark showed an appreciation in value of 70% against 471.36% of the portfolio demonstrating a good portfolio and risk management.

<img src="images/portvsspy.JPG?raw=true"/>


## *Conclusion* 
  This project showcases an approach to financial portfolio analysis, offering insights into profits, losses, dividends, and overall portfolio performance. The visualizations provide a clear understanding of financial trends, aiding in an informed decision-making by the portfolio manager. 
  
  Sugestions on improvement are on the focus on the quality of the trades with an attempt to improve the average of profit per trades. This could lead to a better performance with a net equity greater than the benchmark.
  
  Better understanding on the risk management can improve both short_lived trading profits, reduce losses, and help get a performance boost against the benchmark. But overall it has a good performance against the compared SPY asset. 



You can find the link for the code [here](https://github.com/RafaelBaltazar/RafaelBaltazar.github.io/blob/main/projects/Portfolio%20Analysis/portfolio_analysis.ipynb).
