## Goal
- For this project I was tasked with organizing and analyzing a database of 1,000 sample crowdfunding campaigns.
- The analysis was to determine whether past projects met or exceeded the initial goal to determine what attributes led to past projects receiving funding.
- To complete this analysis and uncover any possible trends, I was to utilize Excel conditional formatting, pivot tables, and visualizations.

## Method
- First, I obtained the provided dataset for analysis and modification
- I used conditional formatting to highlight the values of the Outcome and Percent Funded columns to demonstrate visually whether a campaign was successful, failed, canceled, or is currently live, and what percentage was funded
- The percentage was calculated using a formula that returned the amount of money raised relative to its initial goal:

![image](https://github.com/Grimmandrewj/Excel_Challenge/assets/120341249/66e889c2-ca20-495c-96b5-65e920567a44)

- I then used a formula [=LEFT(N2, SEARCH("/",N2,1)-1] to split the unwieldy Category & Sub-Category column by its delimiter to create two new categories with their respective values
- Using this modified data, I created a pivot table that visualized how many campaigns were successful, failed, canceled, or are currently live organized by category
- From this table, I created a stacked-column pivot chart that can be filtered by country

![image](https://github.com/Grimmandrewj/Excel_Challenge/assets/120341249/12b5e3a1-09a1-4023-99b4-43ecbe64e4b2)

- Then, I created a new pivot table that analyzes the initial sheet to demonstrate the outcome of the campaigns organized by sub-category
- From this table, I created a stacked-column pivot chart that can be filtered by country and parent category:

![image](https://github.com/Grimmandrewj/Excel_Challenge/assets/120341249/9b98d239-3532-4cb0-834c-74555cc22a3e)

- I noted the Deadline and Launched_At columns used Unix timestamps
- To correct this, I used a formula [=(C2-DATE(1970,1,1))*86400] to convert the data into Excel's date format and cleaned up the column names to Date Created Conversion and Date Ended Conversion
- After these modifications, I created a new pivot table visualizing values of the Outcome and Date Created Conversion columns with filters by parent category and years
- I created a pivot chart line graph from this table:

![image](https://github.com/Grimmandrewj/Excel_Challenge/assets/120341249/a69690b7-3206-4ffb-870e-878179f8f894)

- After completing the modification and visualization of the data, I completed an analysis pertinent to the purpose of the project

## Summary and Results
- Given the provided data, what are three conclusions we can draw about crowdfunding campaigns?
  - The highest number of crowdfunding campaigns were created in the categories that fall under media (film & video, music, and theater), and therefore these categories contain the most successful and failed campaigns of any other category. These categories may generate the most interest out of all the other categories
  - The campaigns with the fewest number of backers (regardless of average pledge amount) were the ones most likely to be canceled or failed
  - The majority of the campaigns with the loftiest goal (from $120,000 up to $190,000) ultimately failed before reaching or coming close to their goal, suggesting the initial goal was unrealistic.

- What are some limitations of this dataset?
  - The amount of backers is tallied without any other relevant information about the backers (e.g. demographics, geographical location, age, etc.)
  - The dataset only shows the outcome of campaigns with one crowdfunding strategy and does not show the potential success of campaigns with alternative strategies.
  - This dataset does not track reason for failure or cancelation. Was the goal not reached within a predetermined time period, were advertising funds depleted, did initial interest give way to slowing or stagnant pledges, etc.?

- What are some other possible tables and/or graphs that we could create, and what additional value would they provide?
  - A table, graph, or combination showing number of backers by category could demonstrate which categories attracted the highest number of people (which may provide a different perspective than outcome or overall amount pledged due to differences in the average amount donated per backer).
  - A table and graph showing total amount pledged compared to length of time a campaign was live could demonstrate which campaigns earned the most pledges in the shortest time. This could be a measure of popularity and importance, as well as success rate with a longer period from beginning date to ending date.
