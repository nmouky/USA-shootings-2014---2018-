1. Title: Gun Violence Dataset
	by N. Moukayed - MSc Data Science Goldsmiths

2. Sources: Gun Violence Archive (1718 M Street, N.W. PMB #126Washington, DC 20036-4504) 

* Please note that the data obtained does not provide all shooting incidents. Skewness of data and missing values have been flagged.

==== https://www.gunviolencearchive.org/  ====
     

3. Relevant Information: Five datasets have been extracted from the GVA site, these include shootings that have occured in the past 5 years (2014 - 2018). 

Five datasets have been downloaded as csv files, these have been merged into one dataframe using the pandas library. 
Other manipulations were required to optimise the dataset:
	--- Removed the operations column as that provided information that was not required (i.e. news articles, proof of shooting, etc.)
	--- Converted inputs in Incident Date column from string values into datetime. *This allowed to extract specific days, months and years where incidents have occured.
	--- Created two new columns and added to dataframe: Month and Year - specifying when and where each incident had occurred. 

 
4. Statistics:
	Following notations are related to subsets of dataframe have been divided to provide clear and concise information.
	--- t_inc: Total incidents, sums up total number of killed and injured provided in dataset.
	--- t_kill: Total killed
	--- t_inj: Total injured
	--- t_yr: Total killed and injured in each year spanning from 2014 to 2018. 
	--- t_mth: Total killed and injured in each month. (Aggregated data 2014 - 2018, within 5 years)
	--- t_stt: Total number of killed & injured in each state. Total number of states is 46. (Aggregated data 2014 - 2018, within 5 years)
	--- max_kill: Maximum number of killed in one incident.
	--- min_kill: Minimum number of killed in one incident.

*** Approximately 48% of all incidents had 0 killings

*** Please note that there are 4 states missing in this data. Those are Hawaii, Idaho, New Hampshire and Wyoming.

5. Number of Instances: 1655

6. Number of Attributes: 6

7. Attribute Information:
   1. Incident Date
   2. State
   3. City or County
   4. Address
   5. # Killed
   6. # Injured
 

8. Missing Attribute Values: Operations (Removed due to limited accessibility and irrelevance to dataset)/

9. Summary:

The data obtained allows us to view where incidents have occured most in the United States.
From the following data we can evaluate that the 5 most 'incident-prone' states are (Killed,Injured): 
California (201,761), Illinois (111,668), Florida (196,568), Texas (196,409) and Nevada (72,480).
The deadliest year was 2016 with 451 deaths (1,989 total affected). 
However, 2017 had seen more individuals get injured thus having a larger amount of individuals being impacted (2,240 total affected).
Whereas in the past 5 years the most deadliest months were June (230,822), July (184,882) and October (203,925).
Maximum number of killed in one incident: Las Vegas, Nevada (59 Killed, 441 Injured)
Minimum number of killed in one incident. (789 incidents where no killings have been recorded)

This dataset merely shows the number of lives affected by these incidents, some pertain to certain areas due to population density etc.
This dataset does not take that into account

10. Areas to improve and work on for 2nd part of assignment:

Integrating other datasets to improve quality of captured data (i.e. finding a correlation, etc). 
The following are some datasets that can be integrated -
	a) Population of cities and states
	b) Weather pattern across different parts of the United States.
	c) Type of shootings (i.e. Justified police shootings, self-inflicted, hunting accidents, etc.)
	d) GDP and other economic status of states/cities.
	e) Narcotic legalisation in different states.
	f) Political party affiliation within a state.
	g) Number of police officers within a state/city.

* To learn: Integrating different types of datasets and creating intricate plots such as heatmaps through seaborn etc.
* To research further into: Data on other 4 states and merging with current dataset.
