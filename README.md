# An Analysis of Kickstarter Campaigns
Performing analysis on Kickstarter data to uncover trends in theater campaigns.

## Overview of Project
Performing analysis on Kickstarter data to uncover trends in theater campaigns.

### Purpose
To determine the outcomes of theater campaigns based on their launch dates and funding goals, and have a visualization of these outcomes.

## Analysis and Challenges
In order to understand the data based on our purpose, it has to be filtered to get the desired visualizations. We want visualizations of theater outcomes based on goals, and outcomes based on launch date, so to do this we had to further break down the data and organize it in a way to achieve our purpose.

### Analysis of Outcomes Based on Launch Date
In the Kickstarter workbook, a new tab was created titled “Years” and the YEAR() function was used to extract the year the the “Date Created Conversion” column. A pivot table was created from the data in Kickstarter to create a new sheet titled “Theater Outcomes Based on Launch Date”. The pivot table is filtered based on “Parent Category” and “Years”, columns display “Outcomes”, rows display “Date Created Conversion”, and values display count of “Outcomes”. For the columns we are only looking at “successful”, “failed” and “canceled” within outcomes. Once the pivot table was created, the “Parent Category” was filtered to show data for “theater” and a line chart was created to visualize the relationship between outcomes and launch month.
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/89098766/132780970-3c9b5352-b03f-4d0b-b1f9-810072e6cbe7.png)

### Analysis of Outcomes Based on Goals
Within the Kickstarter sheet, a new sheet was created labeled “Outcomes Based on Goals”. Here we wanted to look at the data based on set goal ranges, and within those ranges the number successful, failed and canceled, as well at the percentages of each. The COUNTIFS() function was used to populate the “Number Successful”, “Number Failed”, and the “Number Canceled” columns based on each goal range for “plays” as the “Subcategory”. The SUM() function was then used to populate the “Total Projects” column with the number of successful, failed, and canceled projects for each row. To further understand the data the percentage of successful, failed and canceled projects were calculated for each row. A line chart was then created to visualize the relationship between goal ranges on the x-axis and the percentage of successful, failed, or canceled projects on the y-axis.
![Outcomes vs Goals](https://user-images.githubusercontent.com/89098766/132781003-f28ab66d-ad65-4c9a-a8d5-3a7a2a6d7b97.png)

### Challenges and Difficulties Encountered
The kickstarter workbook did not initially have the data laid out in a way we needed to visualize the data. The “Category and Subcategory” had to be further broken down into two new columns “Parent Category” and “Subcategory” so the data could be more easily filtered to look at the data needed for theater and plays. The “launched at” column only displayed a time stamp, so a “Date Created Conversion” column and “Date Ended Conversion” column were created to convert the time stamps into readable and filterable dates. Lastly to create the visual charts we needed, pivot tables were used to easily look at specific data.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
The month of May has the highest amount of successful campaigns as well as the highest amount of failed campaigns, however the success rate compared the the failure rate in May is much higher. After May the amount of successful campaigns steadily decreases while the amount of failed campaigns remains relatively consistent. May appears to be the best month to launch a campaign and December appears to be the worst month to launch a campaign.

- What can you conclude about the Outcomes based on Goals?
	Campaigns with goals of less than 1000 have the highest success rate at 75.8% and the lowest failure rate at 24.2%. There is some correlation between a higher goal and a lower success rate seen especially at the greater than 50000 goal that has a 16.7% success rate and a 83.3% failure rate. The most popular goal range for campaigns is 1000 to 4999, with 534 projects and has the second highest success rate at 72.7% with the second lowest failed rate at 27.3%

- What are some limitations of this dataset?
	This dataset is limited to a specific date range from the year 2009 to the year 2017, data outside of this year range could change the conclusions. Additionally these campaigns are all over the world so what is successful in one country could fail in another country or vice versa based on cultural preferences. We also only have data from Kickstarter, so this is not a full population of all theater projects during this time period.
	
What are some other possible tables and/or graphs that we could create?
Additional possibilities for tables include Theater Outcomes by Country to further breakdown the data of successful and failed projects by each country. We can also use box and whisker plots to compare the distribution of goals and total amounts pledged. This will help determine the median of the data and see any outliers, so that campaign goals can be realistically set based on the data provided.
