# An Analysis of Kickstarter Campaigns
Analysis of Kickstarter Crowdingfunding 
## Overview Of Project

Luise estimated that she needed over $10.000 to kick off her play and decided to do a fundraising campaign to fund it.  She is worrisome to do her first fundraising campaing and hence requested help with some data analysis. Throughout this project by performing analysis on Kickstarter data and use of excel functions like conditional formatting and pivot tables, and of visualizations we analyse data to uncover trends. We also determine whether there are specific factors that make a project's campaign with a particular focus on theater successful. We dicovered that in a short period of time Louise’s play reached her fundraising goal. Now, she wants to know how different campaigns fared in relation to their launch dates and their funding goals."


### Purpose

So by visualizing campaign outcomes based on their launch dates and their funding goals, we help her to compare how different campaigns  progressed in relation to their launch dates and funding goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
We visualize campaign outcomes ("successful," "failed," and "canceled") based on launch date by using piviot table and line chart.
First we need to extract the year from the “Date Created Conversion” column from the kickstarter_challenge.xlsx with this function: =YEAR( ).  Next step, insert a pivot table in Excel and filter it based on "Parent Category-theater" and "Years". Then fill the pivot tables field by putting "Date created conversion" as a row and eliminate (year and Quarters) from this field then put "outcomes" in columns and value fields. (Tilte of outcome changed to count of outcomes in values field).Finally insert a lince chart to visualize the relationship between outcomes and launch month.

![Theater_Outcomes_vs_Launch.png](https://github.com/tjavaheripour/Kickstarter-analysis/blob/main/Theater_Outcomes_vs_Launch.png)

The above line chart indicate to the relationship between outcome of campaign and the launch month during 2009 to 2017.Due to the result as we can see the most theater campaigns that were launched in May and June had a higher numbers of success than other months. We can also draw from the chart that starting a campaign on Fall especially on December and Winter would not have the best chance of being successful.
### Analysis of Outcomes Based on Goals
We want to know how outcomes were effected by the Goal, So we created a new sheet called "Outcomes Based on Goals" where we put ranges of goal starting with "Less than 1000" to Greater than 50000 . We used the countifs() function to find out how many projects were in each funding range to finally divide it to the total number of projects to calculate the percentage of successful, failed, and canceled projects by filtering on the Kickstarter "outcome" column,  and on the "Subcategory" column using "plays" as the criteria. For example =COUNTIFS(Kickstarter!F:F,"successful",Kickstarter!D:D,"<1000",Kickstarter!R:R,"plays") for calculate number of success then repeated this with failed and canceled projects as well,After that we populate the number of projects based on their goal range by using sum() function. Finally we created a line chart called "Outcomes Based on Goal" to illustrates the relationship between the funding goal amount ranges and the percentage of outcome for play subcategory .


![Outcomes_vs_Goals.png](https://github.com/tjavaheripour/Kickstarter-analysis/blob/main/Outcomes_vs_Goals.png)

Overall, As we notice the trend of increase and decrease of successful and failed outcomes based on goal are contract each other. By looking at the line chart we can see two dramatic drops in successful rate between $20,000 to $34,999 and $40,0000 and $49,999 funding goals. However, The most successful projects had funding goals less than $5,000 and between $35,000 to $44,999 around 70% success rate. The cancelation rate is zero through these range of goals.
### Challenges and Difficulties Encountered
- Some challenges that I was encountered with Analysis of Outcomes Based on Launch Date :
1. First of all I should extract the year from the “Date Created Conversion” column. So I solved it with year() function
2. Another possible challenge was determining where each dataset should placed in the pivot table. I had doubt about how should I fill the columns, rows, and value of pivot table with appropriate fields.Because this pivot table was based on outcome and Launch Date so I put "Date created conversion as" Rows and outcomes as Columns.
3. I found some difficulties with how could I hide live as outcome because it was asked us to filter the column labels to show only "successful," "failed," and "canceled." However, I found I could unselect live lable either from a line chart or put filter on column lables. 

- challenges that I was faced with Analysis of Outcomes Based on Goals:

  - First I had no idea how I should use countif() and sum() functions for the generation of the Outcomes Based on Goals chart and it was challenging for me. To collect the outcome and goal data for the “plays” subcategory I had to use COUNTIFS() function,The COUNTIFS function counts the number of cells in a range that match one supplied criteria. COUNTIFS(criteria_range1, criteria1, [criteria_range2, criteria2]…) so by searching on google I learnt how to use it correctly then use Sum() function to populate the "Total Projects" column with the number of successful, failed, and canceled projects for each row
## Results

#### - What are two conclusions you can draw about the Outcomes based on Launch Date?
1.	As line chart display, summer is the best time to start the theater’s campaign through the years, because it shows the highest number of successful projects that were launched during May to July.

2.	Actually Fall specially on October might be the worse launch time for theater’s campaign due to the low range of successful and high number of failed outcomes. In addition, starting a campaign on December has less chance to be successful because of low rate of success and significant drop in the total number of campaigns in this month.

#### - What can you conclude about the Outcomes based on Goals?
   I can draw from the chart that the chance of having successful play campaigns is greater when the amounts of goal is lower and having the funding Goal ranges less than $5000 give the higher percentage of success by increasing trend . In addition, the percentage of canceled theater campaigns is zero, so there is a zero flat line for that in the line chart.
#### -  What are some limitations of this dataset?
-	During analysis of data, I notice to reach accurate data, the distribution of campaigns number through months of year should be normal and not far distant from each other.
-	Maybe some outcomes results had been changed through the years of 2017 to 2021 especially due to effect of covid-19 in economic and people’s life, so we shouldn’t expect same trends that perform during 2009-2017.
-	Another limitation of these data is that these kickstar data is categorize by country not especifically consider state or city, so we couldn't expect same results of outcome that happen for example in Us to the whole states. 
-	In analysis of “outcomes by launch date” with focus on theater’s campaigns that include 3 subcategories that are “spaces”, “musical” and “plays” which the majority of these campaign related to “play” subcategory so we couldn’t say with confident these analyze has the same impact on two others subcategory as well.

#### -  What are some other possible tables and/or graphs that we could create?
-create another line chart for "outcome by launch date" based on play as subcategory

## recommendations for Louise

