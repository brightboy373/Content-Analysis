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
After cleaning the datasets, I modeled the data by linking the three tables (`Content Table`, `Reactions Table`, and `ReactionTypes Table`) using **Excel VLOOKUP**. This step consolidated the data into a single table for analysis and visualization.

#### Purpose of Each Table
- **Content Table**: Contains `ContentID`, `Content Categories`, and `Content Type`.
- **Reactions Table**: Stores reactions with fields like `ContentID`, `Reaction_Types`, `Reaction_Scores`, and `Date`.
- **ReactionTypes Table**: Maps `Reaction_Types` to `Reaction Scores`.

#### Linking the Tables
##### Understanding Relationships
- The `Reaction_Types` field is a primary key in the `ReactionTypes Table` but a foreign key in the `Reactions Table`. 
- The `ContentID` field is a primary key in the `Content Table` and a foreign key in the `Reactions Table`.

##### Creating a Merged Table
To prepare a **fact table** for analysis, I needed the following fields in one sheet: 
- `ContentID`
- `Content Categories`
- `Content Type`
- `Reaction_Types`
- `Reaction Scores`
- `Date`

I followed these steps:
1. **Add Blank Columns**: In the `Reactions Table`, I created blank columns for `Content Categories`, `Content Type`, and `Reaction Scores`.
2. **Use VLOOKUP**: I used the **VLOOKUP** function to populate these new columns by fetching data from the `Content Table` and `ReactionTypes Table`.

Example VLOOKUP function:
=VLOOKUP(A2,Content!A1:C1001,3,FALSE)


## Data aggregation and Visualization: Data Visualization:
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




