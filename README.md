# PHBS_BlockChain_2018

## Analysis of the dynamic relationship between the Bitcoin prices of the United States, South Korea and Japan

YanrongWu（Rhea） 1801212952  Fintech

### Abstract
This paper analyzes the Bitcoin price relationship between the United States, Korea and Japan. I collect data on three currency pair prices for the period May 2013 to March 2019 and analyze of which currency market is the leader of Bitcoin prices using VEC model. At this stage, the results suggest that the US market has a profound impact on the Japanese and Korean Bitcoin markets. For the sake of comparison, I also study the data before the tightening of supervision in Korea and Japan. By collecting and analyzing prices for the period May 2013 to December 2017，the result could show that before 2018, Asian market is the leader of Bitcoin prices. The reason for this difference may be due to regulations in Korea (Dec 2017) and panic caused by unsafe accidents in Japanese Bitcoin transactions.

### Keywords: Bitcoin, Cryptocurrencies, VEC Model, Price discovery


### 1. Introduction
Bitcoin is a decentralized peer-to-peer cryptocurrency protocol that was first proposed in a paper by Nakamoto (2008). Since its first launch in 2009, Bitcoin has evolved from an experimental commodity to a booming virtual currency that has received public attention. In 2013, Bitcoin prices soared, making Bitcoin's market capitalization more than $1 billion, and rapidly growing to $217 billion at the end of 2017 [(coinmarketcap.com)](https://coinmarketcap.com). The Bitcoin user base is becoming more and more global and diversified. Due to regulations and other factors, the bitcoin market has fallen back in 2018. Currently, Bitcoin's market capitalization is around $92 billion.

