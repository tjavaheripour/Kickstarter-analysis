# An Analysis of Kickstarter Campaigns
Analysis of Kickstarter Crowdingfunding 
## Overview Of Project

In this module Luise estimates a budget of over $10.000 and is hesitant about jumping into her first fundraising campaign .Throughout this module by Performing analysis on Kickstarter data and use of excel functions like conditional formatting, pivot tables, and visualizations we analyse data to uncover trends and decide whether there are specific factors that make a project's campaign successful with a particular focus on theater.We found that in a short period of time Louise’s play almost reached her fundraising goal.Now, she wants to know how different campaigns fared in relation to their launch dates and their funding goals."


### Purpose

So by visualizing campaign outcomes based on their launch dates and their funding goals, we help her to compare how different campaigns  progressed in relation to their launch dates and funding goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
visualize campaign outcomes ("successful," "failed," and "canceled") based on launch date.
For analyse the data we need o extract the year from the “Date Created Conversion” column with this function: =YEAR( ) then creat a pivot table with "theater" filter then visualize the relationship between outcomes and launch month by line chart.

![Theater_Outcomes_vs_Launch.png](https://github.com/tjavaheripour/Kickstarter-analysis/blob/main/Theater_Outcomes_vs_Launch.png)

the above line chart indicate to the relationship between outcome of campaign and the launch month during 2009 to 2017.Due to the result as we can see the most theater campaigns that were launched in May and June had a higher numbers of success than other months. We can also draw from the chart that starting a campaign on Fall especially on December and Winter would not have the best chance of being successful.
### Analysis of Outcomes Based on Goals
The line graph illustrates the percentage of successful, failed, and canceled plays based on the funding goal amount ,
We use countif() function to count how many successful, failed, and canceled projects were created with goals within the range list, for example =COUNTIFS(Kickstarter!F:F,"successful",Kickstarter!D:D,"<1000",Kickstarter!R:R,"plays") for calculate number of success then repeated this with failed and canceled campaigns as well.

![Outcomes_vs_Goals.png](https://github.com/tjavaheripour/Kickstarter-analysis/blob/main/Outcomes_vs_Goals.png)

Overall, As we notice the trend of increase and decrease of successful and failed outcomes based on goal are contract each other. By looking at the line chart we can see two dramatic drops in successful rate between $20,000 to $34,999 and $40,0000 and $49,999 funding goals. However, The most successful projects had funding goals less than $5,000 and between $35,000 to $44,999 around 70% success rate. The cancelation rate is zero through these range of goals.
### Challenges and Difficulties Encountered
some challenges that I was encountered with Outcomes Based on Launch Date :
1. first of all I should extract the year from the “Date Created Conversion” column. So I solved it with year() function
2. I had doubt about how should I fill the columns, rows, and value of pivot table  with appropriate fields.Because this pivot table was based on outcome and Launch Date so I put "Date created conversion as" Rows and outcomes as Columns.
3. I found some difficulties with how could I hide live label because it ask us to filter the column labels to show only "successful," "failed," and "canceled." However, I found I could unselect live lable either from a line chart or put filter on column lables. 
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?


## recommendations for Louise

