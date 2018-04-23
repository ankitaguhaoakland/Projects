# Projects
# THINGS TO DO BEFORE TURNING IT IN
1) Move the cleaned2_AQ.csv into the data folder, and update references to it in whichever documents use it
2) Remove Jacob's name from all docs (Should we email Prof. Isken to explain what happened, or is that on Jacob because he was the one that dropped out?)
3) 
4) 
5) Go back through and knit all of the RMD files into HTMLs
6) Finishing update the paragraphs below
7) Develop a presentation
8) Record our presentation
9) Edit the presentation
10) delete this list of things to do 
11) zip the file and get ready to upload

====================================================


#Advanced Business Analytics – Final Project Description
========================================================

*Team Members*
------------
Ankita Guha
Kara Marsh

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

*Challenges Encountered*
-----------------------
1) Large data set - made it slow to import tables as data frames
2) Real-life data set - messy - we had to make decisions about NA values and 
whether they could be ignored; had to make decisions on which type of result 
information we were going to consider in our analysis
3) The data was not as continuous as it orginally appeared to be. We had to 
consider the best way to filter the data and make executive decisions on what
data sets could be combined without reducing the integrity of the results. 
4) 

*Personal Learning Objectives*
----------------------------
1) what did we learn?
2) what else did we learn?
3) What third thing did we learn?


# Explanation of the Project stages and files
=============================================

*Necessary Packages to install:*
dplyr
ggplot2
ggmap
gpclib
mapdata
maps
maptools
plyr
sp
stringr
viridis

# Data Cleaning
Associated RMD files: 
Data Cleaning and Data Preparation Phase 1
Data Cleaning and Data Preparation Phase 2


# Exploratory Data Analysis
Associated RMD files: 
EDA 1
EDA 2
Project EDA
TriCountyEDA

# Data Modeling
Associated RMD files: 
NonLinearModelsFor1987_2017_4States
PredictiveRegressionModelingForMI&US


