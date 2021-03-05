# An Analysis of Kickstarter Campaigns
Analysis of Kickstarter Crowdingfunding 
## Overview Of Project

In this module Luise estimates a budget of over $10.000 and is hesitant about jumping into her first fundraising campaign .Throughout this module by Performing analysis on Kickstarter data and use of excel functions like conditional formatting, pivot tables, and visualizations we analyse data to uncover trends and decide whether there are specific factors that make a project's campaign successful with a particular focus on theater.We found that in a short period of time Louise’s play almost reached her fundraising goal.Now, she wants to know how different campaigns fared in relation to their launch dates and their funding goals."


### Purpose

So by visualizing campaign outcomes based on their launch dates and their funding goals, we help her to compare how different campaigns  progressed in relation to their launch dates and funding goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
visualize campaign outcomes ("successful," "failed," and "canceled") based on launch date.
For analyse the data we need o extract the year from the “Date Created Conversion” column with this function: =YEAR(S2) then creat a pivot table with "theater" filter then visualize the relationship between outcomes and launch month by line chart.

![Theater_Outcomes_vs_Launch.png](https://github.com/tjavaheripour/Kickstarter-analysis/blob/main/Theater_Outcomes_vs_Launch.png)
### Analysis of Outcomes Based on Goals
visualize the percentage of successful, failed, and canceled plays based on the funding goal amount by line chart
with use of countif() function for example =COUNTIFS(Kickstarter!F:F,"successful",Kickstarter!D:D,"<1000",Kickstarter!R:R,"plays") for calculate number of success

![Outcomes_vs_Goals.png](https://github.com/tjavaheripour/Kickstarter-analysis/blob/main/Outcomes_vs_Goals.png)
### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?


## recommendations for Louise

