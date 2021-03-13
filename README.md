# An Analysis of Kickstarter Campaigns
Analysis of Kickstarter Crowdingfunding 
## Overview Of Project

Louise estimated that she needed over $10.000 to fund her play and decided to do a fundraising campaign. She is worrisome to do her first fundraising campaign and hence requested help with some data analysis. With data analysis using pivot tables, conditional formatting and charts in Excel, we are going to help her decide on when and how in terms of dollar value to setup her fundraising campaign .


### Purpose

Using data analysis functions in Excel, we are going to help Louise determine 1) the best time of the year to launch theater campaign and 2) best dollar range to set fundraising goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
We need to visualize theater campaigns outcomes ("successful," "failed," and "canceled") based on launch dates by using pivot table and line chart. In order to do so, we need to first extract the year from the “Date Created Conversion” column from the kickstarter_challenge.xlsx using this function: =YEAR(). Next, we are going to insert a pivot table in Excel and filter it based on "Parent Category-theater" and "Years". Then fill the pivot tables field by putting "Date created conversion" as a row and eliminate (year and Quarters) from this field then put "outcomes" in columns and value fields. (Title of outcomes changes to count of outcomes in values field). Finally insert a line chart to visualize the relationship between outcomes and launch month.

![Theater_Outcomes_vs_Launch.png](https://github.com/tjavaheripour/Kickstarter-analysis/blob/main/Theater_Outcomes_vs_Launch.png)

The above line chart illustrates the relationship between outcome of campaigns and the launch month between 2009 and 2017. As shown in the graph May and June have the highest success rates among all months throughout the years.

We can also conclude from the chart that starting a campaign in fall and winter, especially in December would not have the best chance of being successful.

### Analysis of Outcomes Based on Goals
We require to know how outcomes were affected by the goals.  So we created a new sheet called "Outcomes Based on Goals" where we added range of goals starting with "Less than 1000" to “Greater than 50000”. We then used the “countifs()” function to find how many “play” projects were in each outcome corresponding to the goal range. We then need to calculate the success, failure and the canceled rate by dividing the number of successful, failed and canceled campaigns to the number of total projects respectively.

#####For example: =COUNTIFS(Kickstarter!F:F,"successful",Kickstarter!D:D,"<1000",Kickstarter!R:R,"plays") 

The above formula calculates the number of success campaigns reached their goals. 
Next, we populate the number of projects based on their goal ranges by using sum() function. Finally, we create a line chart called "Outcomes Based on Goal" to depict the relationship between the funding goal dollar ranges and the percentage of outcome for play subcategory.



![Outcomes_vs_Goals.png](https://github.com/tjavaheripour/Kickstarter-analysis/blob/main/Outcomes_vs_Goals.png)

Overall, looking at the line chart we see two dramatic drops in successful rate, one at $25,000 to $29,999 reaching almost 20% and another one at $45,000 to $49,999 hitting 0% success rate. On the other hand, the most successful projects had funding goals either less than $5,000 or between $35,000 to $44,999 reaching 70% success rate. The cancelation rate is zero through these range of goals.

### Challenges and Difficulties Encountered
-	Below are some challenges that I was encountered with Analysis of Outcomes Based on Launch Date:
1.	First off, I needed to extract the year from the “Date Created Conversion” column so I did so via using year() function.
2.	Another challenge I faced was determining what to put in each field of the pivot table. I had doubt about how to fill the columns, rows, and values of pivot table with appropriate fields because the pivot table was based on outcomes and Launch Date so I put "Date created conversion” as Rows and outcomes as Columns.
3.	I found some difficulties with how I could hide “live” as outcome because it was asked us to filter the column labels to show only "successful," "failed," and "canceled". However, I found I could unselect live label either from a line chart or put filter on column labels.
-	Challenges that I was faced with Analysis of Outcomes Based on Goals:
o	First I had no idea how I should use countif() and sum() functions for the generation of the Outcomes Based on Goals chart and it was challenging for me. To collect the outcome and goal data for the “plays” subcategory I had to use COUNTIFS() function. The COUNTIFS function counts the number of cells in a range that matches one supplied criteria. COUNTIFS(criteria_range1, criteria1, [criteria_range2, criteria2]…) so by some investigations I learned how to use it correctly then use Sum() function to populate the "Total Projects" column with the number of successful, failed, and canceled projects for each row

## Results

#### - What are two conclusions you can draw about the Outcomes based on Launch Date?
1.	As line chart displays, summer is the best time to start the theater’s campaign through the years, because it shows the highest number of successful projects that were launched during May to July.

2.	Actually starting a campaign on December has less chance of being successful because of low rate of success and significant drop in the total number of campaigns in this month.


#### - What can you conclude about the Outcomes based on Goals?
   I can draw from the chart that the chance of having successful fundraising campaign for play theater is greater when the range of dollar goal is lower and having the funding Goal of less than $5000 gives the higher chance of success. Clearly there is a downward trend of success when fundraising goals increase. The percentage of canceled theater campaigns is zero, so there is a zero flat line for that in the line chart.
#### -  What are some limitations of this dataset?
-	During analysis of data, I noticed that to reach accurate data, the distribution of campaigns number through months of year should be normal and not far distant from each other.
- Maybe some outcome results have been changed since 2017 especially due to effect of covid-19 in economic and people’s lives, so the same trends may not exist today.
- Another limitation of this dataset is we are basing our analysis on the dataset collected from the countries that may not necessarily apply to the city where Louise resides.
- The dataset provided is for fundraising campaigns for the theater category as general whereas this category includes three subcategories: Plays, Musical and Spaces.  Our findings based on the fundraising campaigns for theater may differ slightly for each subcategory, in this case Plays.

#### -  What are some other possible tables and/or graphs that we could create?
- 	Create another line chart with use of pivot table for "outcome by launch date" based on play as subcategory and calculate success percentage for each month and draw its chart accordingly.

-	To compare normal distribution of theater subcategories: “spaces”, “musical” and “plays” with theater category we could use box plots to find outliers. It could be helpful to analyze the "theater outcomes by launch date".

## recommendations for Louise
- Launch theater campaign in May and not around the end of year.
- "Fever" has more chance of success with funding goal of less than $5000.

