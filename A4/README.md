# Visualizations

### Confirmed Cases by Date
<p align="center">
  <img src="https://github.com/azhou5211/hcde_project/blob/main/A4/visualizations/confirmed_cases_by_date.png" />
</p>

This plot displays the total confirmed cases per day in Dallas county of Texas. The plot has three different sections: "No Mask Mandate", "Yes Mask Mandate", "No Data on Mask Mandate".
The "No Mask Mandate" means there was no mask mandate during that day. The "Yes Mask Mandate" means there was mask mandate during that day. The "No Data on Mask Mandate" means there was no data during that time period, and I am unsure if there is a mask mandate or not.

This plot shows us that the mask mandates seem to be during the worst times of covid and there are no mask mandates during relatively low new cases. Since this plot shoes the total confirmed cases, the plot is a little hard to read.
I decide to plot new confirmed cases against date instead.

### New Cases by Date with 7 day delay
<p align="center">
  <img src="https://github.com/azhou5211/hcde_project/blob/main/A4/visualizations/new_cases_by_date_delay.png" />
</p>

This plot displays the new confirmed cases per day in Dallas county of Texas. The plot has three different sections: "No Mask Mandate in the past 7 days", "Yes Mask Mandate in the past 7 days", "No Data on Mask Mandate".
The "No Mask Mandate in the past 7 days" means there was no mask mandate laws in the past 7 days. The "Yes Mask Mandate" means there was a mask mandate law during the past 7 days. The "No Data on Mask Mandate" means there was no data during that time period, and I am unsure if there is a mask mandate or not.

After plotting this plot, I noticed there were a lot of 0 new cases and I decided to investigate further. After inspection, I noticed that the new case count is recorded after 2 day break, which is typically Saturday and Sunday. This also results in a huge number spike on Monday to make up for the 0 counts of the previous two days.
Therefore, be aware the very high spikes and low spikes are due to 2 day breaks every week.

With the 1 week delay on the plot, the plot looks very similar to as the previous plot. It's a very small shift of 7 days.
It looks like the mask mandate laws were put in palce during the worst parts of Covid (high number of daily new cases).
Perhaps, it would be worse without the mask mandate. We do see a spike in covid cases right before the mask mandate though, and that's probably why the mask mandate was put in place.
It does look like soon after the mask mandate, there is a slight drop in covid cases before it spikes up really high around December 2020 and Janurary 2021.
However, the spike drops very soon. I imagine that drop is due to the vaccinations given to the population around that time period.
I also choose not to comment on the dates after August 2021, as the mask mandates data set does not reach this far, and I'm not sure if there is a mask mandate there or not.
I can only comment on the huge spike that has appeared around August 2021 time period.

### New Cases by Date (Near Survey Time Period)
<p align="center">
  <img src="https://github.com/azhou5211/hcde_project/blob/main/A4/visualizations/new_cases_by_date_survey.png" />
</p>

New York Times conducted a survey on how often people wear masks around July 2nd - July 14 of 2020. Therefore, I decided to plot the time series of that time period with +- 2 weeks (June 18 - July 28 of 2020).

There seems to be a lot of jumping around near the end of July. That seems to be due to having no reports on one day, and then a makeup day with almost twice the value.
75% answered "Always" wear mask and 14% answered "Frequently" wear mask.
75% + 14% = 89% wear masks "Frequently" or more.
Considering that 89% wore masks around the July time period, the covid cases were around 1000 a day. It seems to be less before a huge spike coming August and September of 2020. Looking at this plot, it's very hard to say if there was any impact of masks and new covid cases.
However, looking at this plot, it's very difficult to say the impacts of people wearing masks and new Covid cases.

# Reflection

