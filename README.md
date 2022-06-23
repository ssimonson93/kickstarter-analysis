# An Analysis of Kickstarter Campaigns
## Overview of Project

This project was conducted to find trends in data gathered from over 4000 Kickstarter Campaigns in order to determine whether there were any factors that correlated to improved success.  And individual, Louise, intends to begin a crowdfunding campaign on Kickstarter for her play "Fever."  As such, the data analysis was focused on the outcomes of campaigns for theater plays, in order to best decipher whether there are any tactics Louise could employ to increase her chances of success.

## Analysis and Challenges

Data analysis was done using a number of formulas and criteria.  Outcomes of each Kickstarter campaign were cross-referenced with the Launch Date and Funding Goal of each campaign.  Initially, the data set presented dates in Unix timestamp format, so the formula "=(((J2/60)/60)/24)+DATE(1970,1,1)" was used to convert these into normal dates, where "J" referred to the original Unix timestamp column.  The data set was then exported into a Pivottable, where outcomes could easily be counted, filtered, and presented by category and start month, as shown in Figure 1 below.  From this table, a line chart was created to show the count of these outcomes throughout a year, as shown in Figure 2 below.  Goals and Outcomes were analyzed somewhat similarly, except a table was created using a COUNTIFS formula to individually count how many campaigns succeeded, failed, or were canceled based on various ranges of funding goals.  Success, failure, and cancelation percentage was then calculated based on these counts, as shown in Figure 3 below.  From these percentages, another line chart was created to visualize success and failure percentage as goal amounts grew, as shown in Figure 4 below.  No major challenges were encountered, however due to the specificity of many of the formulas used minor mistakes were made that required correction.  Filtering columns incorrectly or omitting portions of formulas and data would result in misrepresented charts, so extra care was necessary to ensure calculations were done properly, and some initial calculations were done manually as well to double check that the desired outcome was being achieved.

### Figure 1

![This is an image](https://github.com/ssimonson93/kickstarter-analysis/blob/main/Outcomes_based_on_Launch_Date_PivotTable_screenshot.png)

### Figure 2

![This is an image](https://github.com/ssimonson93/kickstarter-analysis/blob/main/Theater_Outcomes_vs_Launch.png)

### Figure 3

![This is an image](https://github.com/ssimonson93/kickstarter-analysis/blob/main/Outcomes_vs_Goals_Table_Screenshot.png)

### Figure 4

![this is an image](https://github.com/ssimonson93/kickstarter-analysis/blob/main/Outcomes_vs_Goals.png)
	
## Results

Multiple trends can be seen in the analysis of the Kickstarter Outcomes based on Launch Dates.  The number of Kickstarter campaigns that reach their goals increases, for the most part, through the beginning months of the year, with a significant increase in successful campaigns that start in May specifically.  While this seems to be simply correlated to an increase in the total number of campaigns in May, the number of failed campaigns in May and the surrounding months stays steadily around 50.  This results in about a 67% success rate relative to the total number of campaigns launched in May, so from this trend a conclusion can be drawn that there is a higher chance Louise's campaign will reach its goal if she begins in May. Conversely, while the number of failed campaigns throughout the year stays relatively steady, there is a decline in success after May until December where the number of successful campaigns almost matches the number of failed campaigns.  From this trend, a conclusion can be drawn that Louise's campaign would have the worst chance of succeeding if it begins in December, where the rate of success is the lowest of any month at around 49%.  

From the analysis of the outcomes of Kickstarter Campaigns for Theater Plays by their funding goals, we see a trend of campaigns steadily succeeding less and failing more the higher the funding goal is.  The greatest percentage of projects reach their funding goals when only less than $5000 are necessary to achieve completion, while failure percentage quickly comes within 5% of success percentage in the $5000 to $9999 range and goes on to match and overtake success percentage when campaign goals grow above $15000.  Success rates do become higher than failure rates in the $35000 to $44999 goal range, however the very small amount of campaigns that ask for this amount of money makes it difficult to pinpoint why this may be happening.  Therefore, the main conclusion to be drawn is that the lower Louise can keep her Kickstarter goal amount, the higher chance of success she will have. 

One potential limitation of this dataset is the time period from which it is taken.  The latest campaign included is from May of 2017, and it is possible Kickstarter trends could have changed in the past 5 years.  Also, the descriptions of each campaign are fairly sparse, and further analysis could potentially be done if more detail was provided as to the distribution of the funding for which each project was asking.

While the analysis done was able to come up with a few factors indicating improved success, further analysis could possibly show more correlations.  Particularly, using each campaigns end date, a graph could potentially be constructed showing the number of successful, failed, and canceled outcomes based on the length of time a campaign was active.  This could produce further trends depicting whether a shorter or longer campaign has any correlation to success or failure.
