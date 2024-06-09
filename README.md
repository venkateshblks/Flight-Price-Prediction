# Predict-Fare-of-Airlines-Tickets-using-Machine-Learning

# <a href="https://colab.research.google.com/github/venkateshblks/Predict-Fare-of-Airlines-Tickets-using-Machine-Learning/blob/main/flight_prediction.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>



## 1.. deal with missing values

## 2..Data Pre-process & extract Derived attributes from "Date_of_Journey"

## 3..clean Dep_Time & Arrival_Time & then extract Derived attributes

## 4..analyse when will most of the flights take-off..


## 5..Pre-process Duration Feature & extract meaningful features from it

**Apply pre-processing on duration column**

## 6.. Lets Analyse whether Duration impacts Price or not ?

**convert duration into total minutes duration**

**Non stops flights take less duration while their fare is also low, then as the stop increases,
duration also increases and price also increases(in most of the cases)**

## 7.. on which route Jet Airways is extremely used?

## 8.. Performing Airline vs Price Analysis

**From graph we can see that Jet Airways Business have the highest Price.
 Apart from the first Airline almost all are having similar median**

## 9.. Applying one-hot Encoding on data(Feature Encoding)

## 10..Perform target guided encoding on Data(Feature Encoding)

Now on 2 features , Airline & Destination , we can apply on-hot as there is no such order
but total_stops is my ordinal data , it makes no sense if we apply on-hot on top of this..
similarly if we have any feature which have more categories , it is not good to apply one-hot as it will create
curse of dimensionality issue , which leads to usage of more resources of your pc..

So we can think for appplying mean Encoding or better techniques like Target Guided Ordinal Encoding !

***now lets perform Target Guided Mean encoding on 'Destination'***

## 11.. Perform Label(Manual) Encoding on Data(Feature Encoding)

**Remove Un-necessary features**


**lets drop Date_of_Journey as well as we have already extracted "Journey_hour" , "journey_month" , journey_day"**

**Additional_Info contains almost 80% no_info , so we can drop this column**

**lets drop Duration_total_mins as we have already extracted "Duration_hours" & "Duration_mins"**

**Lets drop "Source" feature as well as we have already perform feature encoding on this Feature**

**lets drop Journey_year as well , as it has constant values throughtout dataframe which is 2019..**

## 12.. Lets Perform outlier detection !

## 13..feature selection

**Mutual information between two random variables is a non-negative
value, which measures the dependency between the variables.
If It is equal to zero it means two random variables are independent, and higher
values mean higher dependency**

## 14..Build ML model

## 15..automate ml pipeline

## 16..hypertune ml mode