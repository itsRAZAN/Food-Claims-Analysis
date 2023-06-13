# Analyzing customer churn (CASE STUDY)

## Background
Vivendo is a fast food chain in Brazil with over 200 outlets.
Customers often claim compensation from the company for food poisoning.
The legal team processes these claims. The legal team has offices in four locations.
The legal team wants to improve how long it takes to reply to customers and close claims.
The head of the legal department wants a report on how each location differs in the time it
takes to close claims.

###  Data Validation 

  To prepare the dataset for our analysis,we explored the data using Power BI for initial review. The original data is **2000** rows and **8** columns, The first thing was to check the data type for all columns, we change "Claim Amount" column from string to decimal number rounded by 2 with currency of Brazil,and for "amount paid" column there were 36 missing value that have been replaced by 20106 the overall median amount paid , and for linked cases 26 missing values was switched with False to correctly made this column as True/False values, for last column cause there were 5 distinct values because meat and vegetable values showed up as lower and uppercase, so we make all values spelled with lowercase. Looking at the remaining columns:

- There are 2000 rows and 8 column, with 2000 unique Claim ID.
- Time to close are all positive value , with no missing values.
- There are 4 different location categories, as expected.
- individuals_on_claim minium range start from 1 to 15, with no missing value.
- There are 2 linked cases options after cleaning - True/False.
- There are 3 causes options after cleaning - “vegetable”, “meat” or “unknown”.

### Which location has the most number of claims?

 There are four location included in this data were the legal team processes these claims, there are Recife, Fortaleza,sao Luis and Natal.The office that receives the most number of claims is in Recife, with sao Luis being second although with half the number of claims then less in Fortaleza and Natal with approximately the same number of claims.This would suggest that the head of the legal department should focus on distributing their members in location with most claims to handle the sutations.
   
![viz1](https://github.com/itsRAZAN/Data-Analysis-Projects/assets/128379502/9917cdc0-3c9f-4a23-8648-2be3c13ff6e2)

### Are Claims balanced across location?
  In another representation of the total number of claims, to see whether the claims are balanced or equal among all four locations, we can say through the chart below that the percentage of 44.25% or almost two-quarters the number of claims received by the Recife office, and the other quarter 25.85% received by the sao Luis office, and the last quarter is divided between the Fortaleza and Natal offices.
  


![viz2](https://github.com/itsRAZAN/Data-Analysis-Projects/assets/128379502/be835dce-3a3f-453a-be72-f1a87044e33d)


              
 ### What is the distribution of time to close claims?

  As the head of the legal department thinks that the time to close for all claims will be important, we should look at how is it distributed. The number of days a claim takes to reply to customers and close claims is often around 100-200 days. And most of the claims close around 170 days.There are some vlaues that get long times to close around 300, 400 and even 500 but this is very uncommon. When looking for claims that are taking longer days, the team should target claims that are 300+ days or more.But we should aware that we may need to work with claims that take less days.
  
  

  

![viz3](https://github.com/itsRAZAN/Data-Analysis-Projects/assets/128379502/8032e835-23dc-4a9f-b2c6-9e921222549b)

  
  ### How does the number of claims vary across each location?
 Finally we want to combine the two pieces of information to see how long claims take days to close depending on their location. So with clamis that take at most 170 days in four locations would be the enough time to close, but we need to look at the two variables together to see if this is realistic.
 In the graphic below we can see that Fortaleza office receives a half quarter of the claims received by the Recife office, and it takes a long time to close it, with few claims that take the longest time outside the norm, as well as the Natal office. On the other hand the Recife office receives the largest number of claims, yet it completes them as soon as possible and with high efficiency. But this could also be an effect of having the most number of lawyers with high efficiency
 
 ![viz4](https://github.com/itsRAZAN/Data-Analysis-Projects/assets/128379502/71d88374-f8d0-4273-93ef-b0d8b845348d)



#### Based on all of the above, we would recommend that the head of legal team to focus on certain location that have highest individual claims and to focus on the offices of Fortaleza and Natal, as they receive the least number of claims,yet it takes a longer time to complete them. Further analysis should be done to understand why the Recife office receives the largest number of claims and the reason for that.This case should be done in further analysis.

