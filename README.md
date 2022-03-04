# Machine learning Portuguese banking institution campaign prediction
<hr style="border:2px solid blue"> </hr>


#### Motivation: 

The overall problem we are tackling is that many banks want to know what type of customers would want to avail a campaign offer so that it will make them understand what type of users they should invest time into. We have set a baseline to first analyze the data through explanatory analysis, by explaining the data we set to analyze the problem statement by performing different classifiers, experimenting different ways to improve performance of those classifiers which can help in the prediction the campaign offers. The initial dataset is the banking dataset with 41188 rows and 21 features. Most features were categorial hence we tried to transform the data and use dummy variables to get in depth of each categorical variable within. The categorical variables were as following: 'job','marital','education','default','housing','loan','contact','month','day_of_week','poutcome'

<hr style="border:1px solid blue"> </hr>

### Research questions: Business goal and impact 
Our main research question is:

To predict whether a customer avails term deposit or not.
However, we did another sub research question in order to analyze the following research question:

#### Can willingness to subscribe for term deposit projects be predicted by education variable, marital status, job and other variables.
As these variables were categorical variables we can only analyze these through EDA, we came to a conclusion through the analysis that variables like education, martial, status does impact the term deposit as we saw that professionals with admin and blue collar jobs are more inclined towards accepting the term deposit. Also, customers who are married are more interested in accepting the term deposit. By looking at education variables we can also see that customers with a higher educational degree are more educated in terms of understanding the policies and terms to accept the term deposit. Furthermore, client whose job profession is admin have subcribed more to the bank deposit term. From all these analysis we came to a conclusion that material status and education has an impact towards term deposit.

#### Average portrait of the person who is willing to subscribe to a term deposit.
From the analysis we have predicted that young people are Millennials that who are currently between 25 and 40 years old are tending towards acceptance of term deposits. These people are highly educated and married. They are also those individuals who are doing high level jobs such as blue collar jobs. As a typical portrait of a person X who is inclined towards term deposit is someone with a highest education level and married witha a blue color job.

#### Exploratory Data Analysis (EDA): Data visualizations have you applied? What are your findings in the data before applying any data mining technique? At this stage sufficient EDA should have been done.
We created a correlation table and heat map of numerical features to see the highly correlated features with threshold 0.9. There are 3 variables which are largely correlated to each other, we are assuming a threshold as 0.9, the value greater than this threshold is assumed to be highly correlated. For instance, euribor3m, nr.employed, emp.var.rate all have correlation values greater than threshold value(0.9). We observe our dataset is not balanced looking at the target variable distribution graph.

Distribution plot for age column to see which age group have subscribed the term deposit, we found 25-50 years age group are more interested. We created lm plots to see if the trend differed between target variable ‘y’ and marital status with respect to age and campaign variables. Looking at the lmplot we observe clients who are married and whose age are between 25-45 years old are responsive toward term deposit. We created histogram for ‘duration’, we observed higher the duration of call, client subscribed more to term deposit.

We created join plot to see trend between age and campaign, we found 25-40 age group people were contacted multiple times for the campaign.

From statistical summary we analyzed that the bank was targeting clients with a minimum age of 17 years old.

We created a count plot for categorical features with respect to target variable ’y’. We observe a client whose job profession is admin has subscribed more to the bank deposit term. Married people are more interested toward term deposit subscription. People who have university degrees are showing more interest and may-august are the month where clients were contacted more by banks.Cellular phone is used more to communicate with the clients. The people with university degree education are the most subscribers to term deposit among all types of educated people.

#### Machine Learning (ML): Which ML techniques used and tried
We tried 7 different classifiers which are randomforest, decision tree, logistic regression, gaussian naive bayes, k_nearestneighbors, gradient boosting and support vector. Further we performed hyper-parameter tuning and PCA analysis over these classifiers in order to analyze performance between the classifiers. We also used a feature importance method for tree-based models( Decision tree and random forest). Decision tree classifiers tend to overfit very easily by memorizing the training data so to reduce the overfitting we chose random forest.


We ran the following classifiers intialled mentioned in the project proposal but we dropped the SVC classifier as it was taking a long time to execute and it was creating a burden on memory. Also for the huge number of dummy variables, svc is not applicable. In SVC we tried creating a model by removing categorical features and workin on numerical only but still it did not work.
<hr style="border:1px solid blue"> </hr>

### Next steps: 
We are thinking of grouping the age variable into different intervals of age groups and checking which interval age group subscribes more to term deposit. We will try to create a realistic model dropping the column 'duration' because when duration 0 there is no chance the client will subscribe to the term deposit. We can say the duration attribute is highly correlated to the target variable.

Other possible ways to improve the classification performance: Hyperparameter Tuning. This will affect the model's parameters during the training phase. So it is very essential to set the right hyperparameters. It is completely trial and error which can give you best accuracy by a few percentage points.

Treating Outliers as we do not have any missing values. Outliers can be biased on the accuracy of the model. Very important treatment.
