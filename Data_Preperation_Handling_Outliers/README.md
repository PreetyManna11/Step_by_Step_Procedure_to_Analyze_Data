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


### How to identify an outlier?

To identify an outlier you need to create box plot of a particular column. In order to make a box plot of a particular column, we need to have atleats 4 statistical summary. Here we will be using Quartile function in order to calculate our statistical summary.


T.B.C




### Source

- Coding Ninjas


#### Hi, I'm Preety! 👋


#### 🚀 About Me
I have completed my graduation from SRM, Chennai and now I am working as a Software Engineer at Cognizant. I have a keen interest in the field of Data Analytics and look forward to enhance my knowledge in the same. 


#### 🛠 Tools required for Analyzing the Data using the framework
MS Excel


## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/preety-manna-687a73194/) 



