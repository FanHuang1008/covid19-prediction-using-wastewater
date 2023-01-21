# covid19-prediction-using-wastewater
Individual contribution in the group project of Modern Data Analytics (B-KUL-G0Z39B) at KU Leuven

Data source
Wastewater: https://github.com/biobotanalytics/covid19-wastewater-data/blob/master/wastewater_by_county.csv
Daily Cases: https://github.com/nytimes/covid-19-data/blob/master/us-counties.csv

When people are infected with COVID-19, even if they don’t have any symptom, the virus can still spread with their feces as well as saliva, and eventually enter the wastewater system. This allows wastewater surveillance to serve as an early warning that COVID-19 is going to spread in the community. When the virus concentration in the wastewater starts to rise, the health department can take early action to prevent the spread of COVID-19. 

In this project, we used the virus concentration in wastewater to predict daily increased cases in the USA by fitting a simple linear model to demonstrate the importance of wastewater surveillance.

An obvious time lag between daily increased cases and virus concentration rolling average can be observed from the time series plot of whole USA. Instead of using the concentration rolling average as a variable to predict the time series of increased cases, we shifted the wastewater data N (N = 1, 2,...., 15) days backward and fitted N linear models with daily increased cases as the target. Lowest MSE occurred when N = 11, so we used this model to predict daily cases and plotted the results. 

From the final figure, we can see that except for the start of COVID-19 and the period when a lot of people were infected, a linear model with shifted wastewater data as the only variable can roughly predict daily increased cases.

