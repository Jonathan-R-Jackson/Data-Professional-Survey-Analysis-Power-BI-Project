# Data Professional Survey Dashboard

### Dashboard Link : https://app.powerbi.com/links/jdwBvAKn-c?ctid=2f00ddd3-7478-4d4a-8024-2ad4c72167ec&pbi_source=linkShare

## Problem Statement

This dashboard was created with the intention of better understanding the Data Analyst population across various demographics by collecting a survey sample. The data collection process was completed by Alex Freburg via Linkedin, with the Survey dataset shared through Github Linked Below.

Data Professional Survey Dataset: https://github.com/AlexTheAnalyst/Power-BI/blob/main/Power%20BI%20-%20Final%20Project.xlsx 


### Steps Followed 

- Step 1 : Load data into Power BI Desktop, dataset is a xlsx file.
- Step 2 : Open the power query editor in order to transform/clean our data set.
- Step 3 : Remove the "Browser", "OS", "City", "Country", and "Referrer" columns since they're blank with no data entered.
- Step 4 : Within a few Columns, such as the "Which title best fits your current role" column, survey respondents were capable of using the "Other" Response selection on the submission form in order to manually enter their current job title causing duplicate entries that need to be standardized, but for the purposes of this dashboard I've split the column by the "(" delimiter in order to group all other entries together for a simplified analysis.
- Step 5: I was able to transform the salary ranges entered within the "Current Yearly Salary" column by obtaining the average of each range using the following DAX formula:
= Table.AddColumn(#"Replaced Value2", "Average Salary", each ([#"Q3 - Current Yearly Salary (in USD) - Copy.1"]+[#"Q3 - Current Yearly Salary (in USD) - Copy.2"])/2) 
- Step 6 : After applying the aforementioned data transformation steps, I then proceeded to the report view, from which I created eight Visualizations using six different graph types including a Treemap with Drill Down Capabilities, Stacked Bar Chart, Stacked Column Chart, Donut Chart, two Gauge meters, and two Data Cards.
- Step 7 : The report was then published to Power BI Service.


# Snapshot Of Dashboard (Power BI Service)

![Dashboard Screenshot in Power BI Service](https://github.com/user-attachments/assets/0759788c-5a48-4644-9fef-7eea21578fa6)


# Insights

The following inferences can be drawn from the dashboard-

### Total Number Of Survey Respondents = 630

   Number of Survey Respondents (Male) = 468 (74.29%)

   Number of Survey Respondents (Female) = 162 (25.71%)

   Work/Life Balance Satisfaction (Male) = Average Rating Of 5.77/10

   Work/Life Balance Satisfaction (Female) = Average Rating Of 5.66/10

   Salary Satisfaction (Male) = Average Rating Of 4.27/10

   Salary Satisfaction (Female) = Average Rating Of 4.28/10


           Thus we can conclude from the respondents surveyed Both
            Men & Women have similarly moderate to low levels of Salary
            Satisfaction and Work/Life Balance with their current position.
           
### Average Salary

    a) Data Scientist - 93.78K
    b) Data Engineer - 65.09K
    c) Data Architect - 63.67K
    d) Other - 60.49K
    e) Data Analyst - 55.30K
    f) Database Developer - 33.20K
    g) Student/Looking/None - 26.58K 
  
  These salary averages will adjust if different countries are selected within the Treemap or if Gender is specified using the respondent ethnicities graph.  
  
  ### Average Age Of Respondents 
  
    Average Age of All Respondents - 29.87
    Average Age of Male Respondents - 29.20 
    Average Age of Female Respondents - 31.78
