README for Assignment 2 W12G1


Overview
=========
Data Preprocessing: data_cleaning.ipynb
Data Analysis: data_analysis.ipynb
Data Modeling: data_modeling.ipynb


Data Preprocessing
=================
Mainly preprocessing all required files, mainly including house-by-suburb csv file and LGA offences excel file.
Deal with missing values and normalizes the text expression.
Merge different files and encode offence informaations.
Classify offences into categories in 3 different way and average offence count and house price and calculate change percentage.

Data Analysis
=============
The code is mainly used for Data Analysis through Exploratory Data Analysis and correlation analysis.


Data Modeling
=============
The code is mainly used for model building, 
using two linear regression models and a decision tree model.


Different Datastes
==========

Data without missing values
---------------------------------------
cleaned_median_house_prices.csv
(same as table 03 in house-by-suburb.csv)
Columns:
* Locality: The name of the suburb or locality where the house price data was recorded.
* 2013 to 2023: The median house price in the respective year (from 2013 to 2023).
* Change Percentage 13-23: The percentage change in house prices over the 10-year period from 2013 to 2023.

cleaned_offences.csv
(same as table 03 in LGA offences.xlsx)
Columns:
* Year: The calendar year when the offence was recorded.
* Year Ending: The date marking the end of the reporting period.
* Local Government Area: The LGA where the offence occurred.
* Postcode: The postal code of the area where the offence was reported.
* Suburb/Town Name: The specific suburb or town where the offence occurred.
* Offence Division: The broader category of the offence (e.g., Property Damage, Drug Offences).
* Offence Subdivision: A narrower category within the offence division (e.g., Criminal Damage, Possession of Drugs).
* Offence Subgroup: A detailed classification of the offence type (e.g., Graffiti, Drug Trafficking).
* Offence Count: The total number of reported offences for this type in the suburb/town.

cleaned_offences_by_police_region.csv
(same as table 01 in LGA offences.xlsx)
Columns:
* Year: The calendar year when the offences were recorded.
* Year Ending: The date marking the end of the reporting period (usually the fiscal year).
* Police Region: The police jurisdiction overseeing the reported crimes.
* Local Government Area: The LGA where the offences occurred.
* Offence Count: The total number of reported offences within the LGA.
* Rate per 100,000 Population: The standardized crime rate per 100,000 residents in the LGA.

Data merged for two file
-----------------------------------
matched_house_prices_with_offences.csv
Columns:
* Locality: The name of the suburb or locality where the house price data was recorded.
* 2013 to 2023: The median house price in the respective year (from 2013 to 2023).
* Change Percentage 13-23: The percentage change in house prices over the 10-year period from 2013 to 2023.
* 2014 to 2023 offence count:The total number of offence price in the respective year(from 2014 to 2023)

matched_offences_with_house_price.csv
(similar as cleaned_offences.csv)
Columns:
* Year: The calendar year when the offence was recorded.
* Year Ending: The date marking the end of the reporting period.
* Local Government Area: The LGA where the offence occurred.
* Postcode: The postal code of the area where the offence was reported.
* Suburb/Town Name: The specific suburb or town where the offence occurred.
* Offence Division: The broader category of the offence (e.g., Property Damage, Drug Offences).
* Offence Subdivision: A narrower category within the offence division (e.g., Criminal Damage, Possession of Drugs).
* Offence Subgroup: A detailed classification of the offence type (e.g., Graffiti, Drug Trafficking).
* Offence Count: The total number of reported offences for this type in the suburb/town.
* House Price:  The median house price in the suburb in that year.

Classify offences into categories in 3 different way
-----------------------------------------------------------------
offence_and_housePrice_by_suburb.csv
Columns:
* Suburb/Town Name: The name of the suburb where the house price and offence data was recorded.
* Year: The calendar year when the house price and offence was recorded.
* House Price:  The median house price in the suburb in that year.
* Offence Count: The total number of reported offences in the suburb.

offence_and_housePrice_by_LGA.csv
Columns:
* Local Government Area: The LGA where the house price and offence data was recorded.
* Year: The calendar year when the house price and offence was recorded.
* House Price:  The median house price in the LGA in that year.
* Offence Count: The total number of reported offences in the LGA.

offence_and_housePrice_by_police_region.csv
Columns:
* Police Region: The Police Region where the house price and offence data was recorded.
* Year: The calendar year when the house price and offence was recorded.
* House Price:  The median house price in the Police Region in that year.
* Offence Count: The total number of reported offences in the Police Region.

Calculate change percentage for suburb in 10 years
-----------------------------------------------------------------------
change_percentages.csv
Columns:
* Suburb/Town Name: The name of the suburb where the house price and offence data was recorded.
* House Price:  The house price rate in the suburb in 10 years.
* Offence Count: The rate of reported offences in the suburb in 10 years.

average offences
-------------------------
average_suburb.csv
Columns:
* Suburb/Town Name: The name of the suburb where the house price and offence data was recorded.
* House Price:  The average house price in the suburb in 10 years.
* Offence Count: The average number of reported offences in the suburb in 10 years.

average_LGA.csv
Columns:
* Local Government Area: The name of the LGA where the house price and offence data was recorded.
* House Price:  The average house price in the LGA in 10 years.
* Offence Count: The average number of reported offences in the LGA in 10 years.

average_police_region.csv
Columns:
* Police Region: The name of the Police Region where the house price and offence data was recorded.
* House Price:  The average house price in the Police Region in 10 years.
* Offence Count: The average number of reported offences in the Police Region in 10 years.



Encode matched_offences_with_house_price.csv
--------------------------------------------------------------------
encode_offences_with_house_price.csv
Columns:
* Year: Encode calendar year when the offence was recorded.
* Year Ending: Encode date marking the end of the reporting period.
* Local Government Area: Encode LGA where the offence occurred.
* Postcode: Encode postal code of the area where the offence was reported.
* Suburb/Town Name: Encode suburb or town where the offence occurred.
* Offence Division: Encode broader category of the offence (e.g., Property Damage, Drug Offences).
* Offence Subdivision: Encode narrower category within the offence division (e.g., Criminal Damage, Possession of Drugs).
* Offence Subgroup: Encode detailed classification of the offence type (e.g., Graffiti, Drug Trafficking).
* Offence Count: The total number of reported offences for this type in the suburb/town.
* House Price:  The median house price in the suburb in that year.



