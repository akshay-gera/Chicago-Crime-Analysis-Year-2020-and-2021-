# Let's Get You Aware About the Crimes Happening in Chicago (for year 2020 and 2021)
Analysis of open source data on crimes reported in the city of Chicago by Chicago Police Department

# Data Source:

https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2


# Background
This dataset reflects reported incidents of crime (with the exception of murders) that occurred in the City of Chicago within the aforementioned period.
Data is extracted from the Chicago Police Department's CLEAR (Citizen Law Enforcement Analysis and Reporting) system.
These crimes may be based upon preliminary information supplied to the Police Department by the reporting parties that have not been verified. 

# Key Observations and Conclusions

## Overall Crime Scenario for both Years
![image](https://user-images.githubusercontent.com/98545133/190919480-3554ea73-1d11-4534-8f34-74797c2ecad4.png)

### Observation
The distribution of crimes looks almost identical for the both years. However, on a closer look we do witness that Crimes leading to arrest has gone down in 2021 while other crimes show a slight increase in 2021.

## What types of crimes are happening in the city?
![image](https://user-images.githubusercontent.com/98545133/190919515-d5ed3af3-c8c9-46a2-a0b0-37ccbfa60560.png)

### Observation
After the most frequent crime type Theft, Battery is the second most occuring crime type in Chicago. It has almost the same percentage as Battery.

Battery, Theft and Criminal Damage together account for 50% of all the crimes in the city. While, ritualism the least occuring crime type

## Is there any change in the crime type composition over the year?
![image](https://user-images.githubusercontent.com/98545133/190919564-5a95d610-3870-4f5f-b59b-e57283f03132.png)

### Observation
The horizontal barchart splits the percentage in years 2020 and 2021 which makes us easier to visualize the change in the percentage levels of each crime type.

We observe a general trend of simultaneous increase and reduction and in crime across all the crime categories.

## Is there any particular day when the crimes happen?
![image](https://user-images.githubusercontent.com/98545133/190919614-e15473a6-b47d-4965-9a99-976702e8622f.png)

### Observation
There is a uniform distribution of values across all days for both the years which shows that there are crimes happening on every day of the week while Friday leads in both the years which has highest count among all days in both years

## Any particular time when crimes happen?
![image](https://user-images.githubusercontent.com/98545133/190919935-b307d571-48cc-4d3c-97a3-bfc5d9248679.png)

### Observation
We observe that the hour 0000, i.e between 12am-1am is the peak time for crimes and it increases in 2021 from 6% to 7% of total crimes. From 1am the crimes start to decrease rapidly till 6 am from where they start to rise again. The second peak we are witnessing is between 12pm to 1pm

## How are crimes spread accross the month?
![image](https://user-images.githubusercontent.com/98545133/190919672-f80c0a8c-9858-4c94-a57d-4ff7094c925f.png)

### Observation
There is a general average of about 17,000 crimes each month of the both years for the City of Chicago. While some months are peaking and some are lower on some months, but there seems to be a uniform distribution of crime rate accross different months for both years. The pattern is different for both years. Aug and Jan peaked for 2020 while for 2021 Sep and Oct had peak crimes


## What is the situation of Domestic Crimes in the city? Do they lead to arrest? Does it happen often every month?
![image](https://user-images.githubusercontent.com/98545133/190919775-0b541dfc-3e5d-4a92-87a6-b7a4e16b0936.png)

### Observation
We observe that highest proportion of crimes is in non-domestic violence which doesn't lead to arrest. Leading months in this category are October and July. In Domestic violence not leading to arrest the frequency is near about evenly distributed accross all months . In domestic violence leading to arrest, also is spread out evenly amongst months

## What are the common locations of the crime?
![image](https://user-images.githubusercontent.com/98545133/190919812-acecc728-1969-4f52-9efc-01bb817450c8.png)

### Observation
Street, apartment and residence are the most common occuring crime location in the city of chicago accounting for over 50% of all the crimes in the city. There is a huge gap between these three locations and all other crime locations of the city which shows that the City needs to prioritze these locations more to bring down crime rate in the city

## How is the crime distributed accross various districts? 
![image](https://user-images.githubusercontent.com/98545133/190919896-31079801-2b09-412d-a874-e6d40c1a526d.png)

### Observation
We observe that District 8 contains highest count of crime in non-domestic non-arrest worthy crimes. While for crimes leading to arrest or more violent in nature and which are non-domestic, District 11 has the highest number. We also do observe that district 31 is the one which doesn't contain any crime count in all four sub-categories which could be a data collection error or data reporting bias.

__________________________________


# Predictive Model Building
We were intersted in quantifying what variable are affecting the outcome of crimes leading to arrest. For this problem we are treating Arrest(Y/N) variable as our target variable which informs us whether a person was arrested or not for the crime.
We chose logistic regression as our choice of algorithm for this modelling exercise since this is a classification problem.

## Following data preparation steps were performed before building the model:

-Dimensionality reduction of the dataset by manually excluding variables which seemed irrelevant

-Reducing cardinality of categorical variables by aggregating values 

-Coverting categorical variables to binary encoded to run ML model on them 

-Performing Logistic Regression on target Variable 'Arrest' to try to extract what factors are leading to arrest of people

## Outcome:

### Performance Metrics
 precision    recall  f1-score   support

           0       0.95      0.72      0.82    107979
           1       0.31      0.76      0.44     17973

    accuracy                           0.73    125952
   macro avg       0.63      0.74      0.63    125952
weighted avg       0.86      0.73      0.77    125952

### Comment
We observe here that our model gives us 73% Accuracy in predicting whether a crime leads to arrest or not based on the input variables. The model could somewhat be reliable as the accuracy is way over 50% which could be more like random guessing. But there is still a lot of scope of improvement to make the model predict more accurately

### Importance of Features and Their influence on the Outcome
![image](https://user-images.githubusercontent.com/98545133/190921765-4b4e26aa-e198-4614-a230-201dff4e863b.png)


### Observations:
Features such as Unlawful possession of handgun and Retail Theft are highest positive scores leading to arrests. In months, Jan and Feb are most prone to crimes leading to arrests. In terms of location, sidewalk has more propensity for arrests. We couldn't find a particular type of crime that would lead to arrest.






