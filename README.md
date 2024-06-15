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
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/line_graph.png"  />
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
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Box_plot_Ret.png"  />
</div>
<br>
