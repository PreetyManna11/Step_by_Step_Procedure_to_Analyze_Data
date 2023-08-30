
## Data Processing - Handling Missing Values

Handling missing values is one of the most important steps in Data Analysis Framework. It cannot be very evident whether your analysis will have a direct impact or not but the impact is a bit subtle but that subtle impact itself can change your analysis.

Here we are going to discuss about below questions :
1. Why is it important to handle missing values?
2. How a missing value is represented?
3. How to identify missing values?
4. How to handle missing values?
   
### Why is it important to handle missing values?

There are two reasons behind it :
* Suppose if you are working with some Machine Learning Model, you need to handle missing values properly as it won't work until and unles you provide a complete dataset.
* Let consider from Analysis POV:
Lets say Your stakeholders asked you to calculate Average Income of all the 100 Customers from the given dataset and you have 5 missing values in your dataset in the income column so you went back to the Data Engineering Team/Data collection Team to enquire regarding the missing values and lets consider 2 scenerios regarding what Data Engineering Team/Data collection Team have informed you :

1. Due to some reason they were not able to collect the data.
2. The customers with missing values income is 0. Let's consider 2 cases :
   
   Case 1 : Now in this case suppose if you directly delete these 5 missing values data, in that case you calculate the Average of 95 customer's income.
   
   Case 2 : Now a consider a case where you replace the missing values with 0 and then calculate the Average of 100 customers.

Now if you compare the Average values of Case 1 to Average value of Case 2, Average value of Case 2 is much more smaller than the Case 1 so if you present your analysis infront of stakeholders, it will be quite misguiding. So in order to avoid such mistakes, it's important to handle missing values.


### There are several ways a missing value can be represented : 
* Blanks/Null Values
* Spaces
* Random Value
* Big Value
* Special Character

There can be N no. of possibilities, how a Missing value can be represented.
It is really important for a data analyst to understand how a missing values can be represented. In order to know how your missing value is represented or what does the missing value means, you need to go back to your Data Eng Team/Data Collection Team.

### How can you identify missing values in the dataset?

* First you need to ask your Data Engineering Team/Data collection team that how is the missing values represented.
* If its represented in the form of Blank/Null Values, You can apply filter to the dataset and check the drop down of the filter to identify whether you have any blank cell in any of the columns.
* You can use COUNTA function to calculate the total no. of filled up cells and then your can calculate the difference between the total no. of cells & the filled up cells in order to get the missing values.
* If it is represented in the form of ten 9's or nine 8's, it will be quite easily be identified using filters.


### How to deal with missing values?

1. Suppose you have a case where you are dealing with data having millions of rows and you have 4-5 missing values and you are not using any machine learning models, in this case you can simply leave as missing values as it is since there are millions of rows and with 4-5 missing values it wont create huge impact on your Analysis.
2. Suppose you have millions of rows and 1-2 values are missing in this case you can delete the rows. But suppose you have 1000's of rows and 100's of rows having missing values so in this case you cannot delete the rows as if you delete it, other rows which were having some values will also get impacted and significant amount of data will get deleted and will later on impact your analysis and decision making of the stakeholders. So if your dataset is small and you have significant amount of missing values, probably 2% to 3%, its better not to delete.
3. The third case can be by using data imputation.

   What does an imputation mean?
   It means you can impute a value or add a value.

   Now there are several ways you can do imputation:
   1. Whenever you see nulls you can fill up with 0.
   2. If you have a categorical column having string type of data, whichever will have a mximum amount of a particular text, you can replace it with that using MODE function.

   Now for numerical column its not that easy that you replace it with zero for thta you need to go back to data engg. team and aks what does the missing value means and ask them whether they had an income or not. If they say they dont have an income in that case its safe to say that you can put 0. But in case where they have an income you need to impute it with either Average/Median.
   - In this case, you first need to calculate Standard Deviation, Average & Median. Now if you see your standard deviation value is a lot lesser than your Average, you can impute the values with average but if your standard deviation is around, equal to or more than average then impute the values with median. So the method we are following here is based upon the principles of Normal Distribution.




### Source

- Coding Ninjas

#### Hi, I'm Preety! 👋


#### 🚀 About Me
I have completed my graduation from SRM, Chennai and now I am working as a Software Engineer at Cognizant. I have a keen interest in the field of Data Analytics and look forward to enhance my knowledge in the same. 


#### 🛠 Tools required for Analyzing the Data using the framework
MS Excel, Google Spreadsheet


## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/preety-manna-687a73194/) 
  
