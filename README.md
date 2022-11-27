
# Terrorist Attack Prediction in Pyspark

## Overview:

In recent years, terrorist activities have been increasing throughout the world. According to a survey, about 68 thousand people lose their lives annually and 220 million people are affected every year due to natural (famine, earthquakes, tsunamis) and man-made calamities (terrorism). Although natural calamities have been constant, the terrorist activities have significantly increased over the years.

![image](https://user-images.githubusercontent.com/58203363/204162750-b83bbc31-2a19-46e7-aaeb-f55e14ee68cc.png)

## Project Objective:
•	To analyze terrorist activities around the globe and predict the success of a terrorist attack using different machine learning approaches


## Data 
We will be using Global Terrorism Database which is an open- source database including information on terrorist attacks around the world from 1970 through 2017. The GTD includes systematic data on domestic as well as international terrorist incidents that have occurred during this time period and now includes more than180,000 attacks. The database is maintained by researchers at the National Consortium for the Study of Terrorism and Responses to Terrorism (START).

Shape of original dataset

![image](https://user-images.githubusercontent.com/58203363/204162868-ae7f9ff6-e7f5-490e-9f41-b7f4edc9962d.png)

We Filtered data before 2012 due to unorganized data collection methodologies along with null values and empty rows for better performance of ML models.  

After Data Cleaning

![image](https://user-images.githubusercontent.com/58203363/204162892-3549bb02-b05f-4c3c-a704-4ca3114fe8d0.png)

## EDA Observations:

•	Iraq, Afghanistan, Pakistan and India have had highest number of terrorist attacks in recent years.

![image](https://user-images.githubusercontent.com/58203363/204162927-57c024c6-4447-4330-b55f-99bf47562f35.png)

•	Bombings/explosions and armed assault are the most common type of attacks to take place

![image](https://user-images.githubusercontent.com/58203363/204162989-79e5bb2d-4227-47e7-baa8-e547622e9479.png)

•	Analyzed variable relationships using correlation matrix for feature selection

![image](https://user-images.githubusercontent.com/58203363/204163019-313054b2-709a-4731-9e11-aac7dbf7a7eb.png)

Target variable: Success

Success has values

1 stands for success of the attack

0 stands for failure to implement the attack

As you can see below, our data has a class imbalance problem for the target variable
![image](https://user-images.githubusercontent.com/58203363/204163147-373eb3db-aec1-4b93-81ce-8a0e5c2015f1.png)

• We have solved this problem by weight balancing using inverse ratio of both classes.

## ML Workflow:
![image](https://user-images.githubusercontent.com/58203363/204163195-4db52dca-59d6-40ed-bd68-b16e973db823.png)

The project's processes and procedures are shown in this flowchart. Data cleansing comes first, during which we dealt with null and missing values. We have employed weights to equalize the data sample because our courses are unbalanced. After that, we performed feature engineering to prepare the numerical and categorical features for the pipeline model using the Sparks ML library's OneHotEncoder, StringIndexer, and VectorAssembler. We divided the data into training and testing going forward. Following this, we created models using random forest, naive bayes, logistic regression, and gradient boost. and after that analyzed them with the help of the classification evaluators in the Sparks ML library.

## Conclusion
Gradient Boost shows the highest accuracy, AUC, and F-1 score. The performance of the model has been further improved by preprocessing the data even further like removing outliers, transforming the skewed features, etc. One of the major takeaways from the project is that accuracy is not the only metric we need to look forward to while we are building the model, there are parameters that need careful consideration based on the use case. In the future, we could build ensemble models to get higher accuracy, precision, and AUC for the data. Additionally, the research could be extended to building multiclass classification, this will help in identifying the regions with high, medium and low risk of attacks such that preventive measures can be taken accordingly.
