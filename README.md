![logo](logo.png)
<br><br>
A notebook that uses Titanic dataset on kaggle to build a predictive model that answers the question: “what sorts of people were more likely to survive?, this notebook includes Data Exploration with visualizations, Data Wrangling and Model building. [Competition Link](https://www.kaggle.com/c/titanic/overview)

# Models 🧮

| Model | Parameters | Acc|
| ------- | -------- | ----------|
| Logistic Regression | Defaults with max_iters = 200 | 0.74|
| GradientBoostingClassifier | Defaults | 0.78|
|SVC | Defaults | 0.69|

# Score 🏆
| Rank  🏅   | TOP 22%|
|---------|---------|
| Acc  🎯   |  0.78   |

# Machine Learning Workflow 3️⃣🔄
1. Data Exploration 🔎
    *  Univariate
    *  Bivariate
    
2.  Data Pre-processing 🛠
    1.  Data Cleaning 🚿
        * Fill NaNs in Age with Mean
        * Fill NaNs in Cabin with most frequent value for each group (grouped by Pclass)
        * Fill NaNs in Embarked with most frequent value 'Southampton'
        * Fill NaNs in Fare with Mean
        * Drop Ticket and PassengerId
    2.  Feature Engineering ⚙️
        * map Cabin values to first letter in its value: to be [A,B,C,D,E,F,G,T]
        * create Family Size, = Parch + SibSp +1
        * create FSize as a categorical value [single, small, Mid, Large]
        * create weightedFare = pow(Fare,i) where i is in [4,3,2]
        * map Name values to ['Mr', 'Mrs', 'Miss', 'Master']
3.  Model Building ⚖️
    * split data to train, test with ratios 80%, 20% respectively
    * build the models stated above
    * fit the model on train
    * evaluate the model on test before submission
    
    
# To DO 📌:
  * Improve the accuracy and rank
