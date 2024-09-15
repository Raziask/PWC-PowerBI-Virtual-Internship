
### Data Analytics PWC-PowerBI-Virtual-Internship Project

I worked on PWC-PowerBI-Virtual-Internship Data Analytics Project. I will be diving into the background, my full process of cleaning, analyzing and visualizing the data, along with my final suggestions and summary of the data. Below is a table of contents in case you want to go to a specific section.

### Table of Contents:

- Background

- Process Microsoft Excel ,SQL,Tableau

- Analysis Process

- Summary of Data

- Business Suggestions

- What I Learned




### Background

This project is part of the PwC Switzerland Power BI in Data Analytics Virtual Case Experience, demonstrating the application of digital tools in data visualization, automation, data cleansing, and more to address common business challenges. It features a series of Power BI dashboards focusing on Call Centre Trends, Churn Analysis, and Diversity & Inclusion. Each dashboard provides actionable insights into different facets of business operations and strategic planning, aiding PwC Switzerland and its clients in enhancing operational efficiency, fostering customer loyalty, and promoting a more inclusive workplace.

Through meticulous data analysis and visualization, this project aims to support informed decision-making and highlight areas for improvement and innovation.



 

### My Role: 
I recently completed a job simulation where I honed my Power BI skills to better comprehend clients’ data visualization requirements. I demonstrated proficiency in data visualization by creating Power BI dashboards that effectively communicated key performance indicators (KPIs), showcasing my ability to respond to client requests with meticulously designed solutions. I leveraged analytical problem-solving skills to scrutinize HR data, particularly focusing on gender-related KPIs, and identified underlying causes for gender balance issues at the executive management level, underscoring my commitment to data-driven decision-making.

To do this, I will follow the six steps of the data analysis process: Ask, Prepare, Process, Analyze and Share, and Act. SQL Queries Used in perform the above steps:


### ASK
# Task2---- Call Centre Trends
•	Overall customer satisfaction
•	Overall calls answered/abandoned
•	Calls by time
•	Average speed of answer
•	Agent’s performance quadrant -> average handle time (talk duration) vs calls answered

# Task3----Customer Retention


1.	Define proper KPIs
2.	Create a dashboard for the retention manager reflecting the KPIs
3.	Write a short email to him (the engagement partner) explaining your findings, and include suggestions as to what needs to be changed



# Task4_Diversity & Inclusion

1.	Define relevant KPIs in hiring, promotion, performance and turnover, and create a visualisation
2.	Write what you think some root causes of their slow progress

 ###  Prepare

   The .pbix files associated with each dashboard are hosted within this repository. After installing Power BI Desktop, download the .pbix files from the repository and open them with Power BI Desktop. The data sources are embedded within the files, eliminating the need for additional setup to explore the visualizations. Users can navigate through the dashboards using the tabs at the bottom of the Power BI interface to explore different visualizations and insights.

To download the .pbix files, navigate to the folder in this repository where they are stored, select a file, and use the 'Download' button. Cloning or downloading the entire repository is an alternative method for accessing all files.




### Process:
I downloaded the requisite dataset pertinent to the task and performed data cleansing. Utilizing the Power BI Desktop application, I created visualizations to discern trends. Additionally, I prepared measures to identify key performance indicators (KPIs).

### Analysis:

   ## Call Centre Trends
The initial dashboard offers an exhaustive overview of call center metrics, emphasizing customer satisfaction, call volumes, and agent performance. It facilitates the identification of areas for enhancement in call center operations.
     # Data Set:[Download Here](

    # DAX Measures Used

```Answered = CALCULATE(COUNT('Call Centre Trends'[Call Id]),FILTER('Call Centre Trends','Call Centre Trends'[Answered (Y/N)]="Y"))```

```Resolved(Y) = CALCULATE(COUNT('Call Centre Trends'[Call Id]),FILTER('Call Centre Trends','Call Centre Trends'[Resolved]="Y"))```



![image](https://github.com/user-attachments/assets/7eeec2f7-bac8-4ea4-b12d-f3336e275433)




   ## Churn Analysis

This dashboard was developed in response to a request from the telecom’s Retention Manager, highlighting key metrics pertaining to customer loyalty and retention. It visualizes data to forecast customer churn and identifies potential strategies to bolster customer retention. Access the live and interactive dashboards here.

   # DAX Measures Used:
   
```% of Dependent = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Dependents]),'01 Churn-Dataset'[Dependents]="yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[Dependents]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```% of Partners = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Partner]),'01 Churn-Dataset'[Partner]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[Partner]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```% of Senior Citizen = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[SeniorCitizen]=1,'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```Online backup in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]),'01 Churn-Dataset'[OnlineBackup]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```Online Security in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),'01 Churn-Dataset'[OnlineSecurity]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```Phone Service  in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),'01 Churn-Dataset'[PhoneService]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```Streaming Movies in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),'01 Churn-Dataset'[StreamingMovies]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```Streaming Tv in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),'01 Churn-Dataset'[StreamingTV]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),'01 Churn-Dataset'[Churn]="Yes"),0)```





![image](https://github.com/user-attachments/assets/93e7bc69-ca0c-4f3a-b690-ab7a2dfc3e65)


  ## Diversity & Inclusion
Focusing on the telecom client’s objective of enhancing gender balance at the executive management level, this dashboard visualizes metrics related to diversity and inclusion, providing insights into current trends and areas for intervention.

 #Dax Measures Used:
 
``` % of Female = DIVIDE('Pharma Group AG'[Number of Female],'Pharma Group AG'[Number of Male]+'Pharma Group AG'[Number of Female])```

```% of Male = DIVIDE('Pharma Group AG'[Number of Male],'Pharma Group AG'[Number of Male]+'Pharma Group AG'[Number of Female])```

```Number of Female = CALCULATE(DISTINCTCOUNT('Pharma Group AG'[Employee ID]),FILTER('Pharma Group AG','Pharma Group AG'[Gender]="Female"))```

```Number of Male = CALCULATE(DISTINCTCOUNT('Pharma Group AG'[Employee ID]),FILTER('Pharma Group AG','Pharma Group AG'[Gender]="male"))```

![image](https://github.com/user-attachments/assets/b028ab38-7626-44b1-bf9f-d7c1121a8752)

### What I Learned



•	Completed a job simulation where I strengthened my PowerBI skills to better understand clients and their data visualisation needs.


•	Demonstrated expertise in data visualization through the creation of Power BI dashboards that effectively conveyed KPIs, showcasing the ability to respond to client requests with well-designed solutions.


•	Strong communication skills reflected in the concise and informative email communication with engagement partners, delivering valuable insights and actionable suggestions based on data analysis.


•	Leveraged analytical problem-solving skills to examine HR data, particularly focusing on gender-related KPIs, and identified root causes for gender balance issues at the executive management level, highlighting a commitment to data-driven decision-making.























