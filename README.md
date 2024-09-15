
# Data Analytics PWC-PowerBI-Virtual-Internship Project

I worked on PWC-PowerBI-Virtual-Internship Data Analytics Project. I will be diving into the background, my full process of cleaning, analyzing and visualizing the data, along with my final suggestions and summary of the data. Below is a table of contents in case you want to go to a specific section.

## Table of Contents

-  [My Role](#my-role)

- [Background](#background)

- [Data Analysis Process](#data-analysis-process)

- [Summary of Data](#summary-of-data)

- [Business Suggestions](#business-suggestions)

- [What I Learned](#what-i-learned)


### My Role: 
---
I recently completed a job simulation where I honed my Power BI skills to better comprehend clients’ data visualization requirements. I demonstrated proficiency in data visualization by creating Power BI dashboards that effectively communicated key performance indicators (KPIs), showcasing my ability to respond to client requests with meticulously designed solutions. I leveraged analytical problem-solving skills to scrutinize HR data, particularly focusing on gender-related KPIs, and identified underlying causes for gender balance issues at the executive management level, underscoring my commitment to data-driven decision-making.




### Background
---

This project is part of the PwC Switzerland Power BI in Data Analytics Virtual Case Experience, demonstrating the application of digital tools in data visualization, automation, data cleansing, and more to address common business challenges. It features a series of Power BI dashboards focusing on Call Centre Trends, Churn Analysis, and Diversity & Inclusion. Each dashboard provides actionable insights into different facets of business operations and strategic planning, aiding PwC Switzerland and its clients in enhancing operational efficiency, fostering customer loyalty, and promoting a more inclusive workplace.

Through meticulous data analysis and visualization, this project aims to support informed decision-making and highlight areas for improvement and innovation.



 


### Data Analysis Process
---

To do this, I will follow the six steps of the data analysis process: **Ask, Prepare, Process, Analyze and Share(Business Suggestions), and Act**.


  ## ASK
  
   #### Task2---- Call Centre Trends
         •  Overall customer satisfaction

         •	 Overall calls answered/abandoned

         •  Calls by time

         •	 Average speed of answer

         •	 Agent’s performance quadrant -> average handle time (talk duration) vs calls answered

   #### Task3----Customer Retention
   
       -  Define proper KPIs
       
       -  Create a dashboard for the retention manager reflecting the KPIs
       
       -	 Write a short email to him (the engagement partner) explaining your findings, and include suggestions as to what needs to be changed



  #### Task4----Diversity & Inclusion

       -	Define relevant KPIs in hiring, promotion, performance and turnover, and create a visualisation
       - Write what you think some root causes of their slow progress

   

 ##  Prepare

   The .pbix files associated with each dashboard are hosted within this repository. After installing Power BI Desktop, download the .pbix files from the repository and open them with Power BI Desktop. The data sources are embedded within the files, eliminating the need for additional setup to explore the visualizations. Users can navigate through the dashboards using the tabs at the bottom of the Power BI interface to explore different visualizations and insights.

To download the .pbix files, navigate to the folder in this repository where they are stored, select a file, and use the 'Download' button. Cloning or downloading the entire repository is an alternative method for accessing all files.




## Process

I downloaded the requisite dataset pertinent to the task and performed data cleansing. Utilizing the Power BI Desktop application, I created visualizations to discern trends. Additionally, I prepared measures to identify key performance indicators (KPIs).




## Analysis

   ### Call Centre Trends
The initial dashboard offers an exhaustive overview of call center metrics, emphasizing customer satisfaction, call volumes, and agent performance. It facilitates the identification of areas for enhancement in call center operations.

   #### DAX Measures Used

```Answered = CALCULATE(COUNT('Call Centre Trends'[Call Id]),FILTER('Call Centre Trends','Call Centre Trends'[Answered (Y/N)]="Y"))```

```Resolved(Y) = CALCULATE(COUNT('Call Centre Trends'[Call Id]),FILTER('Call Centre Trends','Call Centre Trends'[Resolved]="Y"))```








 #### Data Visualization Report

![image](https://github.com/user-attachments/assets/7eeec2f7-bac8-4ea4-b12d-f3336e275433)









  
   
   
   
   
 
   
  
   
   ### Churn Analysis

This dashboard was developed in response to a request from the telecom’s Retention Manager, highlighting key metrics pertaining to customer loyalty and retention. It visualizes data to forecast customer churn and identifies potential strategies to bolster customer retention. Access the live and interactive dashboards here.

   #### DAX Measures Used:
   
```% of Dependent = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Dependents]),'01 Churn-Dataset'[Dependents]="yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[Dependents]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```% of Partners = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Partner]),'01 Churn-Dataset'[Partner]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[Partner]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```% of Senior Citizen = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[SeniorCitizen]=1,'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```Online backup in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]),'01 Churn-Dataset'[OnlineBackup]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```Online Security in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),'01 Churn-Dataset'[OnlineSecurity]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```Phone Service  in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),'01 Churn-Dataset'[PhoneService]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```Streaming Movies in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),'01 Churn-Dataset'[StreamingMovies]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),'01 Churn-Dataset'[Churn]="Yes"),0)```

```Streaming Tv in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),'01 Churn-Dataset'[StreamingTV]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),'01 Churn-Dataset'[Churn]="Yes"),0)```










#### Data Visualization Report

![image](https://github.com/user-attachments/assets/93e7bc69-ca0c-4f3a-b690-ab7a2dfc3e65)







  
  
  
  
  
  
  

  
  
  
  
  ### Diversity & Inclusion
  
Focusing on the telecom client’s objective of enhancing gender balance at the executive management level, this dashboard visualizes metrics related to diversity and inclusion, providing insights into current trends and areas for intervention.

  #### Dax Measures Used
 
``` % of Female = DIVIDE('Pharma Group AG'[Number of Female],'Pharma Group AG'[Number of Male]+'Pharma Group AG'[Number of Female])```

```% of Male = DIVIDE('Pharma Group AG'[Number of Male],'Pharma Group AG'[Number of Male]+'Pharma Group AG'[Number of Female])```

```Number of Female = CALCULATE(DISTINCTCOUNT('Pharma Group AG'[Employee ID]),FILTER('Pharma Group AG','Pharma Group AG'[Gender]="Female"))```

```Number of Male = CALCULATE(DISTINCTCOUNT('Pharma Group AG'[Employee ID]),FILTER('Pharma Group AG','Pharma Group AG'[Gender]="male"))```





#### Data Visualization Report

![image](https://github.com/user-attachments/assets/b028ab38-7626-44b1-bf9f-d7c1121a8752)







## Summary Of Data
---

**Diversity and Inclusion**

•	Gender Distribution: Charts show the distribution of genders across different job levels, highlighting areas where there may be an imbalance.

•	Job Level by Age: Graphs indicate the distribution of job levels by age, suggesting opportunities to diversify age groups within certain roles.

•	Turnover Rate by Department: Data highlights departments with high attrition rates, indicating areas that may need targeted retention strategies.

**Call Center Performance**

•	Customer Satisfaction: Pie charts display average satisfaction ratings, suggesting areas for improvement in customer service.

•	Call Handling: Bar graphs show the number of calls answered each month, indicating trends in call volume and potential staffing needs.

•	Resolution Rates: Data on the percentage of resolved calls suggests opportunities to improve first-contact resolution through better tools and training.

•	Agent Performance: Tables list individual agents’ performance metrics, such as the number of calls answered and average speed of answer, helping identify top performers and those needing support.

**Customer Retention and Service Offerings**

•	Customers At Risk: Data highlights a significant number of customers who might churn, suggesting the need for targeted retention strategies.

•	Service Distribution: Charts show the distribution of services customers have signed up for, indicating opportunities for bundling or introducing new features.

•	Pricing Strategies: Data on yearly and monthly charges can be used to review and optimize pricing strategies to attract and retain customers.

These insights can help guide strategies to improve diversity and inclusion, optimize call center performance, and enhance customer retention and service offerings. 



## Business Suggestions
---
   ### Call Centre 

-	Enhance Customer Satisfaction: The pie chart showing the average satisfaction rating suggests focusing on areas where customer feedback is lower. Implementing training programs for agents to improve their communication and problem-solving skills can help boost satisfaction ratings.
   
-	Optimize Call Handling: The bar graph displaying the number of calls answered each month indicates trends in call volume. Analyzing these trends can help in optimizing staffing levels to ensure adequate coverage during peak times, reducing wait times and improving customer experience.
  
-	Improve Resolution Rates: The percentage of resolved calls can be increased by providing agents with better tools and resources to handle customer issues efficiently. Regularly updating the knowledge base and offering advanced training sessions can empower agents to resolve more calls on the first contact.
  
 -	Monitor Agent Performance: The tables listing individual agents’ performance metrics, such as the number of calls answered and average speed of answer, can be used to identify top performers and those who may need additional support. Recognizing and rewarding high-performing agents can boost morale and productivity.
 	
- Reduce Average Speed of Answer: The average speed of answer in seconds is a critical metric. Implementing strategies to reduce this time, such as improving call routing systems or increasing the number of available agents during high-traffic periods, can enhance overall efficiency.
- 
- Analyze Monthly Trends: The data on calls answered each month from January to March can be used to identify seasonal trends or patterns. This information can help in planning and preparing for future fluctuations in call volume, ensuring consistent service quality.
  
- Implementing these strategies can help improve overall call center performance, leading to higher customer satisfaction and more efficient operations. 

 ### Churn Analysis
 
  - Target At-Risk Customers: The “Customers At Risk” section highlights a significant number of customers who might churn. Implement targeted retention strategies such as personalized offers, loyalty programs, or proactive customer service to address their concerns and keep them engaged.
  
  - Enhance Service Offerings: The “Services Customers Signed Up” section shows the distribution of services. Consider bundling popular services or introducing new features that complement existing ones to increase customer satisfaction and reduce churn.
    
  - Optimize Pricing Strategies: The “Yearly Charges” and “Monthly Charges” data can be used to review and optimize pricing strategies. Offering flexible payment plans or discounts for long term commitments might attract and retain more customers.
    
  - Improve Customer Support: The “Number of Tickets” data suggests a need for efficient customer support. Investing in better support tools, training for support staff, and faster resolution times can improve customer satisfaction and reduce churn.
    
 - Analyze Demographics: The “Demographics” section provides insights into the customer base. Tailoring marketing campaigns and service offerings to specific demographic groups can help in better targeting and retaining customers.
  
  - onitor Payment Methods: The “Payment Method” data indicates the preferred payment options. Ensuring a seamless and secure payment process for these methods can enhance the customer experience and reduce churn.
    
 -  Focus on High-Churn Segments: The “Churn Analysis” section highlights segments with higher churn rates. Conducting in-depth analysis to understand the reasons behind churn in these segments and addressing them can help in retaining more customers.
    
 - 	Implementing these strategies can help improve customer retention, enhance service offerings, and optimize overall business performance
   

  ### Diversity & Inclusion
  
 -	Enhance Diversity and Inclusion: The charts show gender distribution across different levels. If there’s a noticeable imbalance, especially at higher levels, consider implementing programs to support the career advancement of underrepresented genders.
	
 - 	Targeted Recruitment: The job level by age graph suggests opportunities to diversify age groups within certain job levels. Tailoring recruitment strategies to attract a broader age range can help create a more dynamic and innovative workforce.
	
 - 	Reduce Turnover: The turnover rate by department highlights areas with high attrition. Investigate the reasons behind this and develop targeted retention strategies, such as improving work conditions, offering career development opportunities, or enhancing employee engagement.

 - 	Promotion Policies: The promotion data can be used to review and ensure equitable promotion practices. If external hires are favored over internal promotions, consider policies that support internal career growth.
	
- Mentorship Programs: Establish mentorship programs to support employees from underrepresented groups, helping them navigate their career paths and achieve higher positions within the company.

- Performance and Retention Analysis: Analyze the relationship between departmental performance and turnover rates. This can help identify if high performance expectations are contributing to higher turnover and address any underlying issues.
  
Implementing these strategies can help foster a more inclusive, balanced, and stable work environment.





# What I Learned



•	Completed a job simulation where I strengthened my PowerBI skills to better understand clients and their data visualisation needs.


•	Demonstrated expertise in data visualization through the creation of Power BI dashboards that effectively conveyed KPIs, showcasing the ability to respond to client requests with well-designed solutions.


•	Strong communication skills reflected in the concise and informative email communication with engagement partners, delivering valuable insights and actionable suggestions based on data analysis.


•	Leveraged analytical problem-solving skills to examine HR data, particularly focusing on gender-related KPIs, and identified root causes for gender balance issues at the executive management level, highlighting a commitment to data-driven decision-making.























