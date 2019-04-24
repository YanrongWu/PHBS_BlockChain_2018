# PHBS_BlockChain_2018

## Analysis of the dynamic relationship between the bitcoin prices of the United States, South Korea and Japan

### Abstract

### 1. Introduction
Bitcoin is a decentralized peer-to-peer cryptocurrency protocol that was first proposed in a paper by Nakamoto (2008). Since its first launch in 2009, Bitcoin has evolved from an experimental commodity to a booming virtual currency that has received public attention. In 2013, bitcoin prices soared, making Bitcoin's market capitalization more than $1 billion, and rapidly growing to $217 billion at the end of 2017 (coinmarketcap.com). The Bitcoin user base is becoming more and more global and diversified. Due to regulations and other factors, the bitcoin market has fallen back in 2018. Currently, Bitcoin's market capitalization is around $92 billion.

Because of the decentralized structure, no central authority has direct control over the Bitcoin exchange rate. However, regulatory issues still influence the exchange rate between Bitcoin and other currencies. One example is the process of withdrawing and depositing – the easier and cheaper this process is at a particular exchange, the more users it gains and the price at this exchange changes accordingly. This can lead to different prices at different exchanges, an effect we will discuss later.
![US Exchange](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/US%20Exchange.png)
![Japan Exchange](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/Japan%20Exchange.png)
![Korea Exchange](https://github.com/YanrongWu/PHBS_BlockChain_2018/blob/master/Korea%20Exchange.png)
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

### 3. Empirics
The empirical analysis of this paper consists of four steps:
First, study whether the time series has stationarity and determine the model lag period.
Second, research on Japan, South Korea and the United States Bitcoin to test whether there is a cointegration relationship.
Third, if it is determined that different variables have a cointegration relationship, then an error correction model is constructed based on the specific situation.
Fourth, analyze the dynamic linkages of different variables through exchanges and lagging market returns.


#### 3.1 ADF Test
To apply the VAR model, we need to ensure that all variables have a certain degree of stability. By examining the ADF unit roots, we can know that the ADF unit roots of the US, South Korea, and Japan bitcoin prices are significantly less than the 1% and 5% horizontal thresholds. So their time series are unstable sequences. Therefore, it is necessary to negate the original hypothesis and use the method of splitting to process the data so that the ADF unit root test result is not more than 1% of the critical value, indicating that when the 99% confidence level is required, the original hypothesis needs to be rejected, and the split sequence is Without a unit root, the time series has a smoothness that conforms to the standard, that is, the three sequences are first-order single-integer sequences.

#### 3.2 Analysis Determines the Lag Order
The cointegration test and the estimation of the VAR model are affected by the lag order. In the process of judging the lag order, it can be combined with HQ, SC, AIC, FPE and LR criteria, and 8 is set for these criteria information. The lag order is shown in Figure below.

#### 3.3 Johansen Cointegration Test
In the process of analyzing the cointegration relationship of different variables, this topic applies the method of cointegration test. According to the data of Fig. 1, the JJ test is performed under the condition of the eighth-order lag order, and the test result is shown in Fig. 2. Analysis of Figure 2 shows that there are two cointegration relationships for the three variables at the 1% critical level. That is, the co-integration relationship of bitcoin prices in the United States, South Korea, and Japan has a long-term nature.

#### 3.4 VEC Model
The Error Correction Model (VECM) is a VAR model based on cointegration. In the process of analyzing the dynamic relationship between bitcoin prices in Japan, Korea and the United States, an error correction model was constructed based on VAR.

#### 3.5 Result Analysis
The Johansen cointegration test has shown that bitcoin prices in the United States, South Korea, and Japan have a balanced relationship that maintains good stability over a long period of time. So it can be known that there is an inherent equilibrium mechanism in the market. 
When the market price in a certain period deviates from the long-term equilibrium point, the market equilibrium mechanism will continue to be in equilibrium through subsequent adjustments. Therefore, the error correction model can be constructed according to the above formula.
In the short-term, the price of bitcoin in US has a significant impact on Korea and Japan bitcoin prices after a period of lag. There is a two-way causal relationship between Korean bitcoin prices and Japanese bitcoin prices. US Bitcoin market is the price leader.

### Conclusion
Based on the above empirical test and analysis of results, we can get the following conclusions: (1) The US, South Korea, and Japan bitcoin price time series do not have good stability, these time series have good stability in the first-order difference. The equilibrium relationship between these time series has long-term, and different variables will influence and interact with each other under the adjustment of long-term equilibrium relationship.
(2) In the short term, the price fluctuations of bitcoin in US have a strong impact on South Korea and Japan bitcoin prices and play a guiding role in the bitcoin market; while Korean bitcoin price fluctuations have less impact on the US bitcoin markets.

### References
