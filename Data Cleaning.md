# In this section I will discuss how I cleaned my data.
So, first I want to explore the missing data and how to deal with it.

## Let's start with DF_1: CHILD FATALITIES TREND
First a brief description of this dataframe,
The columns that are worth explaining are the following:
- child_fatalities_reported: These are fatalties reported and processed by the CPS
- child_fatalities_reported_agency: These are fatalties reported and processed by other welfare.
  Now let's run an EDA on my DF, 
Let's start with a histogram
![image](https://github.com/many1026/child_victims_analysis/assets/73008381/8cca94fd-6014-4a65-949c-acecba488b5e)
I choose to delete the state NATIONAL where it contains the aggregate sum of all states.
Ill continue my wiork on tabbleau
