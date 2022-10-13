# Crowdfunding Analysis of International Plays


## Overview of Project
We were tasked with helping Louis, an up-and-coming playwright, analyze crowdfunding data so that she can effectively identify specific factors that make a project's crowdfunding campaign successful.  She hopes to use our analysis to start a campaign to raise funds for her own play *Fever*.  

### Purpose
Our analysis will help Louis better understand crowdfunding campaigns from start to finish, so that she can set up her campaign for success and meet the $10,000 budget estimate that she has set.  Through the use of various analytical methods in Microsoft Excel, we manipulated existing crowdfunding data to better lead Louis in the many choices she must make by illustrating patterns from past successful, failed, and canceled plays. 


## Analysis and Challenges
The data analysis was conducted using pivot tables, descriptive statistics, and line graphs to manipulate the data in a way that effectively shows patterns and trends to help Louis with her fundraising choices.  A breakdown of that data and the methods of analyzation are below:

### Analysis of Outcomes Based on Launch Date
A helpful bit of information for Louis to know while making the decision to start a crowdfunding campaign is: when are the most successful times of the year to launch her campaign?  To determine this, we created a pivot table that compared the number of successful, failed, and canceled fundraising campaigns for different plays over the time period of 2009 to 2017.  The number of outcomes were broken out by month, and the data was filtered so that the only parent category shown was theater functions. The resulting pivot table is shown below:

![Outcomes_vs_Launch_Pivot.png](https://github.com/hillmanj1995/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Launch_Pivot.png)

The data from that pivot table was then used to create a line chart to better illustrate the outcomes per month.  That line chart is shown below:

![Theater_Outcomes_vs_Launch.png](https://github.com/hillmanj1995/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
Another piece of information that will help Louis with her decision making is to know how successful different goal amounts are.  To create this analysis, we created a table that listed ranges of fundraising goals, in increments of $5,000, and counted the number of successful, failed, and canceled plays, then provided the percentages of those plays against the total of projects for that goal range (percentage successful, percentage failed, percentage canceled).  That table is shown below:

![Outcomes vs. Goals Table.png](https://github.com/hillmanj1995/kickstarter-analysis/blob/main/Resources/Outcomes%20vs.%20Goals%20Table.png)

The command used to calculate the number of successful, failed, and canceled fundraising campaigns for plays for each goal range was the COUNTIF function.  An example of the code used for that function is shown below, calculating the number of successful plays for a goal range of $1,000 to $4,999:

`=COUNTIFS(Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,">=1,000",Kickstarter!$R:$R,"plays",Kickstarter!$D:$D,"<=4,999")`

The table that was populated by these commands was then used to create a line chart showing the trends of the various outcomes based on the goals.  This chart is shown below:

![Outcomes vs. Goals.png](https://github.com/hillmanj1995/kickstarter-analysis/blob/main/Resources/Outcomes%20vs.%20Goals.png)

### Challenges and Difficulties Encountered
The largest challenge faced by the analyst was user error.  For instance, during the analysis the data from the pledge column got copied into the goals column, which then resulted in incorrect tables and charts for the Outcomes based on Goals section.  It took a long period of time and multiple iterations of graphs for the analyst to derive that the goal data was wrong.  Other challenges arose by incorrectly inputting commands or taking the wrong data ranges for the charts.


## Results

### Conclusions on the Outcomes Based on Launch Date Analysis
The analysis of the Theater Outcomes based on Launch Dates illustrated that the most successful time of the year to launch starts in May and then decreases through the summer to about August.  August through April saw lower numbers of sucessful launches, averaging around 61 successful shows per month, versus the May though August period, which averaged around 93 successful plays per month.

### Conclusions of the Outcomes Based on Goals Analysis
When we look at the results from our analysis of the Outcomes based on Goals, it showed that a high percentage of successful campaigns had a fundraising goal between $0 and $19,999.  Goals of over $20,000 had a higher likelihood of failing than succeeding.  This trend shows that Louis's estimated budget of $10,000 has around a 55% success rate of being met. 

### Dataset Limitations
Some of the limitations of this data are that they do not account for people's preferences in play genre.  An analysis on successful fundraising campaigns vs genre could be helpful to a playwright, so that they can change their pieces to appeal to whatever is "hot" at the moment.

### Alternative Methods of Analysis
Other possible ways to provide a cohesive analysis of this data would be to provide a box and whisker chart to identify any outliers in the data that could potentially skew our results.  We could also create bar charts as another way to show the numbers of successful, failed, and canceled plays over a period of time, similar to the Theater Outcomes based on Launch Date line chart that was made.  