Fig.1 Market Cap& Price from 2013/05/01 to 2019/03/31（Source：[coinmarketcap.com](https://coinmarketcap.com)）
![Market Cap](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/MarketCap.png)
![Exchange volume distribution](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/Exchange%20volume%20distribution.png)

Data on 2019/03/31（Source：[data.bitcoinity.org](https://data.bitcoinity.org)）

Because of the decentralized structure, no central authority has direct control over the Bitcoin exchange rate. However, regulatory issues still influence the exchange rate between Bitcoin and other currencies. One example is the process of withdrawing and depositing – the easier and cheaper this process is at a particular exchange, the more users it gains and the price at this exchange changes accordingly. This can lead to different prices at different exchanges, an effect we will discuss later.

Fig.4 US Exchange（Source：[coinmarketcap.com](https://coinmarketcap.com)）
![US Exchange](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/US%20Exchange.png)
Fig.5 Japan Exchange
![Japan Exchange](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/Japan%20Exchange.png)
Fig.6 Korea Exchange
![Korea Exchange](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/Korea%20Exchange.png)

The purpose of this paper is to further investigate this multi-exchange environment, especially the price discovery of Bitcoin exchanges and to know which exchange has a guiding role in the Bitcoin market. To decide whether an exchange is a leader or a follower, we can use the following way of thinking: if the exchange is related to a lagging market return, not the market return at that time, then the exchange is a follower. If the opposite is true, then the exchange will lead the market.

Most of the previous literature focused on the generation of Bitcoin, the development of regulatory policies, and the relationship between Bitcoin prices at different exchanges, and how to test short-term causal links and correlation analysis. Buchholz et al. (2012) conclude that Bitcoin price is mainly driven by its supply and demand in the market, the demand for Bitcoin is mainly determined by the value of it as a medium of exchange. Yermack (2013) argues that Bitcoin is an investment asset or speculative tool rather than a currency. Bitcoin price is highly correlated with its own trading characteristics, has no correlation with classical currencies, and is not influenced by macroeconomic events. Bouoiyour & Selmi (2014) attempt to describe Bitcoin value by regressing its market price against a number of independent variables including the market price of gold and so on. This article aims to determine the relationship between the Bitcoin prices in different exchanges. For the model selection, I decide to use the VEC Model.

Cointegration test and the vector error correction (VEC) model are suitable technical methods to describe the dynamic effects of the interaction and disturbance between the non-stationary time series. Cointegration test is to determine whether there is a stable linear combination between a collection of non-stationary time series. The linear combination is called the cointegration equation, which reflects the long-run equilibrium relationship between these non-stationary variables. 

Johansen established VAR model with cointegration constraints, which is known as vector error correction (VEC) model, to describe the long-run equilibrium relationship and short-term deviation and reveal the dynamic attribute of the system. Saša Žiković et al. (2014) use VECM approach to detangling growth, exports, imports and FDI knot in selected CEE countries. Kristoufek (2013) analyzes the search queries on Google Trends and Wikipedia affecting Bitcoin and study their relationship，which shows that not only are the search queries and the Bitcoin prices connected but there also exists a pronounced asymmetry. So we can also use VEC model to analyze the dynamic relationship between the Bitcoin prices of US, Korea and Japan.


### 2. Model
#### 2.1	Stability Test 
In order to judge the stability of a variable, a unit root test is required. Unit root test methods include Dickey and Fuller, Phillips-Perron, Augmented Dickey and Fuller (ADF), etc. In the DF test, the time series is assumed to be regarded as the error term of the first-order autoregressive process AR(1) with random white noise. During the test, a time series needs to be obtained by higher order autoregressive analysis. When adding the white noise characteristic of the random error term in DF, it should be confirmed that the random error term is white noise. With Dicky and Fuller, the existing inspection process can be extended to implement the ADF (Augment Dickey-Fuller) test. 

Assume the following:

![Fomula 1](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/Fomula%201.png)

#### 2.2 Cointegration Test
The cointegration is actually a common random trend. To achieve the cointegration test, we also confirm the linear combination of a set of non-stationary sequences, and seek a stable equilibrium relationship. In special cases, a pseudo-regression problem will occur. At this point, there are two time series with the same trend component. To make the regressions corrected to get reliable results, use this relationship for cointegration. Through cointegration, it is possible to transfer long-term equilibrium relationships and find variable relationships that present a trend of randomness. Aiming at this kind of connection, the introduction of “relatively stable” can realize the reliability adjustment of the model. For example, if we want to apply the VAR model, we need to ensure that all variables have the random tendency of the unit root eliminated, so we can get error-corrected model.

Assume the following：

![Fomula 2](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/Fomula%202.png)

#### 2.3 VAR Model
As a common econometric model, the vector autoregressive model is also called the VAR model. The model, proposed by Christo¬pher Sims, is a statistical model that needs to be based on data analysis. Using this model, the transformation of each endogenous variable in the system can be achieved. Using the obtained lag value function, the model can be established to realize the transformation from univariate to multivariate time series variables, and then a new "vector" autoregressive model is obtained. With a certain degree of stability, by examining the ADF unit roots, we can know that the ADF unit roots of the US, South Korea, and Japan bitcoin prices are significantly less than 1% and 5%.

The VAR model is:

![Fomula 3](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/Fomula%203.png)

Among them, Y_t is a column vector composed of bitcoin prices in the United States, South Korea, and Japan.

#### 2.4 VECM Model
In the above VAR model, although the relationship between the variables is not stable, but there is a cointegration relationship with each other, the error correction model(VECM) can be obtained by transformation. ECMs are a theoretically-driven approach useful for estimating both short-term and long-term effects of one time series on another. The term error-correction relates to the fact that last-period's deviation from a long-run equilibrium, the error, influences its short-run dynamics. In addition, the error correction model can also determine whether the short-term relationship between variables is a permanent deviation or a temporary deviation.

This report focuses on empirical research, so does not describe much in method theory.

### 3. Empirics
The empirical analysis of this paper consists of four steps:
First, study whether the time series has stationarity and determine the model lag period.
Second, research on Japan, South Korea and the United States Bitcoin to test whether there is a cointegration relationship.
Third, if it is determined that different variables have a cointegration relationship, then an error correction model is constructed based on the specific situation.
Fourth, analyze the dynamic linkages of different variables through exchanges and lagging market returns.
This paper uses Eviews software to analyze data.

Table 1: Descriptive Statistics

Variable | Mean | Median | Maximum | Minimum | Skewness | Kurtosis | Std. Dev. | Jarque-Bera
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
usd | 2381.0900  | 620.9900 | 19665.39 | 67.8090 | 2.024991 | 7.295408 | 3392.244 | 3135.307
krw | 2380.524 | 621.0051 | 19660.16 | 66.3586 | 2.025302 | 7.298469 | 3392.411 | 3138.127 
jpy | 2382.826 | 620.2965 | 19714.90 | 66.2551 | 2.026480 | 7.307500 | 3396.303 | 3146.837 

#### 3.1 ADF Test
To apply the VAR model, we need to ensure that all variables have a certain degree of stability. By examining the ADF unit roots, we can know that the ADF unit roots of the US, South Korea, and Japan Bitcoin prices are significantly less than the 1% and 5% horizontal thresholds. So their time series are unstable sequences. Therefore, it is necessary to negate the original hypothesis and use the method of splitting to process the data so that the ADF unit root test result is not more than 1% of the critical value, indicating that when the 99% confidence level is required, the original hypothesis needs to be rejected, and the split sequence is Without a unit root, the time series has a smoothness that conforms to the standard, that is, the three sequences are first-order single-integer sequences.

Table 2: ADF Statistics

Variable | ADF Statistic | 5%Critical Value | 1%Critical Value | P Value | Conclusion
------------ | ------------- | ------------- | ------------- | ------------- | -------------
usd | -1.503252 | -1.940972 | -2.566044 | 0.1245 | unstable 
krw | -1.503228 | -1.940972 | -2.566044 | 0.1246 | unstable 
jpy | -1.499779 | -1.940972 | -2.566044 | 0.1254 | unstable 
Dusd | -8.764657 | -1.940972 | -2.566044 | 0.0000 | stable 
Dkrw | -8.880809 | -1.940972 | -2.566044 | 0.0000 | stable 
Djpy | -8.781487 | -1.940972 | -2.566044 | 0.0000 | stable 

#### 3.2 Analysis Determines the Lag Order
The cointegration test and the estimation of the VAR model are affected by the lag order. In the process of judging the lag order, it can be combined with HQ, SC, AIC, FPE and LR criteria, and 8 is set for these criteria information. The lag order is shown in the table below.

Table 3: Lag determination

Lag | LogL | LR | FPE | AIC | SC | HQ
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
0 | -38262.42 | NA | 5.68e+11 | 35.57919 | 35.58710 | 35.58208
1 | -32580.57 | 11342.56 | 2.91e+09 | 30.30458 | 30.33623* | 30.31615 
2 | -32556.18 | 48.63012 | 2.87e+09 | 30.29026 | 30.34565 | 30.31053 
3 | -32539.69 | 32.81264 | 2.85e+09 | 30.28330 | 30.36244 | 30.31225 
4 | -32516.63 | 45.84687 | 2.81e+09 | 30.27023 | 30.37310 | 30.30786 
5 | -32500.60 | 31.81874 | 2.79e+09 | 30.26369 | 30.39030 | 30.31001 
6 | -32440.23 | 119.6766 | 2.66e+09 | 30.21593 | 30.36628 | 30.27093 
7 | -32417.90 | 44.19515* | 2.63e+09* | 30.20354* | 30.37763 | 30.26722* 
8 | -32412.02 | 11.662936 | 2.64e+09 | 30.20644 | 30.40426 | 30.27881 

*Note:*indicates lag order selected by the criterion

LR: sequential modified LR test statistic(each test at 5% level)

FPE: Final prediction error

AIC: Akaike information criterion

SC: Schwarz information criterion

HQ: Hannan-Quinn information criterion

#### 3.3 Johansen Cointegration Test
In the process of analyzing the cointegration relationship of different variables, this topic applies the method of cointegration test. According to the data of Table 3, the JJ test is performed under the condition of the eighth-order lag order, and the test result is shown in Table 4. Analysis of Table 4 shows that there are two cointegration relationships for the three variables at the 1% critical level. That is, the co-integration relationship of Bitcoin prices in the United States, South Korea, and Japan has a long-term nature.

Table 4: Johansen Cointegration Test

Hypothesized No. of CE(s) | Trace Statistic | 5%Critical Value | P Value | Max-Eigen Statistic | 5%Critical Value | P Value
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
None* | 859.7598 | 29.79707 | 0.0000 | 458.7435 | 21.13162 | 0.0000
At most 1* | 401.0163 | 15.49471 | 0.0000 | 398.4181 | 14.2646 | 0.0000 
At most 2* | 2.598184 | 3.841466 | 0.1070 | 2.598184 | 3.841466 | 0.1070 

*Note: Trace test indicates 2 cointegrating eqn(s) at the 0.05 level

Max-eigenvalue test indicates 2 cointegrating eqn(s) at the 0.05 level

*denotes rejection of the hypothesis at the 0.05 level

#### 3.4 VEC Model
The Error Correction Model (VECM) is a VAR model based on cointegration. In the process of analyzing the dynamic relationship between Bitcoin prices in Japan, Korea and the United States, an error correction model was constructed based on VAR.

Table 5: VEC Model

![VECM](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/VECM.png)
*Note: Standard errors in()& t-statistics in []

![Result 1](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/Result%201.png)

If we take the price data from 2013/5/1 to 2017/12/31, the result can be show:

![Result 2](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/Result%202.png)


#### 3.5 Result Analysis
The Johansen cointegration test has shown that bitcoin prices in the United States, South Korea, and Japan have a balanced relationship that maintains good stability over a long period of time. So it can be known that there is an inherent equilibrium mechanism in the market. 

When the market price in a certain period deviates from the long-term equilibrium point, the market equilibrium mechanism will continue to be in equilibrium through subsequent adjustments. Therefore, the error correction model can be constructed according to the above formula.

During 2013/05/01-2019/03/31, the price of Bitcoin in US has a significant impact on Korea and Japan Bitcoin prices after a period of lag in the short-term. There is a two-way causal relationship between Korean Bitcoin prices and Japanese Bitcoin prices. US Bitcoin market is the price leader.

Compared with the results of data analysis before 2018, the United States was not the dominant player in the Bitcoin market before 2018. On the contrary, the trading volume of Bitcoin in Japan and South Korea accounted for more than half of the global transaction volume. At that time, the Asian market was the Bitcoin price leader. 

In the short-term, South Korea and Japan Bitcoin prices have a significant impact on US Bitcoin prices after a period of lag, whereas US Bitcoin prices have no significant impact on Korea or Japan bitcoin prices. This is different from the results from the data from 2013/05/01 to 2019/03/31. We believe that it was due to the strong supervision of Bitcoin in South Korea at the end of 2017, and also because of the frequent outbreaks of Bitcoin exchanges in Japan, such as the bankruptcy of Mt. Gox, It also has a strongly negative impact on the Japan Bitcoin market transactions.


### Conclusion
Based on the above empirical test and analysis of results, we can get the following conclusions: 

(1) The US, South Korea, and Japan Bitcoin price time series do not have good stability, these time series have good stability in the first-order difference. The equilibrium relationship between these time series has long-term, and different variables will influence and interact with each other under the adjustment of long-term equilibrium relationship.

(2) In the short term(2013/05/01-2019/03/31), the price fluctuations of Bitcoin in US have a strong impact on South Korea and Japan Bitcoin prices and play a guiding role in the Bitcoin market; while Korean Bitcoin price fluctuations have less impact on the US Bitcoin markets.

(3)Using the data from 2013/05/01 to 2017/12/31, we can know during this period, US market isn't the price leader but Japan and Korea have a significant impact on US Bitcoin price after a period of lag. The reason for this difference may be due to the regulatory behavior of Bitcoin in the Asian market. We can alse use VEC model to analyze factors affecting the price of Bitcoin.

### References
[1] Buchholz, M., Delaney, J., Warren, J., et al. (2012). Bits and Bets, Information, Price Volatility,and Demand
for Bitcoin. Economics, 312.

[2] Bouoiyour, J., Selmi R. (2014), What Bitcoin Looks Like?, MPRA Paper, University Library of Munich, Germany

[3] Kristoufek, L. (2013). BitCoin meets google trends and wikipedia: Quantifying the relationship between phenomena of the internet era. Scientific Reports (Nature Publisher Group), 3, 3415. doi:http://dx.doi.org/10.1038/srep03415

[4] Yermack, D. (2015). Is bitcoin a real currency? an economic appraisal. National Bureau of Economic R
esearch. doi:10.1016/B978-0-12-802117-0.00002-3

[5] Zikovic, S., Zikovic, I. T., & Grdinic, M. (2014). A VECM approach to detangling growth, exports, imports and FDI knot in selected CEE countries. Croatian Operational Research Review, 5(2), 161-175. Retrieved from https://search.proquest.com/docview/1663359065?accountid=13151
