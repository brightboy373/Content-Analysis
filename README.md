# Social Buzz's Content Performance Analysis

## Project Overview

This project aims to provide insights into the content performance of a social media platform called Social Buzz. By Analyzing various aspects of the content data, we seek to answer some questions, identify the most popular content categories among users, make-data driven recommendations, and gain a deeper understanding of their content performances.

## Data Sources

+ Forage
  
## Tools

+ Excel (Cleaning, modeling, Visualization)

## Question for analysis
+ What are Top 5 best-performing Content Category?
+ What are Top 2 Best-performing Content type?
+ What is the month with the highest content published?

## STEPS TAKEN:

### Data Cleaning
- Ensuring Consistency in Data Types: I validated that each column contained only a single datatype, ensuring uniformity and accuracy across the dataset.
- Removing Unnecessary Characters: I used the "Replace" function to eliminate unwanted characters, such as quotation marks, that could interfere with the analysis.
- Dropping Irrelevant Columns: I identified and removed columns that were not essential for the analysis, such as the UserID column, to enhance focus and reduce noise.
- Renaming Columns for Clarity: To improve the dataset’s readability and interpretability:
  - I renamed Categories in the Content Table to Content Categories.
  - I renamed Scores in the Reaction Table and Reaction Type Table to Reaction Scores.

### Data Modeling:
Once the data was clean, I modeled the datasets by linking the 3 tables with VLOOKUP. Using SUMIF, I calculated the total reactions for each content category to uncover engagement trends. I copied all the datasets in different sheets in one workbook, this is to make it easier for me to reference and merge them in one sheet. By doing these I will have all the columns I need for my analysis and visualization. Using Vlookup to merge the table, here is the code: =VLOOKUP(A2,Content!A1:C1001,3, false).

### Data aggregation and Visualization: Data Visualization:
I created powerful visualizations using Pivot Tables and Pivot Charts, ensuring the charts were intuitive and used colour encoding to highlight the highest-performing values for clarity and emphasis.


## Insights
Despite technological advancement, animals are the most popular content category among users on Social Buzz.
Animals has over 1.8k reactions, which is more than any other category. Technology has the least reactions, with only 1.698k. While science, healthy eating, and food are also popular, none resonate with users as strongly as animal content, which consistently captures the most attention.

The month of May generated the highest number of posts, with 2.138k posts recorded, making it the most active month.
January and December followed closely, with December’s activity likely influenced by the festive and holiday season, as users tend to share more content during celebrations. 
In contrast, February recorded the lowest number of posts, possibly because users are more focused on work and routine activities during this time.

Photos and Videos are the best performing contents on social Buzz.
Photos lead with a performance of 51%, slightly outperforming video contents at 49%. This shows that while users might enjoy video contents, photos often deliver message more effectively and resonate faster with audiences than any other content type.
The “Heart” reaction is the most frequently used reaction on Social Buzz, indicating that majority of content resonates deeply with users’ emotions and feelings. Additionally, many post elicit the “scared” reaction, showing that some post create shock and fear. Additionally, “Hate” is also one of the least used reaction, followed closely by “interested”, which indicates that these types of content evoke fewer strong responses from users. 

## Recommendation

Social Buzz should enhance its algorithm to promote contents published in the month of December as users tend to post more content during holiday and festive period.
More attention should be allocated to animal and science content category especial photo and video contents, with addition of science and other categories so that users can have varieties of content to consume. For example, you could run a campaign with content focused on this category or work with healthy eating brands to promote content.

## Summary

We solved this task and found the top 5 most popular categories as asked, but we also went one step further.  We discovered that animals and science are the two most popular content categories, suggesting that users relate more with "real-life" and "factual" content. We also found out that while users might enjoy video contents, photos often deliver message more effectively and resonate faster with audiences than any other content type. This could be an indication to show the types of people that are using your platform, and you could use this insight to boost engagement even further. As much as this analysis communicated better insight, we are happy to take it to the next stage and we have the skills within Accenture to help you realize these kinds of insights in production and other sectors across your organization and in real-time. We would love to help you with this.




