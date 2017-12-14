MULTI-FACTOR PORTFOLIO TRADING STRATEGY
=======================================
The project aims to construct portfolios based on the stock selection criteria and trading strategy that invest an equal amount of total account value in stock selected at each rebalancing time point. 

Program is divided into two parts: optimization and implementation. The optimization part optimizes the performance by changing input parameters. After optimal input parameters are determined, they are applied to the out-of-sample period. 

SETUP
=====
Used jupyter notebook as compiler
1.	Install Python3
2.	Install csv
3.	Install pandas_datareader
4.	Install pandas
5.	Install numpy 
6.	Install fix_yahoo_finance 
7.	Install sys
8.	Install datetime 
9.	Install random
10.	Install statsmodels 
11.	Install scipy 

CLASSES AND METHODS
===================

A. SecurityData

Initialize with ticker, marketshare and IPO date of the stocks

B. Portfolio
1. stock_selection(t,m,n,L)
Input – date of selection, 
        period for calculating reversion factor,
        period parameter for calculating momentum factor,
        period parameter for calculating log-return volatility 

2. generate_position(buy_list,pre_buy_list,t,portfolioFactor)
Input – list of selected stocks to construct portfolio,
        list of selected stocks to construct portfolio in the last rebalancing time point,
        date of position generation,
        amount of money invested in each stock

3. max_dd(ser)
Input – series used to calculate max drawdown

4. beta_port(buy_list,panel_data,t)
Input - list of selected stocks to construct portfolio,
        stock data for calculating beta,
        the date of the beta

5. generate_beta_port(panel_data,strategy,m,n,L,U,TC, datelist,mkt)
Input - stock data,
	       function of strategy,
         period for calculating reversion factor,
        period parameter for calculating momentum factor,
        period parameter for calculating log-return volatility,
        period of rebalancing,
        transaction cost,
	       list of dates when the portfolio is constructed,
        market index data

6. backtest_portfolio(panel_data,strategy,m,n,L,U,TC, datelist)
Input - stock data,
	       function of strategy,
         period for calculating reversion factor,
        period parameter for calculating momentum factor,
        period parameter for calculating log-return volatility,
        period of rebalancing,
        transaction cost,
        list of dates when the portfolio is constructed

C. Strategy
1. generate_signal(buy_list,pre_buy_list,t)
Input - list of selected stocks to construct portfolio,
        list of selected stocks to construct portfolio in the last rebalancing time point,
        date of signal generation




CONTACT
=======

Please send bug reports and other feedbacks to:
yliu3007@gatech.edu
