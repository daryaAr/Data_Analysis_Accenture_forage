# Data_Analysis_Accenture_forage
This repository is about the data analysis project form Accenture's job simulator. In this simulator, I, as a Data Analyst will be a part of a team at Accenture. Our team has been assigned a new project for a client called **Social Buzz**.

## First Task: Understanding the problem

As a Data Analyst my first task is to read the brief from Social Buzz. This brief helps me for:

- Understand the client and business problem at hand.
- Identify the requirements that need to be delivered for this project.
- Identify which tasks you should focus on as a Data Analyst.
  
## Second Task: Data cleaning and modeling

as for my second task, the client has sent through:

7 data sets (each data set contains different columns and values) and a data model (this shows the relationships between all of the data sets, as well as any links that you can use to merge tables). The data model is as below:


 
  1. **User:**
      + ID: Unique ID of the user (automatically generated)
      + Name: Full name of user
      + Email: Email address of user
    
  2. **Profile:**
      + User ID: Unique ID of a user that exists in the User table
      + Interests: Interests of the associated user
      + Age: Age of the associated user
    
  3. **Location:**
      + User ID: Unique ID of a user that exists in the User table
      + Address: Full address of the user
    
  4. **Session:**
      + User ID: Unique ID of a user that exists in the User table
      + Device: Mobile device that they used for this session on the application
      + Duration: Amount of time in minutes that this user stayed active on the application during this session
    
  5. **Content:**
      + ID: Unique ID of the content that was uploaded (automatically generated)
      + User ID: Unique ID of a user that exists in the User table
      + Type: A string detailing the type of content that was uploaded
      + Category: A string detailing the category that this content is relevant to
      + URL: Link to the location where this content is stored
    
  6. **Reaction:**
      + Content ID: Unique ID of a piece of content that was uploaded
      + User ID: Unique ID of a user that exists in the User table who reacted to this piece of content
      + Type: A string detailing the type of reaction this user gave
      + Datetime: The date and time of this reaction

  7. **ReactionTypes:**
      + Type: A string detailing the type of reaction this user gave
      + Sentiment: A string detailing whether this type of reaction is considered as positive, negative or neutral
      + Score: This is a number calculated by Social Buzz that quantifies how “popular” each reaction is. A reaction type with a higher score
        should be considered as a more popular reaction.
        


To to make sure I am using the right data to answer the business questions I follow these steps:

1. Requirements gathering
2. Data cleaning
3. Data modelling

For the first step, requirements gathering, I use the data model to identify which datasets will be required to answer my business question - which is to figure out the top 5 categories with the largest popularity. As a result, I have found out that I need the datasets:

- **Reaction**
- **Content**
- **Reaction Type**

To clarify why I made this selection, I know that the brief carefully states that the client wanted to see “An analysis of their content categories showing the top 5 categories with the largest popularity”. As explained in the data model, popularity is quantified by the “Score” given to each reaction type. Therefore, I need data showing the content ID, category, content type, reaction type, and reaction score. So, to figure out popularity, I have to add up which content categories have the largest score.

Before begining, I have to imply the second step, which cleaning the data. In the jupyter notebook Accenture Cleaning, I cleaned the data by Clean the data by:

 + removing rows that have values which are missing,
 + changing the data type of some values within a column, andremoving columns which are not relevant to this task.





