# Assignment3

Ref：《资金流量指标MFI》http://www.360doc.com/content/09/0420/11/32668_3197857.shtml

Momentum indicator is a technical indicator that uses the principle of dynamics to study trends and reverse phenomena in the process of transformation. As time becomes smaller and the changing speed and energy gradually slow down, the market may transform. Common momentum indicators include ADX, CMO, MACD, RSI, KDJ, Momentum Index (MOM) and William indicator. 

Recently I have seen a relatively rare momentum indicator called Money Flow Index (MFI). The MFI was proposed by JWelles Wilder's in March 1989, which combined consideration of price and volume, and was equivalent to the RSI indicator of trading volume. Generally speaking, the increase in price increase and the decrease in price decrease are an inertial effect. When the stock price rises in a wave, the transaction volume must increase with it.

The Shanghai Composite Index from 2009 to now and the MFI that I calculate is shown below：
![Figure_1-3](https://user-images.githubusercontent.com/78809297/117569712-9babb980-b0f9-11eb-976a-147a73d5a04f.png)

Calculation method

1. Typical price (TP) = the arithmetic average of the highest price, lowest price and closing price of the day

2. Currency flow (MF) = typical price (TP) × N day trading volume

3. If the current day's MF>yesterday's MF, then the current day's MF value is regarded as positive currency flow (PMF)

4. If the MF of the day is less than the MF of the yesterday, the MF value of the day will be regarded as negative currency flow (NMF)

5. MFI=100-[100/(1+PMF/NMF)]

6. The parameter N is generally set to 14 days.

Application rule

1. Displaying overbought and oversold is the most basic function of the MFI indicator. When MFI>80, it is overbought. When it goes back and breaks below 80, it is a short-term selling opportunity.

2. When MFI<20, it is oversold. When it breaks through 20, it is a short-term buying opportunity.

3. When MFI>80 and divergence occurs, it is regarded as a sell signal.

4. When MFI<20 and a deviation occurs, it is regarded as a buy signal.

![Figure_1](https://user-images.githubusercontent.com/78809297/117570252-e5959f00-b0fb-11eb-9fea-e8e3d2dd88b7.png)
![Figure_1-1](https://user-images.githubusercontent.com/78809297/117569916-81261000-b0fa-11eb-923e-6bf5e6da6c79.png)
![Figure_1-2](https://user-images.githubusercontent.com/78809297/117570237-dc0c3700-b0fb-11eb-916d-2a009a3bbf07.png)
The following is a historical backtest of different parameter combinations and time intervals. It is not difficult to find from the figures below that the 20/80 oversold and overbought signals are not ideal. When the overbought value is changed to 90, results get obviously better. In addition, the MFI backtesting effect since 2016 is relatively good, especially when the overbought value is changed to 90, and the backtesting effect since 2000, 2005 or 2009 may not be as good as the market, reflecting the longer the time period, the MFI The worse the effect of the indicator, in fact, the MFI indicator is a technical indicator that provides short- and medium-term trading signals.


  - 2009 to now, overbought:80, oversold:20![Figure_1-4](https://user-images.githubusercontent.com/78809297/117570621-7c169000-b0fd-11eb-8d45-ba68dcb907ca.png)
  - 2009 to now, overbought:90, oversold:20![Figure_1-5](https://user-images.githubusercontent.com/78809297/117570639-95b7d780-b0fd-11eb-94ed-13c42727155c.png)
  - 2009 to now, overbought:95, oversold:20![Figure_1-6](https://user-images.githubusercontent.com/78809297/117570654-a8caa780-b0fd-11eb-8edf-290f59f72c89.png)
  - 2009 to now, overbought:95, oversold:30![Figure_1-7](https://user-images.githubusercontent.com/78809297/117570660-ae27f200-b0fd-11eb-9365-c3bda99dba1e.png)
  - 2009 to now, overbought:95, oversold:15![Figure_1-8](https://user-images.githubusercontent.com/78809297/117570687-dd3e6380-b0fd-11eb-9626-f4481755af66.png)
  - 2016 to now, overbought:90, oversold:20![Figure_1-9](https://user-images.githubusercontent.com/78809297/117570690-e0395400-b0fd-11eb-9d29-d9c874fc3a05.png)


  
