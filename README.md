# Energy-Burden-Project
Explanatory and predictive model of energy burden at the US county level

## 1. Data set

The data set was obtained from the National Renewable Energy Laboratory (NREL) Website and is titled **“Equitable Energy Investment Prioritization Data Set”** (2021). Its goal is to provide metrics around renewable energy deployment potential and energy justice. The former consists of estimates with a high degree of uncertainty, therefore we determined to focus on metrics around energy justice, which includes the energy burden.

The following are variables relevant to our project. In the process of exploratory data analysis and feature selection during model fitting many variables were modified and/or removed. For the final set of variables, see the Detailed Report.

1.	State, categorical
2.	County population, continuous,  2013 - 2017
3.	Reference Vehicle Counts, continuous, 2018: battery electric vehicle, hybrid electric gasoline vehicle, plug-in hybrid electric vehicle, internal combustion engine vehicle
4.	Energy Burden variables, continuous, 2018: multiple variables, see discussion in the report.
5.	Unemployment Rate, continuous, 2020
6.	Percent of work force employed in mining, quarrying or oil and gas, continuous, 2015 – 2019
7.	Rural-urban continuum code, categorical, 2013: codes 1 through 9 – represent urban and rural counties with a certain population, the higher the code the more rural the county is.
8.	Farming-dependent county code, categorical, 2015: yes/no
9.	Population loss county code, categorical, 2015: yes/no
10.	Persistent Poverty County Code, categorical, 2015: yes/no
11.	Minority Indicator, continuous,  2013 – 2017: this is a "score" variable
12.	Low Income Indicator, continuous, 2013 – 2017: this is a "score" variable
13.	Less than High School Indicator, continuous, 2013 – 2017: this is a "score" variable
14.	Cancer Indicator (environment hazard), continuous, 2013 – 2017: this is a "score" variable


## 2. Research Question

This project attempts to find associations between certain demographic variables, such as county population, percent minority, unemployment rate, vehicle counts and the average energy burden. Relevant population is all of United States – this is represented by data at the county level. Originally, the explanatory model was supposed to be linear, however significant bias was detected when checking linear model assumptions - this was due to manually approximating energy burden at the county level. Therefore, it was determined to switch to the logistic regression model, which classifies energy burden as either "high" (greater than four percent) or "low" (less than or equal to four percent). See Detailed Report for more information.

## 3. File navigation

* **Detailed Report and Findings**: detailed discussion of the project steps. Starting with exploratory data analysis, necessary variable transformations to model fitting and evaluation (checking for multicollinearity, model assumptions, outlier detection) and policy recommendations.

* **Energy Burden Presentation**: slide deck focusing on high level EDA, which includes screenshots of Tableau visualizations, interpretation of logistic regression and policy recommendations

* **R markdown code**: R code with all of the project steps, comments included

* **energy_burden_final_project_ml**: python code with a KNN model, which predicts energy burden at the county level. Includes train/test split, search for the optimal number of neighbors based on the test set area under the curve.

