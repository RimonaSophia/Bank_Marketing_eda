# Bank Marketing Campaign Analysis

## Overview

This project analyzes data from a bank marketing campaign to answer three key questions regarding customer demographics and the effectiveness of marketing strategies. The analysis focuses on:

1. **Are married or single individuals more likely to subscribe?** This insight can help target promotions effectively.
2. **What is the impact of marital status on subscription rates?** This will allow for targeted marketing strategies.
3. **How does call duration affect subscription rates?** Understanding the average call duration for non-subscribers can inform the sales team's approach to improving engagement.

## Table of Contents

1. [Technologies Used](#technologies-used)
2. [Database Setup](#database-setup)
3. [Data Cleaning](#data-cleaning)
4. [Data Analysis](#data-analysis)
5. [Conclusion](#conclusion)

## Technologies Used

- Python
- Pandas
- Matplotlib
- Seaborn
- SQLite

## Database Setup

The data is stored in an SQLite database. The following steps were taken to create the database and insert data:

1. **Connect to SQLite Database**: A connection to the SQLite database (`bank_marketing.db`) was established.
2. **Create a Table**: A new table named `bank_marketing_t` was created to hold the relevant demographic data.
3. **Load Data**: Data was loaded from a CSV file (`bank-additional-full.csv`) into the SQL table.

### SQL Table Structure

The structure of the table is as follows:

| Column     | Type       |
|------------|------------|
| age        | INT        |
| job        | VARCHAR(50)|
| marital    | VARCHAR(50)|
| education  | VARCHAR(50)|
| duration   | INT        |
| campaign   | INT        |
| previous   | INT        |
| poutcome   | VARCHAR(50)|
| y          | VARCHAR(10)|

## Data Cleaning

Before analysis, the data underwent several cleaning steps:

1. **Select Relevant Columns**: Only the columns necessary for analysis were retained.
2. **Convert Data Types**: Object types were converted to categorical types to improve memory efficiency.
3. **Check for Null Values**: Verified that there were no missing values in the dataset.
4. **Insert Data**: The cleaned DataFrame was appended to the SQL table.

## Data Analysis

### Objectives
The analysis aims to address three key questions regarding the effectiveness of the bank's marketing campaign:

1. **Subscription Likelihood by Marital Status**: Are married or single individuals more likely to subscribe to the bank's offerings? This insight can help tailor promotional strategies based on the marital status of potential customers.

2. **Subscription Trends Among Different Marital Categories**: Further exploration of marital status to determine whether married individuals are more likely to subscribe compared to those in other categories. This data can inform targeted marketing promotions.

3. **Impact of Call Duration on Subscription Rates**: How does the duration of calls affect subscription decisions? Understanding the relationship between call length and subscription status may provide actionable insights for the sales team.

### Methodology
- **Data Preparation**: The analysis is conducted on data extracted from the `bank_marketing_t` SQL table, which contains relevant demographic information and subscription status. The data includes columns such as age, job, marital status, education level, call duration, and previous outcomes.


## Conclusion

### Key Findings
1. **Marital Status vs. Subscription Status**:
   - The count plots reveal the distribution of subscription status across different marital categories.
   - Initial observations suggest that **married individuals** exhibit a higher subscription rate compared to **single** and **divorced** individuals, indicating that targeted promotions could be more effective when aimed at married clients.

2. **Job Type Analysis**:
   - The job type count plot indicates varying subscription rates based on employment categories. Certain job sectors appear more likely to subscribe, highlighting potential segments for targeted marketing.

3. **Effect of Call Duration on Subscription Rates**:
   - The analysis showed that the mean call duration for subscribers is significantly higher than that for non-subscribers. Specifically, the average duration for non-subscribers is approximately **220.84 seconds**, while for subscribers, it is around **553.19 seconds**.
   - This finding suggests that longer engagement during calls correlates with higher subscription rates, indicating that the sales team should focus on optimizing call durations to enhance conversion rates.

### Implications for Marketing Strategy
- **Targeted Promotions**: Insights into marital status and job type can guide the bank's marketing team in designing targeted promotional campaigns tailored to specific demographics.
  
- **Sales Training**: Given the significant relationship between call duration and subscription likelihood, training the sales team to maximize effective engagement during calls could lead to increased conversion rates.
  
- **Follow-Up Strategies**: It may be beneficial to implement follow-up strategies that leverage these insights, focusing on customers who align with the identified high-conversion demographics.
