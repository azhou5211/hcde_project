# HCDE Project
This is the repository for HCDE project. It contains my source code for my analysis. The analytical methods and source code can be found [here](https://github.com/azhou5211/hcde_project/blob/main/A6/notebooks/A6.ipynb).

# Introduction
For my analysis, I will be looking at COVID-19 cases, mask mandates, unemployment rate, and uninsured health insurance rates for Dallas, Texas. Dallas is known to be a republican state and relatively against health insurance. It is common to find Dallas among the highest uninsured health insurance rates in the United States, and it has held the highest uninsured health insurance rates quite consistently over the past few years. “Hospital leaders have said that these uninsured patients put off preventable care until something is wrong and end up in the emergency room with costly uncompensated care for hospitals to deal with.” This is a serious issue on itself, however, with COVID-19 the issue may be much more severe.

It is quite common for people to get their health insurance from their employment. So, it should not be without a doubt that health insurance rates and employment rate are highly correlated values. One of the most popular topics during the period of COVID-19 was unemployment. As COVID-19 pandemic became a serious problem in the United States, the unemployment rate shot up, which likely made a lot of people lose their health insurance, and in turn these people did not seek their needed medical attention. So for my analysis, I would like to understand how COVID-19, mask mandates, unemployment rate, and uninsured health insurance rates impacted each other and ultimately how did these impact death rate?

### Hypothesis:
•	COVID-19 daily cases is positively correlated with unemployment.  
•	Mask mandates will slow down the spread of COVID-19.  
•	As COVID-19 cases increases, unemployment increases.  
•	As unemployment increases, uninsured health insurance rates increase.  
•	As uninsured health insurance rates increase, more people are likely to not to get their needed medical attention.  


# Data Sources
This repository used 6 data sources

US confirmed cases COVID-19 data - John Hopkins University.  
https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_confirmed_cases.csv

US confirmed death COVID-19 data - John Hopkins University.  
https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_deaths.csv

U.S. State and Territorial Public Mask Mandates From April 10, 2020 through August 15, 2021 by County by Day - CDC  
https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i

Mask-Wearing Survey Data - The New York Times (July 2 and July 14)  
https://github.com/nytimes/covid-19-data/tree/master/mask-use

Unemployment Rate - Bureau of Labor Statistics  
https://data.bls.gov/timeseries/LAUMT481910000000003?amp%253bdata_tool=XGtable&output_view=data&include_graphs=true

Uninsured Health Insurnace Rate - US Census  
https://www.census.gov/

### Licenses and Terms of Use:
John Hopkins University Covid Data:  
Found at the bottom of this [repository](https://github.com/CSSEGISandData/COVID-19).

CDC:  
https://www.cdc.gov/other/agencymaterials.html

The New York Times:  
[License](https://github.com/nytimes/covid-19-data/blob/master/LICENSE)

Bureau of Labor Statistics:  
https://www.bls.gov/cps/certifications-and-licenses.htm

US Census:  
https://www.census.gov/data/software/x13as/disclaimer.html

### Notes:
- Dallas, Texas's FIPS code is 48113.
- US confirmed cases and death COVID-19 data has date as their own individual columns. I melted the dates into two columns: date and value, where value is either confirmed cases or death depending on file. Filter the county and state to Dallas, Texas.
- Mask mandates needs to be filtered to Dallas, Texas by state and county.
- The survey data also needs to be filtered to the ZIP code 48113.
- All files that contain a ZIP code are not working well. Convert them into a string and pad with 0 in front for 5 digit values.
- Unemployment rate contains values in columns of data and year as a seperate column. This table also needs to be melted to include only two columns: date, unemployment rate.

# Analytical Methods
For my analysis, the main methodology methods will be using data visualization and linear regression. As any data science project, I started off with exploratory data analysis, which mainly consisted of data visualization. As all of my data is time series data, I will be making many time series plots with unemployment rate and uninsured health insurance rates to see if there are any correlations and interesting findings. I will start off by plotting COVID-19 case count and daily cases along with mask mandates in a time series to get a better understanding of COVID-19 and mask mandates data in Dallas, Texas. Since unemployment and uninsured health insurance data is annual and monthly, I plan on pulling data before the pandemic and compare how the pandemic impacted the values in comparison. I will plot unemployment rate and uninsured health insurance rate in a time series on its own to see were the rate usually hovers before the pandemic hits. I will also plot unemployment rates and uninsured rates that are close to the pandemic, so I can include the new COVID-19 cases and mask mandate data into the visualizations. To not confuse the reader of the plots, I decided to make two plots for unemployment rate and uninsured health insurance rates for better visibility and clarity. However, these plots are all just for exploratory data analysis and visualizations, they are not good tools for determining correlation between variables.

For my second part of analysis, I will be using statistical methods such as regression and ANOVA to determine correlation between variables and coefficients to determine how a variable is correlated with another. Regressions are very nice for when the dependent and independent variables are continuous. Regression will be useful for determining the correlation between unemployment rate and new COVID-19 cases. ANOVAs are very nice for when dependent variable is continuous but the independent variable is categorical. ANOVA is good to determine the correlation between mask mandates and the new COVID-19 cases. Due to very few data points overlapping for uninsured health insurance rates and COVID-19, correlations will have to be inferred from data visualizations and results from the other tests. I will also be comparing how Dallas, Texas compares in death rate compared to other counties in the United States. To ensure a fair comparison with other counties, I will be using death rate normalized over the population and multiplying by 100,000 for interpretability. The metric will turn out to be something like 100 deaths / 100,000 people.


All source code and analytical methods can be found in the [notebook](https://github.com/azhou5211/hcde_project/blob/main/A6/notebooks/A6.ipynb).

# Results
All findings and summary can be found in this [report](https://github.com/azhou5211/hcde_project/blob/main/A7/Final.pdf).
