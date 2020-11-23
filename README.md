# Kickstarter_Challenge
Two new analyses: outcomes based on goals and outcomes based on launch date and Written Report for Weekly Challenge 1

## Overview of Project
Continue to exercise my Excel prowess by creating two new analyses: outcomes based on goals and outcomes based on launch date, as well as a written report.
I will submit the following:
* Deliverable 1: Outcomes Based on Launch Date Chart
* Deliverable 2: Outcomes Based on Goals Chart
* Deliverable 3: A written analysis of the results (README.md)

### Purpose
>Louise’s play *Fever* came close to its fundraising goal in a short amount of time. Now, she wants to know how different campaigns fared in relation to their launch dates and their funding goals. Using the Kickstarter dataset that I’ve already combed through, I’ll visualize campaign outcomes based on their launch dates and their funding goals. I’ll then submit a written report based on my analysis and the visualizations I create.

## Analysis and Challenges
All source documents for this analysis can be found in [Git Hub](https://github.com/GloriaY007/Kickstarter_Challenge.git).

To perform the below analyis I had to first work with the Kickstarter data set, review the data, sort, filter, and clean some fields such as the *Launch Date* column. The *Launch Date* column was initially set up in UNIX format. I had to make sure that I transformed the numbers in that column to readable date formats in the *Date Created Conversion* column. After completing that step, I created a column named *Year* to extract the year for each row of data using the YEAR function. This led to findings below.

### Analysis of Outcomes Based on Launch Date
Using the entire set of data, I created a **Pivot table** that was set up to filter campaigns categorized as 'theather' in the Parent category column and I added a Year filter to easily drill down on the data. I also configured the pivot table to show and count outcomes for successful, failed, live, and canceled campaigns. I added the Date Created Conversion field to the rows to complete the pivot table.
After this initial set up, I then refine my selection by grouping the dates by Months, sorting the outcomes in descending order, and filtering only for successful, failed, and canceled campaigns. After this, I created a line chart to better visualize the findings

![Theater_Outcomes_vs_Launch](https://github.com/GloriaY007/Kickstarter_Challenge/blob/main/Theater_Outcomes_vs_Launch.png)


### Analysis of Outcomes Based on Goals
For this analysis, I had to mainly use the **COUNTIFS** function and the Kickstarter data set (Goal, Outcome, Subcategory columns). 
In a new worksheet, I first created the below columns:
- Goal
- Number Successful
- Number Failed
- Number Canceled
- Total Projects
- Percentage Successful
- Percentage Failed
- Percentage Canceled

Then, I listed in the *Goal* column 12 various ranges i.e. *Less than 1000, 1000 to 4999 etc...*.

This particular worksheet relied on a good understanding of the logic behind what I was looking for. For each columns, I was counting the data based on the range, whether or not the campaigns were successful, failed, or were canceled, and if they were subcategorized as *plays*. This requires that I set the COUNTIFS function right the first few times because, while duplicating the function, I could duplicate errors.

After completing the next three columns with the counts of successful, failed, or cancelled projects, I then used the **SUM** function to add up all projects for each row. I used that column for my next set of calculations. To find the *Percentage Successful* I divided the *Number of Successful* by the number of *Total Projects* and then formated the cell in percentage. I applied the same principle to all remaining columns and completed the table.

Once the table was completed, I inserted a line chart that helped us visualized the results of the table.

![Outcomes_vs_Goals](https://github.com/GloriaY007/Kickstarter_Challenge/blob/main/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
**The Pivot Table**:
The pivot table in itself is a fairly straightforward step, however depending on your version of Excel and understanding of the instructions, you can have some difficulties using the **Group Selection** button under the *PivotTable Analyze* header in Excel. This particular button was harder for me to play around with and configure. It took me a few tries and I finally:
1. Updated the *Date Created Conversion* column in the Kickstarter worksheet
2. Restarted a new Pivot Table 
3. Configured as mention above
4. Then, Grouped the selection **only** by Months

The end results was much cleaner and easier to understand.

**Table and chart**:
When it comes to the *Outcomes Based on Goal* worsheet, the challenge there is to pay attention on the criteria and range we are selecting withing the function. I initially forgot to include the Subcategories as a criteria and that skewed my results. I also had a few issues copying my formula over, and I used the dollar sign in my formulas ($) to ensure that the column that was refered in the formula remained the same. This quickly helped me finish my table.

## Results
- Outcomes based on Launch Date

Based on the chart we can conclude that from 2009 to 2017, the month of May has been the best time to launch a crowdfunding campaign. At the same time, December seems to be the worst time to start a gampaign.

- Outcomes based on Goals

Based on the chart we can conclude that all (100%) campaigns between $45,000 and $49,000 were unsuccessul. In fact, most successful campaign seems to be below $5,000, with 75% of successful campaigns being for less than $1,000.

- Limitations of this dataset

In my opinion, some of the limitations with this data set come with the lack of additional factors, aside from time and goal, to truly understand what makes a campaign successful. 

- Possible tables and/or graphs that we could create

There are many other charts that can be used to visualize this data set. For example, we could create **clustered columns** or **bars** to visualize the percentage of successful campaigns for less than $1,000, **pies** to see the percentage of successful campaign launched in January. In any case, the most important thing is to choose the right graphs to visualize the data. Chhosing the worong visualization tool could cause confusion with the viewer or lead to mistaken data interpretation.
