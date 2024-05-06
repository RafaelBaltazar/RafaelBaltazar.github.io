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

![Alt text](https://top_ten_div.jpg)

2. It is visible that the most profit was made through selling of crypto assets followed by CFDs and, the stocks purchased during the period weren't profitable, being the only asset class that made a loss.

![Alt text](https://amount_by_asset.jpg)

That is also represented on the most profitable assets seen in the picture:

![Alt text](https://amount_by_asset.jpg)

This could be a reflection of the asset volatility or a portfolio more aligned towards crypto assets. 

3. The account activity displayed a constant deposit over time of an average of $700.00, having just one big outlier in october 2020 with an unusual ammount deposited of more than $6000.00. It was possible to determine the total accumulated deposits over the period, an important metric to define it the portfolio was profitable over time.

![Alt text](https://deposits.jpg)    ![Alt text](https://total_deposits.jpg)

4. It's possible to see that the portfolio holds $1763.00 on average of it's capital in cash. For a portfolio manager it is important to keep a portion of it's capital allocated to make any further allocations without having to realize other positions. It shows that the portfolio is active and have an active approach buying and selling assets.

5. The portfolio value over time accounts for the deposits and for that reason it is necessary to take that factor in. The picture shows the difference between them where on the left the deposits covers the losses made. Prudence is advised when analysing a portfolio appreciation over time and proper understanding of it's metrics can lead to an unreal impression. In this case the net growth is 471.36% opposed to 4024.47% without taking the deposits from the total portfolio value.

![Alt text](https://comparison_portfolio_value.jpg)

6. The drawdown metric is used to determine how much the portfolio dropped in a particular period of time. This is important to measure the potential loss of a portflolio and how much an investor can expect to lose. The portfolio shows a drawndown of 8.07% on a monthly average and maximum of 31.22% on a single month. 

![Alt text](https://drawdown.jpg)

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


## *Conclusion* 
This project showcases an approach to financial portfolio analysis, offering insights into profits, losses, dividends, and overall portfolio performance. The visualizations provide a clear understanding of financial trends, aiding in an informed decision-making by the portfolio manager. 

You can find the link for the code [here](https://github.com/RafaelBaltazar/RafaelBaltazar.github.io/blob/590f7836deb1410fbc6ab95c17181532a7ad282d/projects/Portfolio%20Analysis/portfolio_analysis.ipynb).
