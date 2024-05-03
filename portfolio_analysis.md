# *Portfolio Analysis*

## *Description* 
The analysis focuses on an account statement obtained from an Excel file, dissecting various aspects such as closed positions, dividends, financial summary, account activity, and portfolio equity. Utilizing Pandas, Plotly, and Altair, this project aims to give comprehensive visualizations and insights into the data provided for an informed decision by the portfolio managers and a comprehensive visualization to the account owner.

## *Code Summary*

### *Importing and Organizing Data:* 
Loaded financial data from an Excel file and organized it into different DataFrames for easy analysis using pandas read_csv function. For the different sheets in the excell file it was split into different data frames for easier manipulation and understanding. 

Reading:
```    df = pd.read_excel(file_path, sheet_name=None) ```

Spliting into different Data Frames:
```    account_summary =df['Account Summary']```
```    closed_positions=df['Closed Positions']```
```    account_activity=df['Account Activity']```
```    dividends=df['Dividends']```
```    financial_summary=df['Financial Summary']```
```    portfolio_equity=df['Portfolio Equity'] ```

### *Exploratory Analysis* 
Explored each sheet's data, checked for null values, and filled missing values appropriately. Also provided analysis on dividends received, deposits made over the years. On the positions closed over time it was possible to calculate profit/losses made, fees paid, and most profit and losses made by asset. Analysing the Portfolio Equity it was possible to identify the growth of the portfolio, cummulative returns and drawdown over time.

#### *Key findings:*
1. Through the exploration of the dividend sheet it was possible to identify which dates dividends are mora abundant. That's good for an investor to have a more predictability on the cashflow provided by his investments. It was also possible to see how much dividends where paid during the period analysed along with a visualisation on the top 10 dividend payers of the portfolio.

![Alt text](https://top_ten_div.jpg)

2. It is visible that the most profit was made through selling of crypto assets followed by CFDs and, the stocks purchased during the period weren't profitable, being the only asset class that made a loss.

![Alt text](https://amount_by_asset.jpg)

3. The account activity displayed a constant deposit over time of an average of $700.00 , having just one big outlier in october 2020 with an unusual ammount deposited of more than $6000.00. It was possible to determine the total accumulated deposits over the period, an important metric to define it the portfolio was profitable over time.


### *Benchmarking with SPY* 
Compared portfolio equity with SPY (S&P 500 ETF) prices to gauge performance including an insight on what it would be discounted the deposits made over time for a more precise understanding of the performance. Other instrument could be used for comparisson such as gold, inflation, and others.

## *Conclusion* 
This project showcases a superficial approach to financial portfolio analysis, offering insights into profits, losses, dividends, and overall portfolio performance. The visualizations provide a clear understanding of financial trends, aiding in an informed decision-making by the portfolio manager. 

You can find the link for the code [here](https://github.com/RafaelBaltazar/RafaelBaltazar.github.io/blob/590f7836deb1410fbc6ab95c17181532a7ad282d/projects/Portfolio%20Analysis/portfolio_analysis.ipynb).
