---
layout: post
title:  "US COVID-19 Data Analysis"
date:   2020-8-11 00:00:00 -0400
categories: jekyll update
---

# US COVID-19 Data Analysis

Project analysis of the New York Times COVID-19 data. The story that we get from this data is difficult to take. It shows that COVID-19 is more deadly depending on where you are in the US and isolation lowers the chances of infection and death. It’s a tough story to wrap our heads around because infection and death should be dependent features.

[The project notebook can be viewed on GitHub.](https://github.com/KalenWillits/Covid-19/blob/master/Covid-19.ipynb)
### The data is puzzling.

The Covid-19 pandemic has become a point of high controversy in the US. Opinions have been muddled by different practices of classification and over saturation of data. [Some resources claim the entire response to Covid-19 is a political hoax.](https://www.washingtontimes.com/news/2020/apr/28/coronavirus-hype-biggest-political-hoax-in-history/) [Fox News suggests that the deaths reported in the US are inflated.](https://www.foxnews.com/politics/birx-says-government-is-classifying-all-deaths-of-patients-with-coronavirus-as-covid-19-deaths-regardless-of-cause) However, the entire world seems to have gone into lockdown. Here we will attempt to gain insight on the integrity of the [COVID-19 data provided graciously by the New York Times.](https://github.com/nytimes/covid-19-data) We will also reference the [2019 US Census data](https://www.census.gov/search-results.html?q=population+data+by+state+2020&page=1&stateGeo=none&searchtype=web&cssp=SERP&_charset_=UTF-8) for perspective.
2019 US Census data by state ranked by population.

![](/figures/covid/perspective.png)
>The COVID-19 Infections Graph begins at the yellow line. COVID-19 deaths graph are shown at the red line. These graphs are shown by the yellow and red arrows to explicitly show that the following graphs are not measured by the same x-axis. The red line does not appear on the populations graph.

We can see by the vertical yellow line that we begin to measure infections at a relatively low number when compared to the entire population. Be aware that the vertical yellow line is denoted by the state with the highest amount of infections in the US, which we will be able to see clearly in the plot below. According to our data, the average amount of infections by population is 1.3%. Another point that must be made is we are not measuring time. The number of people that have been recorded as infected are not the same as the number of people that are currently infectious. Although these numbers are many, this data could support that the [CDC preventative measures](https://covid.cdc.gov/covid-data-tracker/?CDC_AA_refVal=https%3A%2F%2Fwww.cdc.gov%2Fcoronavirus%2F2019-ncov%2Fcases-updates%2Fcounty-map.html#county-map) are working or the virus is not being properly measured. Perhaps a mix of both.

>![](/figures/covid/state_infections.png)
 COVID-19 confirmed and probable infections in the US by state from the New York Times data set.

The infections plot carries a similar distribution to its parent populations plot. At a glance, we could say that the data that shows a higher population contributes to a higher number of people infected, until we get to Washington state. Washington appears to have less COVID-19 activity when compared to other states with similar populations. If we check the [states with the most aggressive counter measures to COVID-19](https://www.usnews.com/news/best-states/articles/2020-03-17/10-states-with-the-most-aggressive-response-to-coronavirus), Washington state ranks in 5th place. Some aggressive measures from Washington state include a [four step data-driven plan](https://www.governor.wa.gov/sites/default/files/SafeStartPhasedReopening.pdf) with excellent feature definitions. Unfortunately, our New York Times data set does not show evidence that these aggressive measures have helped reduce the amount of COVID-19 activity when compared to the other 9 states on the list.


>![](/figures/covid/state_deaths.png)
COVID-19 confirmed and probable deaths in the US by state from the New York Times data set.

When viewing the deaths chart, we should expect the amount of deaths reported to be strongly correlated with the amount of infections, however this is clearly not the case. Alaska reports deaths per infections as 0.5% and Connecticut has a reported death rate of 8.83%. Either something is causing COVID-19 deaths to have a wide range of survival rates from state to state or the reporting is incorrect, there are arguments for both sides. The data says that the average death rate in the US is nearly 3%, this is especially troubling when compared to [Germany’s metric of 0.4%](https://www.cnn.com/2020/03/24/opinions/germany-low-death-rate-for-coronavirus-sepkowitz/index.html). The argument in this article is that Germany has tested more of the population and found more infections that are asymptomatic resulting in a higher infection rate and lower death rate. [Fox News](https://www.foxnews.com/politics/birx-says-government-is-classifying-all-deaths-of-patients-with-coronavirus-as-covid-19-deaths-regardless-of-cause) reports that people who die with COVID-19 are being reported as a victim of COVID-19 regardless of other factors contributing to death. Without an international standard for logging these deaths the above comparison carries little weight.

To dive deeper into the data, Below we will observe a table of the infection rate and death rate for each state as well as some summary statistics.

>![](/figures/covid/table.png)
Table of New York Times data set, COVID-19 infection and death ratios. Where infections = infections / population and deaths = deaths / infections. Ordered by descending population size.

The most interesting thing about this table is the range of deaths vs the range of infections. If we assume the behavior of the COVID-19 virus is a constant, this range should provide little variation. Instead, the data shows that there is a range of 8.29% death rate depending on which state you are in. This could be evidence that hospitals in states that are showing above a 5% death rate are unable to provide the same treatment as other states, or the data is not getting reported in the same manner.

So what states are getting the best COVID-19 metrics?

Both Alaska and Hawaii have infection rates and death rates lower than 1%. This could be an indicator that isolation is the best preventative measure to COVID-19.

The story that we get from this data is difficult to take. It shows that COVID-19 is more deadly depending on where you are in the US and isolation lowers the chances of infection and death. It’s a tough story to wrap our heads around because infection and death should be dependent features. The range brings up many questions worth investigating.

Sources

- [Kaggle Covid-19 Dataset - Scientific community call to action](https://www.kaggle.com/fireballbyedimyrnmom/us-counties-covid-19-dataset?select=us-counties.csv)

- [New York Times COVID-19 data](https://github.com/nytimes/covid-19-data)


- [Coronavirus myths: Don't believe these fake reports about the deadly virus](https://www.cnet.com/health/false-information-about-coronavirus-here-are-the-top-rumors-spreading-about-it/)

- [2019 Census Data](https://www.census.gov/search-results.html?q=population+data+by+state+2020&page=1&stateGeo=none&searchtype=web&cssp=SERP&_charset_=UTF-8)


- [Cases & Deaths by County](https://www.cdc.gov/coronavirus/2019-ncov/cases-updates/county-map.html)

- [Coronavirus hype biggest political hoax in history](https://www.washingtontimes.com/news/2020/apr/28/coronavirus-hype-biggest-political-hoax-in-history/)

- [Fox News shares that the deaths reported in the US are inflated](https://www.foxnews.com/politics/birx-says-government-is-classifying-all-deaths-of-patients-with-coronavirus-as-covid-19-deaths-regardless-of-cause)

- [government is classifying all deaths of patients with coronavirus as 'COVID-19' deaths, regardless of cause](https://www.foxnews.com/politics/birx-says-government-is-classifying-all-deaths-of-patients-with-coronavirus-as-covid-19-deaths-regardless-of-cause)

- [Safe Start Washington](https://www.governor.wa.gov/sites/default/files/SafeStartPhasedReopening.pdf)

- [10 States with the Most Aggressive Response to Covid](https://www.usnews.com/news/best-states/articles/2020-03-17/10-states-with-the-most-aggressive-response-to-coronavirus)

- [Why is Covid-19 death rate so low in Germany?](https://www.cnn.com/2020/03/24/opinions/germany-low-death-rate-for-coronavirus-sepkowitz/index.html)

- [Our ongoing list of how countries are reopening, and which ones remain under lockdown](https://www.businessinsider.com/countries-on-lockdown-coronavirus-italy-2020-3?op=1#el-salvador-began-to-reopen-its-economy-on-june-16-35)

- [CDC's 'best estimate' is 40 percent COVID-19 infections are asymptomatic](https://www.foxnews.com/science/cdc-best-estimate-40-percent-covid-19-infections-asymptomatic)

- [Population density in the U.S. by federal states including the District of Columbia in 2019](https://www.statista.com/statistics/183588/population-density-in-the-federal-states-of-the-us/)
