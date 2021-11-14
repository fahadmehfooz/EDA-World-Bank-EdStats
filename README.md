#  EDA Worldbank EdStats: Project Overview

## Problem Statement:
* We are provided with a dataset named World Bank EdStats that contains 3665 indicators describing education access ( primary, secondary and tertiary), GDP, literacy rate, population growth and technical aptitude (PISA, TIMSS, PIRLS).
* The idea of the project is to analyze the data, mark the variation of indicators across the globe and group the countries according to their similarities and differences.
* 
## About The Data:
 
 * EdStatsData  (886931 rows and  69 columns): This is our primary file. This dataset is the one which contains the scores for all countries for various indicators over the years starting from 1970. It also contains the projections for multiple indicators for future decades. The dataset has peculiar features. A majority of values are either missing or null. Given below is a graph displaying the distribution of data for every year.

* EdStatsSeries (3666 rows and  20 columns) – EdStatsSeries carries all information about the indicators which are used by the World Bank  to monitor progress of economies. There are approximately 3700 indicators used to  determine which countries have improved in terms of education and other parameters. The dataset contains the description of the indicators, their units of measurements and their sources.

* EdStatsCountry (242 rows and 31 columns)- EdStats Country carries important information of all the countries that we will encounter in the dataset. Indicators such as latest population census, region and income group of a particular country are provided.


## Data Preparation:
* After exploring the dataset, we tried to form a key approach to process the dataset to find the underlying patterns across all countries for all the indicators. 
* Performed all these operations using: pandas, matplotlib, seaborn and plotly.

* Our main goal was to:-
1) Remove the futile data.
2) Make a befitting dataset.
3) Identify Patterns.
4) Develop Hypothesis. 

## Null Value Treatment:
* As we had a large dataset so in order to abridge it, we formulated a way to remove extraneous data.
* We removed the future projection data , as it does not hold real information and only contains future predictions so we have discarded data after 2015 till 2100

* Nan Values: We dropped all the rows which have null values in every year column. This resulted  in a remarkable reduction (almost 60%). The final dataset had around 356K records.

## EDA 

### For BRIC countries:
* Population Analysis:
1) As depicted by the graph, the population trends for INDIA and CHINA are the similar. Same can be said for the other 3 countries.
2) The populations for Russia,  SA, Brazil stayed relatively stable.

* PRE-PRIMARY GROSS Enrollment Ratio Analysis:
1) INDIA performs poorly when it comes to enrollment of children in pre-primary classrooms
2) The enrollment % for India is merely 10% towards the end of 2015 whereas it is roughly 80% for other BRICS members

* TERTIARY GROSS Enrollment Ratio Analysis:
1)From this graph we can see that Russia has always had a greater percentage of its young population in the universities and colleges(around 80% of youth aged between 16 and 21 in 2015).
2) The number of young adults in colleges has been rising for almost every BRICS country throughout the last 4 decades

* Mortality Rate Analysis:
1) As countries become more educated, the mortality rates drop, and the rate of drop is higher in countries where more focus was laid on tertiary education for previous generations.

### For India, China and USA: Similar eda was performed.


## Conclusion:

- From the BRICS countries, we can conclude that :
* The populations of India and China showed growth over the years, with India’s growth rate overtaking China’s after 2000s.
* India’s pre-primary and tertiary enrollment percentage is pretty low when compared to other BRICS countries, but increasing from 1995.
* Impact of year-wise expenditure by government on tertiary education shows the increase in tertiary enrollment percentage
* The mortality rate has dropped for every country, the highest drop being observed in India where more focus was laid on education over the years
* Immigration in the USA from 1990-2000 increased the population growth rate for that 10-year time period
* The countries having the highest dropout rate affected the GNI per capita for those countries

## Challenges Faced:

* It was very challenging to completely understand the data and to comprehend the relevance of each CSV file.
* As the percentage of missing data was huge, it took a lot of effort to decide on the final data to keep for analysis.
* Filtering out the best indicators from 3700 indicators to keep for analysis.
* Deciding on the set of countries to work based on economy and geography.
