# **Projects**

This repository contains a collection of my projects from different areas of quantitative finance and data science, divided into 3 categories:
- Portfolio Optimization
- Machine Learning
- Derivatives Pricing

A brief description of particular projects and related files is provided below.

## **Portfolio Optimization**

### **Evaluation of SBF120 Stocks Portfolios Performance**

This project presents a comparison of the performance of different portfolios composed of the top 10 stocks from SBF120 - index involving 120 largest stocks from the Paris Euronext exchange. The performance is evaluated for the year 2019, and the constructed portfolios are the following:
- Equally-weighted portfolio - portfolio with equal weights assigned to each stock
- Markovitz minimum-variance portfolio - portfolio with weights minimizing its variance for the covariance matrix calibrated over the years 2017-18 (i.e., portfolio corresponding to the leftmost point on the efficient frontier curve)
- Equally-weighted Risk Contributions portfolio - portfolio with weights proportional to the contribution of each stock to the total variance of the portfolio for the covariance matrix calibrated over the years 2017-18

For each portfolio, the evolution of the value over time is plotted, and Sharpe ratio, as well as maximal drawdown, are obtained.

The following files are related to this project:
- [Evaluation_of_SBF120_Stocks_Portfolios_Performance.ipynb](/Evaluation_of_SBF120_Stocks_Portfolios_Performance.ipynb) - Jupyter notebook containing all the codes
- [sbf120_as_of_end_2018.xlsx](/sbf120_as_of_end_2018.xlsx) - price and market cap data from the end of 2010 to Sep 2021 for the SBF120 stocks as of 2018 end

## **Machine Learning**

### **Bank Marketing Report**

The aim of this project is to analyze a dataset related to the marketing campaigns run by a bank. In order to perform this exercise, 3 classification models are developed to predict whether a given client has subscribed a term deposit or not. The quality of the models is evaluated, and analysis of the impact of particular variables on the target variable is conducted. Insight gained from this exercise may help develop marketing campaigns by optimizing clients targeting actions (and possibly their form), helping to choose clients that are most probable to subscribe a term deposit when targeted, thus decreasing advertising costs. The report is prepared in R.

The following files are related to this project:
- [Bank_Marketing_Report.Rmd](/Bank_Marketing_Report.Rmd) - R code generating the output
- [Bank_Marketing_Report.html](/Bank_Marketing_Report.html) - a notebook in HTML generated based on the above code; it can be downloaded and opened to see the output without running the code

### **Analysis of the Broker-Dealer's Trading Dataset**

This project presents an analysis of the data concerning offers made by a broker-dealer to different clients and their outcome. It includes midprice of a given security, ID of a client making inquiry, indication whether he intends to buy or sell, price offered by a broker-dealer, and the outcome of the deal (whether it was accepted or not).

First, two classification models are developed for each client - Logistic Regression and Linear Support Vector Machine (SVM). The data is divided into the training set and test set. The models are trained on the former, and their performance is assessed on the latter.

Next, clustering using k-means algorithm is applied on the data in order to classify the clients based on their propensity to accept or refuse the deal depending on the offered bid-ask spread.

The following files are related to this project:
- [Analysis_of_the_Broker-Dealer's_Trading_Dataset.ipynb](/Analysis_of_the_Broker-Dealer's_Trading_Dataset.ipynb) - Jupyter notebook containing all the codes
- [trading_data.csv](/trading_data.csv) - the dataset used for the analysis

## **Derivatives Pricing**

### **Pricing Options with PDE Implicit Scheme**

This project presents pricing of the call-spread and put options with a use of partial differential equation (PDE) implicit scheme. Obtained prices are compared with the prices given by Black-Scholes formula.

The following files are related to this project:
- [Pricing_Options_with_PDE_Implicit_Scheme.ipynb](/Pricing_Options_with_PDE_Implicit_Scheme.ipynb) - Jupyter notebook containing all the codes

### **Fast-Reversion Limit of the Heston Model**

This project presents an independent implementation of the 'Fast-reversion Heston' (FRH) model introduced by Mechkov (2015) (https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2418631). By taking the instantaneous variance mean-reversion speed to infinity, the paper attempts to deal with the classic drawbacks of the standard Heston model, such as inability to capture a strong volatility smile for shorter maturities, observed in the market data, or calibration ambiguity - larger variance volatility can be compensated by larger reversion speed. On the other hand, due to infinitely fast reversion, FRH is unable to capture volatility clustering observed in the empirical data.

The functions respective for the FRH are defined, and further used to price European call options. The results are compared with prices obtained with a standard Black-Scholes formula. Next, option pricing under FRH with a use of backward propagation is performed. Finally, the implied volatility surface given by FRH is obtained.

The following files are related to this project:
- [Fast-reversion_limit_of_the_Heston_model.ipynb](/Fast-reversion_limit_of_the_Heston_model.ipynb) - Jupyter notebook containing all the codes
- [Implied_volatility_surface_FRH.png](/Implied_volatility_surface_FRH.png) - a screenshot of the 3D volatility surface plot generated at the end of the code (unable to display directly in notebook)

### **Variance Swap Pricing under the Heston Model**

This project involves pricing of a variance swap under the Heston model with closed-form formula and Monte Carlo methods. Similarly, the most relevant Greeks are obtained with closed-form formulas and finite difference scheme.

The following files are related to this project:
- [Pricing_Variance_Swap_under_Heston.ipynb](/Pricing_Variance_Swap_under_Heston.ipynb) - Jupyter notebook containing all the codes
