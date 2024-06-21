## Title: Relationship Between Global Nickel Price and Global Copper Price.
----
<div align="center">
  <img height="300" width="100%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Copper-Nickel-1.jpg"  />
</div>

----

### 1. Introduction

Nickel and copper are highly important metals that play a pivotal role in construction, electronics and transportation industries. Owing to their function in sustaining the global economy, economists closely monitor the prices of copper and nickel for signs of health of the economy. To this end I take interest to apply econometric tools for time series data to investigate the relation between the prices of the two metals.

### 2. Data and Methodology

For this project, I use nickel and copper global price data obtained from FRED (Federal Reserve Economic Data) database. The data is seasonally unadjusted quartely data spanning from 1990 to 2023.

See table below for the summary statistics of the data:

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Summary_statistics.png"  />
</div>
<br>

#### 2.1 Data Visualisation

#### Prices

In this section, we visualise our data to observe any trends and/or anomalies.

Fig 2: Stack-up line graph of Copper and Nickel global prices

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Line_graph1.png"  />
</div>
<br>

Fig 3: Box-Plot Summarising the Price Distribution of the two Global Commodites

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Box_plot.png"  />
</div>
<br>

Fig 4: Scatter Plot Exploring the Correlation Between the Prices of Copper and Nicker

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Relationship_between_nickel_and_copper_prices.png"  />
</div>
<br>

We observe that the prices of the two commodities closely follow each other, with price of nickel being substantively above that of copper for every copper. Furthermore, we notice that nickel picked in 2007 to reach a peak of 47K per metric tonne only to dip in 2009. The same trend is almost observable for copper which also experienced  a dip in 2009, likely due to the global financial crisis.

#### Returns

In this section, instead of visualising commodity prices in a particular period, we shift our focus to observing the Quarterly price changes.

#### Returns Summary Statistics

We start by analysing the returns summary statistics. From the below table, we can notice that the returns of the two commodities from quarter to quarter are almost identical, with Copper and Nickel commodities experiencing an arithmetic mean quarterly return of 1.6% and 1.7% respectively. Furthermore, the returns are not as volatile at 12% and 15% standard deviation for copper and nickel respectively.

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Quarterly_Ret_Summary.png"  />
</div>
<br>

#### Charts

Fig 5: Stack-up line graph of Copper and Nickel Commodities Quarterly Returns

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Global_Metals_Quarterly_Ret.png"  />
</div>
<br>

Fig 6: Box-Plot Summarising the Returns Copper and Nickel

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Box_plot_Rett.png"  />
</div>
<br>

The boxplot reveals a depth of details on how the two commodities differ in turns of returns. While the mean return for both nickel and copper averages about 1.6% per quarter, the former reveals high volatility from the risk point of view, effectively dipping its Sharpe ratio. Thus, the two commodities may be suitable to individuals with a completely different risk profile.

### 3. Analysis and Modeling

#### 1. Informal checks

In time series analysis, it is advisable to perform informal checks on the data before carrying on with formal testing. Informal checks allow us to identify whether the data is stationary or non stationary. As a way of definition, stationary data is time series data that has constant mean and variance while non-stationary data is data that is upward trending or vice versa.

Method A: Plotting

    A1. Plotting Level Data

Per fig 2 ( brought down below), we can observe that our data tend to trend upwards together. Thus, indicating a lack of stationarity.

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Line_graph1.png"  />
</div>
<br>

    A2. Plotting First-Difference Data

Economic theory recommends transforming the data into its first difference to achieve stationarity. We do that in this section. When the data is first-differenced (see fig 7 below) we notice that it becomes stationary and therefore gives an indication that the data has unit roots.

•  By way of definition, a time series with a unit root is one where the influence of past values on the current value is so strong that the series is non-stationary.

•  If the equation of our time series looks like: Xt=ρXt−1+ϵt and if ρ=1, then the series has a unit root. This means today's value is just yesterday's value plus some random shock.

•  Because ρ=1,  the effect of past values does not diminish over time, making the series non-stationary and very unpredictable.

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/First-difference_data.png"  />
</div>
<br>

Fig 7: First-difference price data of Copper and Nickel

Method B: Autocorrelation Function (ACF)

ACF is another informal method of testing whether the data is stationary or not. As a rule of thumb, data is stationary if it shows fast decay i.e. autocorrelation values diminish quickly and become insignificant after a few lags.

    B1. Copper - Level Data ACF

Fig 8. Correlation Plot of First Level Copper Price Data Lagged to 21 Lags

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/ACF-Copper_LD.png"  />
</div>
<br>

As can be observed, our data is not stationary as the lags do not diminish rapidly to fall under the significance band. Thus, our level data has long memory.

    Copper - First Difference Data ACF

Fig 9. Correlation Plot of First Difference Copper Price Data Lagged to 21 Lags

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/ACF-Copper_FD.png"  />
</div>
<br>

We observe that the first differenced data is stationary. Thus, first differencing the data removes memory from it.


    B2: Nickel - Level Data ACF

Fig 10. Correlation Plot of First Level Nickel Price Data Lagged to 21 Lags

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/ACF-Nickel_LD.png"  />
</div>
<br>

As can be observed, our data is not stationary as the lags do not diminish rapidly to fall under the significance band. Thus, our level data has long memory.

    Nickel - First Difference Data ACF

Fig 12. Correlation Plot of First Level Nickel Price Data Lagged to 21 Lags

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/ACF-Nickel_FD.png"  />
</div>
<br>

We observe that the first differenced data is stationary. Thus, first differencing the data removes memory from it.

#### Formal Checks

Recall that we have so far concluded that our data contains unit roots. To proceed, we use formal methods to tests the unit roots. One popular such method is the:

##### i. Augmented Dickey Fuller Test (ADF)

The null hypothesis of the ADF test is that the time series has a unit root, indicating that it is non-stationary. The alternative hypothesis is that the time series data is stationary after accounting for unit roots.

ADF is a regression of the form: Δyt ​= α + βt + γyt−1 ​+ δ1​Δyt−1​ +...+ δp​Δyt−p​ + εt​.

Furthermore, like most time series regression models, the actual critical values to use for decision rules are specially calculated, and in this particular case of ADF, we use ones from Koop econometrics below:

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/ADF_critical_values.png"  />
</div>

##### 1. Copper

A. Drift

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Copper_drift.png"  />
</div>
<br>

B. Trend

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Copper_trend.png"  />
</div>
<br>

Conclusion: After running ADF test using the URCA library in R and using a confidence level of 5% and sample size of 100, we fail to reject the null hypothesis that our Copper time series data is non-stationary and has unit roots, agreeing with the informal checks. Furthermore, we can see that the data is non-stationary with a deterministic trend.

##### 2. Nickel

A. Drift

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Nickel_drift.png"  />
</div>
<br>

B. Trend

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Nickel_trend.png"  />
</div>
<br>

Conclusion: Similar to Copper, our nickel time series data is non-stationery and has a deterministic trend.
