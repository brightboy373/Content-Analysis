# Social Buzz's Content Performance Analysis

## Project Overview

This project aims to provide insights into the content performance of a social media platform called Social Buzz. By Analyzing various aspects of the content data, we seek to answer some questions, identify the most popular content categories among users, make-data driven recommendations, and gain a deeper understanding of their content performances.

## Data Sources

+ Forage

## Datasets  
- <a href = "https://github.com/brightboy373/Content-Analysis/blob/main/Content.csv">Content Table</a>
- <a href = "https://github.com/brightboy373/Content-Analysis/blob/main/ReactionTypes.csv">ReactionTypes</a>
- <a href = "https://github.com/brightboy373/Content-Analysis/blob/main/Reactions.csv">Reactions</a>
  
## Tool(s)

+ Excel (Cleaning, modeling, Visualization)

## Question(s) for analysis
+ What are Top 5 best-performing Content Category?
+ What are Top 2 Best-performing Content type?
+ What is the month with the highest content published?

## STEPS TAKEN:

### Data Cleaning
- Ensuring Consistency in Data Types: I validated that each column contained only a single datatype, ensuring uniformity and accuracy across the dataset.
- I used the filter icon to identify blank spaces and inconsistencies in rows. I deleted the null values from the datasets.
- Removing Unnecessary Characters: I used the "Replace" function to eliminate unwanted characters, such as quotation marks, that could interfere with the analysis.
- Dropping Irrelevant Columns: I identified and removed columns that were not essential for the analysis, such as the UserID column, to enhance focus and reduce noise.
- Renaming Columns for Clarity: To improve the dataset’s readability and interpretability:
  - I renamed Categories and types in the Content Table to Content Categories and Content type.
  - I renamed Scores in the Reaction Type Table to Reaction Scores.
  - I renamed type from Reactions Table to Reaction Types.
   

### Data Modeling:
Once the data was clean, I modeled the datasets by linking the 3 tables with VLOOKUP. Using SUMIF, I calculated the total reactions for each content category to uncover engagement trends. I copied all the datasets in different sheets in one workbook, this is to make it easier for me to reference and merge them in one sheet. By doing these I will have all the columns I need for my analysis and visualization. Using Vlookup to merge the table.

To link these datasets in Excel I have to understand the relationships between one datasets and other. Reaction_Type is a primary key in ReactionTypes Table but a foreign key in Reactions Table, that’s a relationship and possible link merge both tables. The ContentID is a primary key in Content Table and also a secondary key in Reactions Table.

I needed Reaction scores from Reaction Table and Content categories from Content table, so in one table I can have ContentID, Content categories, Reaction_Types, Reaction scores, and Date in one sheet so that I can have all the rows required for my analysis.

On my fact table (Reactions Table), I will create a new column for Content category and Reaction Scores, then use Vlookup on the column created to drag the content category from content table and reaction scores on reactiontype table.

So I created a blank column by highlighting and right clicking on the another column, I created a column for content category in reactionS table in the same position it is indexed at content table and same for reaction scores. Created a column for content category and reaction scores in reactions table.
Using Vlookup to merge the table, here is the code: =VLOOKUP(A2,Content!A1:C1001,3, false).
The A2 was the lookup value from reactions table, Content!A1:C1001 (The table array covered the contentId to content_Category which is indexed 3) , false means return exact value only. I merged all the columns needed for the analysis in reaction sheet and I named them merged table



### Data aggregation and Visualization: Data Visualization:
I created powerful visualizations using Pivot Tables and Pivot Charts, ensuring the charts were readable and used colour encoding to highlight the highest-performing values for clarity and emphasis. I also created KPIs to show the month with the highest reaction, content category with most reaction, and unique content categories.

<img width="747" alt="Capture-charts" src="https://github.com/user-attachments/assets/ce610bae-2014-4db3-9a9d-85d2d1cb60dd" />



## Insights
Despite technological advancement, animals are the most popular content category among users on Social Buzz.
Animals has over 1.8k reactions, which is more than any other category. Technology has the least reactions, with only 1.698k. While science, healthy eating, and food are also popular, none resonate with users as strongly as animal content, which consistently captures the most attention.

The month of May generated the highest number of posts, with 2.138k posts recorded, making it the most active month.
January and December followed closely, with December’s activity likely influenced by the festive and holiday season, as users tend to share more content during celebrations. 
In contrast, February recorded the lowest number of posts, possibly because users are more focused on work and routine activities during this time.

Photos and Videos are the best performing contents on social Buzz.
Photos lead with a performance of 51%, slightly outperforming video contents at 49%. This shows that while users might enjoy video contents, photos often deliver message more effectively and resonate faster with audiences than any other content type.


## Recommendation

Social Buzz should enhance its algorithm to promote contents published in the month of December as users tend to post more content during holiday and festive period.

More attention should be allocated to animal and science content category especial photo and video contents, with addition of science and other categories so that users can have varieties of content to consume. For example, you could run a campaign with content focused on this category or work with healthy eating brands to promote content.

## Summary

I solved this task and found the top 5 most popular categories as asked, but we also went one step further.  I discovered that animals and science are the two most popular content categories, suggesting that users relate more with "real-life" and "exploratory" content. We also found out that while users might enjoy video contents, photos often deliver message more effectively and resonate faster with audiences than any other content type. This could be an indication to show the types of people that are using your platform, and you could use this insight to boost engagement even further.




