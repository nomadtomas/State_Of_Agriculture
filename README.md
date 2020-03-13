# State Of Agriculture
Agriculture has such broad economic, technological, and political implications.  President Lincoln not only established the Department of Agriculture in 1862, he referred to it as the “people’s department”.  It is precisely the people that represent this sector that this study will focus.  The scope of the analysis is focusing on five row-crops (corn, wheat, soybeans, cotton, and hay) given that they account for roughly 90 percent of harvest acreage in the US.  Along with this analysis I will be utilizing a linear regression and random forest models to try to predict end-of-year production for the row crop commodities.    

## Table of Contents

* [Study Approach](#approach)
* [Exploratory Data Aanalysis (EDA)](#eda)
* [Data Sources](#data-sources)
* [Machine Learning Models](#ml-models)
* [Technologies](#technologies)
    * [Database](#database)
    * [Python](#python)
    * [Visualization](#visualization)
* [Conclusion](#conclusion)

  
## Approach:
The approach will be to gather datasets regarding row crop planted, harvested, and production numbers.  The model will incorporate location at the county level for each state with production.  Through the linear model I will try to find which commodities are more correlated given the mutual exclusivity of farming (if you plan corn this year you did not plant cotton).  

## Data Sources:
The main data source I will be using will be from the National Agricultural Statistics Service.  https://www.nass.usda.gov/.   They have all data required for the project, though it will require multiple methods of incorporating such information.  

## EDA:
<p align="center">
  <img src="images/corn19.png">
</p>  

Predicting future planted acres by USDA-NASS was divided into multiple steps.  One was by summing all state level numbers to get the national total, the other was by summing all county numbers to get the national total.  Through EDA; however, it was found that those two methods do not equal each other, even though they should. 

<p align="center">
  <img src="images/national_ww_plt_ac.png">
</p> 

## ML-models:
Two models were used for this analysis.  Linear Regression and Random Forest Regressor.
Results:

Linear Model R2: 0.988<br>
RFR Model R2: 0.986

## Technologies
<p align="center">
  <img src="images/logos.png">
</p>

###### Database:
Data Storage: PostgresSQL<br>
Other: Docker 

###### Python:
Data Analysis: Python 3, Numpy, Pandas, Matplotlib, SqlAlchemy, Scikit-Learn<br>

## Conclusion: