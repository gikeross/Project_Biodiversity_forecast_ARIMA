# Project_Biodiversity_forecast_ARIMA: studying factors that affect the trend

## Summary
By definition Biodiversity is the variety of plant and animal life in the world or in a particular habitat, a high level of which is usually considered to be important and desirable.
This project aims to understand some macro-environmental factors that impacted the biodiversity and predict in which year the index will reach the critical value of 50%. 

To do so, we are going to analyse various datasets related to environment. It is important to highlight that many factors have contributed in the past to impact the level of biodiversity, some of this factors are directly caused by Human beahviour and other are non-controlable. 
The primary objective is to gain insights into trends, patterns, and contributions of what impact this index and collect data regading territory, global temperature, macro-analysis of resources used that cannot explain the overall situation but are highly correlated with the topic and are extremely close to justify some trend. Said so, countless factors have contributed to reach this point.  

## Data Sources
 
In order to choose the right metrics to take into consideration, I before studied the world trend regading environment and i found out that global warming, territory usage and shift plus resources exploitation with CO2 prodution are consuming not just the wolrd but it's also taking out territory of wild animal.

The main datasets have been extracted from ourworldindata.org | gbif.org | biodiversity.europa.eu

## List of main files

1. **ARIMA prediction (`ARIMA_forecast_world.xlsx`):**
   - Dataset that joins the real index biodiversty data for the period 2001 to 2021 and plots the prediction obtained in our analysis from 2022 to 2200.

2. **Analysis of the world territory (`LAND_USED.xlsx`):**
   - Dataset reports the analysis of the area for each country of the world from the period 2010 to 2021 by distinguish if it is 'LAND AREA', 'FOREST' etc. in square kilometers.

3. **Biodiversity index (`aggregate_exstintion_measure.xlsx`):**
   - Dataset plotting the index of biodiversity for each country, For the analysis has been used the wolrld index.
   **Biodiversity index_average (`Biodiversity index (`avg_cou_biod_2021_RLI.xlsx`):**
   - output of te analysis where is take into account the avarage from the upper and lower index value

4. **global temperature datase (`annual_temp_and-co2-emissions-per-country.xlsx`):**
   - Data report the temperature variation from 1970 until 2022 per country.

5. **alternative prediction (`bounded_predictions_2100.xlsx`):**
   - Dataset reporting the result from a linear regression made from the main biodiversity index data.
   
6. **Quantity of earth consumed (`eart_consumption_country.xlsx`):**
   - This databased report the number of earth intended as resources provider, each country need to mantain its economy as it is
  
7. **Measure the wildlife population (`global-living-planet-index.xlsx`):**
   - This databased measures the average decline in monitored wildlife populations. The index value measures the change in abundance in 31,821 populations across 5,230 species relative       to the year 1970
     
## Data analysis steps:

## Data Cleaning and Exploration
- understand the data and trying to make it usable for the analysis - applyed the mean to get the avarage of the index and pivotting to get country and year in column

## prepare ARIMA - maximization 
- I prepared the split between train and test data to perform control over the result and I evaluate the error using RMSE
- Second, evaluate the model by maximizing the p_values, d_values, q_values with leat error resulting an RMSE of 0.001

## Comparing result with data
- plot the result to see the trend of my prediction and my datas - the two lines were practically equal confirming the prediction was reliable
- studying the residual to check if my datas were well fitted as well as see if the density respected the pattern of a normal distribution around 0 of mean

## applying ARIMA 
- applyng the model from the start year of 2022 and checking in which year we reached the 0.5

## alternative analysis with Linear Regression
- the Linear regression has been applied for each country forecasting a sample year of 2100 choosen arbitrarly - as a resilt of this, this analysis was more agression and showed the final output of index = 0.44 against the 0.54 of the Arima analysis


## CONCLUSION
This analysis was mainly focused to give a general view of the causes that impact our biodiversity and trying to raise people awarness. The main goal was to predict using ARIMA method when the biodiversity index would hit the 0.5 and was forcast in between the year 2132 & 2133.

# This project has a visualization on Tableau Public on the following link:
 https://public.tableau.com/app/profile/giacomo.rossini/viz/PROJECT2_17025013200780/FINAL_dashboard?publish=yes
