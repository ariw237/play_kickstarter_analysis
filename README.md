# Kickstarting with Excel  
## Overview of Project  
This project is designed to gain additional insight into how different Kickstarter campaigns fared based on either their launch dates or their initial funding goals. We are assuming that our client, Louise, after launching a successful campaign for her play "Fever" and almost reaching her goal in a short period, needs this information for future planning. Ultimately this project is designed in order to obtain additional experience using newly acquired Excel data manipulation techniques.  
### Purpose 
We are given a large dataset of Kickstarter campaigns in a variety of categories and all with different funding goals, and results. Our goal here is to create visual data that describes the outcomes of the Kickstarter campaigns based on either: the date in which they were started, or the initial funding goal. Given that our client's focus is on plays, we will be focusing mainly theatre performances and plays. These charts will enable us to draw conclusions if any concerning how our campaign's outcome may be impacted by its funding goal or start date and/or time of year.
## Analysis and Challenges 

We are initially given a large excel spreadsheet:  

![excel_screenshot](https://user-images.githubusercontent.com/60231630/134794628-390354ec-cb7f-4805-a24f-d80611251866.png)

Note the campaign ids in the left-column along with data of interest in subsequent columns. 

### Analysis of Outcomes based on Launch Date

Our first challenge is to parse theatrical campaigns from the dataset along with the months from each of all the years the campaigns started.  This is accomplished using pivot tables to filter our campaign categories to only include theatrical performances. As we are interested in campaign outcomes as they relate to month of the year for all years represented in the dataset, we must parse out the month from the dates given for each campaign start date and add that to the pivot table as well.  The following images show several of the filters we applied and the columns we used in our pivot tables. 

Main dataset:

![filters_1](https://user-images.githubusercontent.com/60231630/134794887-165b376d-d1c3-407c-b758-6527129d38a5.png)

Pivot Table:

![filters_2](https://user-images.githubusercontent.com/60231630/134794894-1fe5db88-7df8-46e0-a210-b9d23cfcafc7.png)

Using these results we were then able to create graphs giving us information theatrical campaigns and the result of those campaigns based on the month of the year the campaign was started for all available years in the main dataset.

### Analysis of Outcomes based on Goals 
To determine how our the funding outcome is affected by the initial funding goal, it is necessary to count the number of particular outcomes of a campaign and "bin" that data into a set of funding goal ranges. Funding outcomes include: "successful", "failed", or "canceled". This entails creating a secondary spreadsheet with a column containing our "binned" funding goals:

![excel_screenshot_2](https://user-images.githubusercontent.com/60231630/134795046-b5c9548b-e409-4bbe-aa7c-69a40f15bf5a.png)

We then must add additional columns that give counts of successes, failures, and cancellations for each range of funding goals. This is accomplished using builtin functions such as COUNTIFS to obtain this information. For example:

![countif](https://user-images.githubusercontent.com/60231630/134795188-8b7d81db-b477-437e-ba8e-be24493f18af.png)

From this we can get outcome percentages based on funding goals and draw conclusions from this data. 



### Challenges and Difficulties Encountered  

Some of the more complex COUNTIF syntax created some difficulty. However this was overcome by trial and error testing different functions on random sets of data on random spreadsheets.

## Results  
- What are two conclusions you can draw about the outcomes based on Launch Date?  
  
  Based on the data it would appear that launch dates have no effect on the rate of campaign cancellations, however campaigns launched during April and May appear to   have the highest rates of successful outcomes and this trend seems to last into Northern Hemisperic summer. Visually it appears that successes and failures are       weakly correlated and that may need to be taken into account.
  
- What can you conclude about the Outcomes based on Goals?  
  
  The greatest spread between successes and failures occurs with goal amounts less than $1000. However if one must absolutely use higher goal, the greater spread       between successes and failures occurs between $35000 and $50000
  
- What are some limitations of this dataset?  
  
  We could look further and see how if these trends are similar across all countries in which case another dataset that takes into account time of year the campaign     starts but allows you to filter by country may provide more insight. Additional regression analysis in order to determine the probability of a campaign being         successful based on country and month might also help.  Summer occurs in the Northern Hemisphere during the months with higher successes. Do the same trends hold     true for countries in the southern hemisphere where winter is starting during those months. Perhaps dividing countries by hemisphere and seeing the trends             (successes by month) reverse themselves.
- What are some other possible tables and/or graphs we could create?  

  We need not limit ourselves to theatrical performance. Perhaps similar graphs of other campaigns related to the "arts" would give us some additional insight into     how to execute our campaign. Also, as noted above, creating graphs and tables to group countries by hemisphere might also be helpful.
