# HCDE Project
This is the repository for HCDE project. It contains my source code for my analysis. The analytical methods and source code can be found [here](https://github.com/azhou5211/hcde_project/blob/main/A6/notebooks/A6.ipynb).


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

Notes:
- Dallas, Texas's FIPS code is 48113.
- US confirmed cases and death COVID-19 data has date as their own individual columns. I melted the dates into two columns: date and value, where value is either confirmed cases or death depending on file. Filter the county and state to Dallas, Texas.
- Mask mandates needs to be filtered to Dallas, Texas by state and county.
- The survey data also needs to be filtered to the ZIP code 48113.
- All files that contain a ZIP code are not working well. Convert them into a string and pad with 0 in front for 5 digit values.
- Unemployment rate contains values in columns of data and year as a seperate column. This table also needs to be melted to include only two columns: date, unemployment rate.

All analytical methods can be found in the [notebook](https://github.com/azhou5211/hcde_project/blob/main/A6/notebooks/A6.ipynb).
