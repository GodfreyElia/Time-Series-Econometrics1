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

a. Fig 2: Stack-up line graph of Copper and Nickel global prices

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/line_graph.png"  />
</div>
<br>

b. Fig 3: Box-Plot Summarising the Price Distribution of the two Global Commodites

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Box_plot.png"  />
</div>
<br>

c. Fig 4: Scatter_Plot Exploring the Correlation Between the Prices of Copper and Nicker

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Relationship_between_nickel_and_copper_prices.png"  />
</div>
<br>

We observe that the prices of the two commodities closely follow each other, with price of nickel being substantively above that of copper for every copper. Furthermore, we notice that nickel picked in 2007 to reach a peak of 47K per metric tonne only to dip in 2009. The same trend is almost observable for copper which also experienced  a dip in 2009, likely due to the global financial crisis.

#### Returns

In this section, instead of visualising commodity prices in a particular period, we shift our focus to observing the Quarterly price changes.

<div align="Left">
  <img height="60%" width="75%" src="https://github.com/GodfreyElia/Time-Series-Econometrics1/blob/main/Diagrams/Relationship_between_nickel_and_copper_prices.png"  />
</div>
<br>

