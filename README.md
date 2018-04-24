
***Advanced Business Analytics – Final Project Description***
=============================================================

*Team Members*
------------
  + Ankita Guha
  + Kara Marsh

*Project Title*
-------------
Analyzing EPA data to determine patterns in pollution

*Type of Final Project*
---------------------
Project Type I - Analysis of EPA data

*Executive Summary of the Proposed Project*
-----------------------------------------
We have analyzed a large data set from the EPA. This data set contains 
information on the location, time, type, substance, and results of individual 
sample testing. We have cleaned the data and performed exploratory data 
analysis in R to find some general trends within subsets of the data. Based on
this exploratory analysis, we picked some subset of the data on which to 
perform linear and non-linear analysis to find models and relationships that 
may be predictive of future samples. Because this data set covers sampling 
from 1987 to 2017, we have tested our models using the data within the set. 

*Data Needs and Sources*
-----------------------
We have used the following dataset from Kaggle:
Source: https://www.kaggle.com/epa/air-quality
Link of the original Data File Used to Clean and Prepare the Data Frames: https://www.kaggle.com/epa/air-quality/data 

*Important Variables Used & Brief Description*
-----------------------------------
+ latitude:The monitoring site’s angular distance north of the equator measured in decimal degrees.
+ longitude:The monitoring site’s angular distance east of the prime meridian measured in decimal degrees.
+ parameter_name: Air Constituents which are Pollutants or Non-Pollutants 
+ metric_used: The total time for which the parameter_name was measured.
+ method_name: A short description of the processes, equipment, and protocols used in gathering and measuring the sample.
+ year: The year the annual summary data represents.
+ arithmetic_mean: The average (arithmetic mean) value for the year.
+ arithmetic_standard_dev: The standard deviation about the mean of the values for the year.
+ address: The approximate street address of the monitoring site.
+ state_name: The name of the state where the monitoring site is located.
+ county_name: The name of the county where the monitoring site is located.
+ norm_mean: Calculated column of Normalized arithmetic mean value.

*Challenges Encountered*
-----------------------
1) Large data set - made it slow to import tables as data frames
2) Real-life data set - messy - we had to make decisions about NA values and 
whether they could be ignored; had to make decisions on which type of result 
information we were going to consider in our analysis
3) The data was not as continuous as it orginally appeared to be. We had to 
consider the best way to filter the data and make executive decisions on what
data sets could be combined without reducing the integrity of the results. 
4) The blank method_name has a great deal of influence over the dataset.
5) Mostly the parameter_name Ozone as the chief Pollutant has been found to be captured under the blank method_name.
6) Normalizing one subset of data frame improved not only the Model Fit but also produced an exact match of the train and test data prediction in case of building some of the Non Linear Regression Model. 
7) While performing the Logistic Regression Model Fit, we found that Ozone that has been identified as the main Pollutant in previous models of Linear Regression Model Fit mainly due to the variable  method_name or the unnkown test, which was blank in the original dataset that we got from Kaggle. Thus Ozone seemed to be out of the perview of our data, when we were not considering the blank method_name. We had a tough time to figure out on how to replace the blank string data values with 'NA' and then replace these 'NAs' with 'Missing Data From Kaggle'. That's because in the initial Data Cleaning & Preparation Stage these blank data values were not captured as NA. And we were on the verge of losing a significant chunk of Pollutant data that have been captured by this specific test or the method_name which was initially blank from the original Kaggle data.  


*Personal Learning Objectives*
----------------------------
1) What did we learn?

+ We learned how to deal with Millions of data
+ Data cleaning and data manipulation for ease of analysis
+ Treat blank space as character string, in case those blank spaces are not showing up as NA
+ The library plyr should be installed before dplyr

2) What else did we learn?

+ Getting perfect Model Fit was mainly due to the fact that we used some of our Response Variables in our Models for predicting the Predictors.
+ Plot maps from the latitude and the longitude data

3) What third thing did we learn?

+ For the Map to be more explicit in nature, one can increase or decrease the **zoom** argument to acheieve the desired level of Map visual. We have decided our zoom to be at a desired level, for the purpose of providing a suitable aerial view of all the 4 States that we are looking into. 
+ Stack Overflow helped us a lot! 
+ Another interesting fact point that we learned while using ggmap() is that after a certain point of time, query used to fetch map data might not run, if a certain quota of fetching map API data from google is met. We came across an error something like: **geocode failed with status OVER_QUERY_LIMIT, location = "michigan"**, that means that we have run our code many times and hence the IP address has met it's limit to use and fetch API data from Google. 
**Source: https://stackoverflow.com/questions/tagged/google-geocoding-api?page=4&sort=unanswered**


**Explanation of the Project stages and files**
=============================================

*Necessary Packages to install:*

boot 	
coefplot 	
dplyr 	
e1071 	
ggmap 	
ggplot2 	
gpclib 	
mapdata 	
maps 	
maptools
plyr 	
RColorBrewer
reshape2
scales 	
sp 	
stringr 	
VIM 	
viridis

# Data Cleaning
Associated RMD files: 

+ Data Cleaning and Data Preparation Phase 1
+ Data Cleaning and Data Preparation Phase 2


# Exploratory Data Analysis
Associated RMD files: 

+ EDA1
+ EDA2
+ TriCountyEDA


# Data Modeling
Associated RMD files: 

+ NonLinearModelsFor1987_2017_4States
+ PredictiveRegressionModelingForMI&US

# Future Project Scope
It would be nice to have a Forecasting of the Pollutants Data across the time lines or performing a time series Prediction of the Pollutant Data across this Dataset.

# N.B
Due to the enormous data quantity it would be necessary to follow the steps in downloading and running the data files as explicitly mentioned in the following steps below:

+ Step 1: Download the Data File from Kaggle (https://www.kaggle.com/epa/air-quality/data)
+ Step 2: Then Run the RMD File named: Data Cleaning and Data Preparation Phase 1
+ Step 3: Next Run the RMD File named: Data Cleaning and Data Preparation Phase 2
+ Step 4: i)  Run the RMD File named: EDA1
          ii) Run the RMD File named: EDA2
          iii) Run the RMD File named: TriCountyEDA
+ Step 5: Run the NonLinearModelsFor1987_2017_4States
+ Step 6: Run the PredictiveRegressionModelingForMI&US

Once the original data file is downloaded from Kaggle. The individual CSV data files will be created while running the above mentioned RMD Files step bt step. These individual CSV data files so created after running the RMD Files, are used in our subsequent analysis that are projected in our RMD Files as well.
