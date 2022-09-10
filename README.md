# Chicago-Crime-Analysis-Year-2020-and-2021-
Analysis of open source data on crimes reported in the city of Chicago by Chicago Police Department

# Data Source:
The data has been sourced from Google Cloud where the dataset is publicy available for open use. 
Data Source: https://console.cloud.google.com/marketplace/details/city-of-chicago-public-data/chicago-crime?filter=solution-type:dataset

Data origination: https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2

For further use, API is also available to extract data from City of Chicago website: https://dev.socrata.com/foundry/data.cityofchicago.org/ijzp-q8t2

# Key Note:
The analysis is based on the data reported between January 1, 2020, to November 23rd, 2021. The idea was to make a two year analysis and at that point of time, December 2021 data was not available.

# Background
This dataset reflects reported incidents of crime (with the exception of murders) that occurred in the City of Chicago within the aforementioned period.
Data is extracted from the Chicago Police Department's CLEAR (Citizen Law Enforcement Analysis and Reporting) system.
These crimes may be based upon preliminary information supplied to the Police Department by the reporting parties that have not been verified. 

# Analytical Workflow

## Exploratory Data Analysis
Checking structure of data and datatypes
Completeness of data 
Feature engineering
Exploring variable distribution 
Data visualization to see distributions

Observations: 
-Battery, Theft, and Criminal Damage account for > 50% of all crimes. 
-Serious offence crimes, i.e., crimes leading arrests are peaking in the month of January each year.
-Street, Apartments and Residence account for around 60% of the crime locations and there is huge gap between the distributions of crime over rest of the locations.
-District 31 has very low frequency of crime. If this is not a result of a data collection error, this district could be a ideal or low crime District in Chicago.

## Model Building
Dimensionality reduction of the dataset by manually excluding variables which seemed irrelevant
Reducing cardinality of categorical variables by aggregating values 
Coverting categorical variables to binary encoded to run ML model on them 
Performing Logistic Regression on target Variable 'Arrest' to try to extract what factors are leading to arrest of people

Observations:
Features such as Unlawful possession of handgun and Retail Theft are highest positive scores leading to arrests. In months, Jan and Feb are most prone to crimes leading to arrests. In terms of location, sidewalk has more propensity for arrests. We couldn't find a particular type of crime that would lead to arrest.






