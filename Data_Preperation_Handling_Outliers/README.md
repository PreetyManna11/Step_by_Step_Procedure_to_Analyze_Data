## Outliers

### What is Outliers?

Outliers are nothing but who is different from the rest of the community.

### Why is it important to handle outliers in your dataset?

Lets suppose you have a dataset with Name and Income column as shown below

Name    |  Income
A       |   10000
B       |   1000
Gates   |   400000000
X       |   5000
Y       |   4000

Among all the customers whose income lies from $1000 - $10000, Gates is the outlier.

Now Your stakeholder asked you to Calculate average Income of the customers, now if you calculate the average including the outlier, the average will be too high and it will mislead our stakeholders regarding the income of the customer as it will indicate that all the customers income is high. So in order to avoid this problem, we can follow the below cases :

Case 1 : You calculate average of the customers without including outlier, clearly mentioning it to the stakeholders.
Case 2 : You calculate average of the customers including outlier & clearly mentioning it to the stakeholders that outlier is included in order for thme to make a correct decision.

### What are the ways to handle outliers?

Once you are aware that a value is an outlier, you can quickly go back to data engineering team or Data collection Team and ask them whether

Case 1 : the outlier is a measurement error or not, if they say its a measurement error you need to delete that particular row.
Case 2 : if the outlier is not a measurement error and a viable value in that case we need to go back to the business problem and check what has been asked for?


### How to identify an outlier?



