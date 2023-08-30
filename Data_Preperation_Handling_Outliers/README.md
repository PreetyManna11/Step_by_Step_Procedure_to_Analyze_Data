## Outliers

Handling Outliers is quite important while you Prepare your data. There are few questions which are worth asking while handling outliers:
1. What is outlier?
2. Why is it important to handle outlier?
3. How to handle outlier?

### What is Outliers?

In Plain English Statement, Outliers are nothing but which is different from the rest of the community.

### Why is it important to handle outliers in your dataset?

Lets suppose you have a dataset with Customer Name and Income column as shown below

Customer Name | Income |
--- | --- |
A | 10000 |
B | 1000 |
Gates | 400000000 |
X | 5000 |
Y | 4000 |

Among all the customers whose income lies from $1000 - $10000, Gates is the outlier.

Now Your stakeholder asked you to Calculate average Income of the customers, now if you calculate the average including the outlier, the average will be too high and it will mislead our stakeholders regarding the income of the customer as it will indicate that all the customers income is high. So in order to avoid this problem, we can follow the below cases :

Case 1 : You calculate average of the customers income without including outlier, clearly mentioning it to the stakeholders.

Case 2 : You calculate average of the customers income including outlier & clearly mentioning it to the stakeholders that outlier is included in order for thme to make a correct decision.

### What are the ways to handle outliers?

Once you are aware that a value is an outlier, you can quickly go back to data engineering team or Data collection Team and ask them whether

Case 1 : the outlier is a measurement error or not, if they say its a measurement error you need to delete that particular row.

Case 2 : if the outlier is not a measurement error and a viable value in that case we need to go back to the business problem and check what has been asked for? And accordingly we need to handle. If they have asked to caculate income then Probably show 2 cases as discussed above.


### How to identify an outliers In MS excel?

To identify an outlier you need to create box plot of a particular column. In order to make a box plot of a particular column, we need to have atleats 4 statistical summary. Here we will be using Quartile function in order to calculate our statistical summary.

Suppose you have few data for Amount spent by customer :

$2, $10, $18, $12, $3, $7, $100, $42, $27, $58, $112, $62

Now you need to arrange the data in ascending order to find out Quartile :

$2, $3, $7, $10, $12, $18, $27, $42, $58, $62, $100, $112
Qmin     Q1            Q2             Q3              Qmax

- Qmin     -> $2
- Q1       -> 25% (percentile) * (Total Count of Data) -> 3rd value
- Q2/median-> 50% (percentile) * (Total Count of Data) -> 6th value
- Q3       -> 75% (percentile) * (Total Count of Data) -> 9th value
- Q4/Qmax  -> $112 100% (percentile) * (Total Count of Data)
- IQR      -> Q3-Q1 (Inter Quartile Range)


In Excel, you simply need to calculate the Quartile value by using QUARTILE(array,quart) function by selecting the whole columns in place of array and providing what value of quartle you want from 1-4. This is how you find the value of all the quartiles in excel.

Now after you find out the quartile values 

Numeric Column Name | Qmin | Q1  | Q2  | Q3  | Q4

Now you need to select all the above values as mentioned and insert a box plot.

In the picture below

- Qmin -> Represented as a value 3 which usually is an outlier if its too distant from the box
- Q1   -> Represented as a value 5.25
- Q2   -> Represented as a value 15
- Q3   -> Represented as a value 23.75
- Q4   -> Represented as a value 29 which usuallly is an outlier if its too distant from the box
- IQR  -> Box height 

So this is how you identify whether an outlier is there or not.

![image](https://github.com/PreetyManna11/Step_by_Step_Procedure_to_Analyze_Data/assets/61684282/7880896f-f294-4cc5-a90e-32fdb5681915)

This helps to visualize the distribution of the data and immediately you can see whether the distance between Q3 and Qmax is too high or Q1 and Qmin is too high or not.

Now This way we can get some idea whether we have any outlier present or not using Box Plot/Candle Stick Chart.

Now Lets Analytically calculate that each of the value present in the dataset is an outlier or not.

Find out :

Qmin, Q1, Q2, Q3, Q4, IQR

Lets suppose V is the value and if 
V > Q3 + 1.5*IQR   -> indicates the value above Q3
V < Q1 - 1.5*IQR   -> indicates the value below Q1

If any one of the above criteria satisfies then the value is declared as Outlier

In Excel, we simply create a column to check outlier and use =IF(OR(V > Q3 + 1.5*IQR , V < Q1 - 1.5*IQR),1,0). This means if any of the condition mentioned above satisfies then it will give an output as 1 or else 0.




### Source

- Coding Ninjas


#### Hi, I'm Preety! 👋


#### 🚀 About Me
I have completed my graduation from SRM, Chennai and now I am working as a Software Engineer at Cognizant. I have a keen interest in the field of Data Analytics and look forward to enhance my knowledge in the same. 


#### 🛠 Tools required for Analyzing the Data using the framework
MS Excel


## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/preety-manna-687a73194/) 



