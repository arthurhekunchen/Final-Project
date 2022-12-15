# Final-Project

## Introduction

####  The data is about red wine samples (vinho verde) from Portugal. It was collected from May 2004 to February 2007 using only protected designation of origin samples that were tested at the official certification entity.

#### The data contains 1599 observations (wine samples) and 12 attributes or variables related to the wine. The 12 attributes and a description of each variable (attribute) are provided below in a tabular format. For more details, see the table below.
![image](https://user-images.githubusercontent.com/93305410/207961287-9218f210-18f3-48d6-b412-d366c135d213.png)

#### The objective is to determine the most effective method for determining the wine's quality, or in other words, explore the variables that may impact the quality of the wine.

## Results
### Model 1: Regression Model
<img width="244" alt="image" src="https://user-images.githubusercontent.com/93305410/207965889-a4e35845-1fa7-4b84-bc9c-e794506423ec.png">
As shown in Figure above, the model’s performance is ordinary, according to the evaluation metrics we use here. Only a 0.6219 accuracy out of 1.0, with CI of (0.5663, 0.6752). The kappa coefficient was calculated as 0.3489, which is a considerably fair result

### Model 2: Random Forest with Cross-validation
<img width="266" alt="image" src="https://user-images.githubusercontent.com/93305410/207966178-ad490581-5ae1-4a67-b08f-e6fbde42a00e.png">
<img width="306" alt="image" src="https://user-images.githubusercontent.com/93305410/207966220-49886e0f-c1cc-459c-938c-b895e0fd1404.png">
The variable importance plot in Figure 8 provides a list of the most significant variables in descending order by a mean decrease in Gini. The top variables contribute more to the model than the bottom ones and also have high predictive power in classifying default and non-default customers.

a) In this case, alcohol has the largest mean decrease in Gini compared to other variables, which demonstrates that it has high predictive power in predicting our target variable – wine quality. This is kind of reasonable since A wine with a higher alcohol content will have a fuller, richer body, while a lower-level alcohol wine will taste lighter and more delicate on the palate (Masterclass Staff, 2020).

b) Sulfites are a group of chemical compounds found naturally in a variety of foods and beverages. Research shows that a small percentage of the population is even sensitive to sulfites and may experience side effects like headaches, hives, swelling, stomach pain, and diarrhea. That may be one of the reasons why it’s the second most important of our all variables.

c) Besides, Total sulfur dioxide, Volatile acidity and Density also show high importance in our analysis, which may contribute to the realistic wine manufacturing process.

### Model 3: SVM
<img width="298" alt="image" src="https://user-images.githubusercontent.com/93305410/207966599-8188256d-9fe8-448d-8546-26d28f90aba5.png">
The accuracy of SVM is 0.6688, which indicates that the SVM model correctly predicts the value for quality more than 66% of the time. It’s just slightly worse than the random forest model, and much better than linear regression.

## Conclusion
o	I was able to construct a model that can help industry producers, distributors, and sellers forecast the quality of red wine products and better grasp each key and up-to-date characteristic by analyzing the physicochemical test samples data of red wines from the north of Portugal. 

o	Regarding our primary question, all features in our dataset have shown an effect on the quality of wine. The major findings are that alcohol level has had a major effect in determining the quality of wine. However, the increase in alcohol level has also been viewed as a feature of good wine but, it should not increase to an amount where the wine will be categorized as hard liquor.

o	I also discovered that Model #2 — Random Forest outperformed others with evaluation metrics in Table 3 below. The model indicates that 5 of the features were the most influential: alcohol, sulphates, Total sulfur dioxide, Volatile acidity and Density. High-quality wines appear to have lower volatile acidity, greater alcohol, and medium-high sulphate readings.

![image](https://user-images.githubusercontent.com/93305410/207966916-ed61f2f4-be94-4461-9b9b-00a63c2a390a.png)

## References
[1] Data Source: https://archive.ics.uci.edu/ml/datasets/wine+quality

[2] James, G., Witten, D., Hastie, T., and Tibshirani, R. (2013) An Introduction to Statistical Learning with applications in R, www.StatLearning.com, Springer-Verlag, New York

[3] P. Cortez, A. Cerdeira, F. Almeida, T. Matos and J. Reis. Modeling wine preferences by data mining from physicochemical properties. In Decision Support Systems, Elsevier, 47(4):547-553, 2009.


