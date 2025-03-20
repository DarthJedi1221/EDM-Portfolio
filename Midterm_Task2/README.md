## Midterm Lab Task 2 -  Data Cleaning and Preparation using POWER QUERY
* Task Description:
Company X wants to clean and analyze job posting data from the Uncleaned_DS_Jobs.csv dataset (from Kaggle). The goal is to answer these questions:

1. Which job roles pay the most and least?
2. Which company sizes pay the best?
3. Where do specific job roles or titles pay the best and worst in a particular state?
   
# Steps Performed in Data Cleaning and Transformation:
* <ins>Clean Salary Estimate Column:
> <sup>Remove all characters after "(" in the Salary Estimate column and Use Transform → Extract → Text Before Delimiter and type "(".
* <ins>Create Min and Max Salary Columns:
> <sup>Create two new columns from Salary Estimate for Min Salary and Max Salary and Use Column from Examples → From Selection, then type values like 101 for Min Salary.
* <ins>Create Role Type Column:
> <sup>Categorize job titles into types like "Data Scientist", "Data Analyst", etc., using a Custom Column.
>> ***Example:***
```
if Text.Contains([Job Title], "Data Scientist") then  
"Data Scientist" 
else if Text.Contains([Job Title], "Data Analyst") then  
"Data Analyst" 
else if Text.Contains([Job Title], "Data Engineer") then  
"Data Engineer"
else if Text.Contains([Job Title], "Machine Learning") then  
"Machine Learning Engineer" 
else  
"other" 
```
* <ins>Fix Location Column:
> <sup>Correct the Location column by replacing city names with state abbreviations (e.g., "California" to ", CA").\
> Use Custom Column to replace city names, then split the column.
* <ins>Handle Negative Values:
> <sup>See competitors column filter all -1’s\
See revenues column filter 0’s\
See industry column filter -1’s 
* <ins>Clean Company Names:
> <sup>Remove unwanted words like "Rates" from the company name.
* Remove Unnecessary Columns:
> <sup>Delete columns like Description that are not needed for analysis.

# Screenshot of Dataset Before Cleaning and Transformation
<img width="569" alt="Before Cleaning and transformation m2" src="https://github.com/user-attachments/assets/5f9ca205-a8b8-43e3-bf30-00dc2f419e3a" />
# Final Output (Screenshot of Final Queries):

# Normalization
* _Dependencies and References of the QUERIES_
![Sample Output]
<img width="452" alt="Normalization m2" src="https://github.com/user-attachments/assets/671a7941-61b7-498e-840a-82bfdb1013b9" />

# Uncleaned DS Jobs(_Cleaned Data_)
![Sample Output]
<img width="571" alt="Uncleaned DS Jobs m2" src="https://github.com/user-attachments/assets/c2703586-f0f6-4aa8-af91-fc65d051c5a1" />

# Sal by Role Type dupl
![Sample Output]
<img width="572" alt="Sal_by_role_type_dup m2" src="https://github.com/user-attachments/assets/cef6cf0c-e783-4013-8fcd-b43610573882" />

# Sal by Size ref
![Sample Output]
<img width="569" alt="Sal by Size ref m2" src="https://github.com/user-attachments/assets/19f10df0-1274-465c-8c83-e13d3862ec91" />

# Sal by State ref
![Sample Output]
<img width="572" alt="Sal by State ref m2" src="https://github.com/user-attachments/assets/d0073dca-4b99-4e85-9e19-8c6c661b94b2" />


