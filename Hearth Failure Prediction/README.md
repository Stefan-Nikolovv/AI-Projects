### Heart-Failure-Prediction Project ##
# Used dataset can be found in Kaggle here: [text](https://www.kaggle.com/datasets/andrewmvd/heart-failure-clinical-data/data)


# 1. Importing Required Libraries
# The code starts by importing several important Python libraries:
## pandas: For data manipulation and analysis.
## numpy: For numerical computations.
## matplotlib.pyplot and seaborn: For data visualization.
## sklearn: For machine learning algorithms and tools.

## 2. Loading and Exploring the Dataset
### The dataset is loaded from a CSV file, and its structure is examined:
### data = pd.read_csv("heart_failure_clinical_records_dataset.csv")
### type(data)
### data.shape
### data.columns
# Note: data.shape: Returns the number of rows and columns in the dataset.
#       data.columns: Displays the names of the columns in the dataset.

### 3. Categorical and Continuous Variables
### The dataset is split into categorical and continuous variables:
### categorical_variables = data[["anaemia","diabetes","high_blood_pressure","sex","smoking"]]
### continuous_variables = data[["age","creatinine_phosphokinase","ejection_fraction","platelets",###  "serum_creatinine","serum_sodium","time"]]
### categorical_variables: Includes binary features such as anaemia, diabetes, etc.
### continuous_variables: Includes numerical features like age, creatinine_phosphokinase, etc.

### 4. Checking for Missing Values
### The code checks for any missing values in the dataset:
### data.isna().sum()
### data.isnull().sum()
### Note: At that point of your code we can see that we dont have any missing values or null values.

### 5. Statistical Summary of Continuous Variables
### A statistical summary of the continuous variables is generated:
### continuous_variables.describe()
### Note: that describe() will provide us statistics for our variables 
### like counts, median, min, max and etc.

### 6. Exploratory Data Analysis (EDA)
### 6.1. Death Event Count by Group
### The code groups the data by DEATH_EVENT and counts the number of occurrences:
### data.groupby("DEATH_EVENT").count()

### 6.2. Scatter Plot: Age vs. Platelets
### A scatter plot visualizes the relationship between age and platelets, colored by DEATH_EVENT:
### that will show us what are the death events by age and by platelets

### 6.3. Correlation Heatmap
### The correlation between features is visualized using a heatmap:
### that will show us what is the correlation for our variables we are using from -1 to 1 
### if the values starts with minus we have negative correlation 
### if the values starts with plus we have postive correlation
### that means we have on positive correlation variables depends on it

### 6.4. Categorical Data Count Plots
### Count plots for each categorical variable, split by DEATH_EVENT, are created:
### here we can see counts for each categorical variable depended on death event
### they are represented with 0 for lived and 1 for deaths

### 6.5. Continuous Data Histogram Plots
### Histograms for each continuous variable, split by DEATH_EVENT, are plotted:
### here we can see counts for each continuous variable depended on death event
### they are represented with 0 for lived and 1 for deaths

### 6.6. Box Plot: Sex vs. Age
### A box plot shows the distribution of age across sex, split by DEATH_EVENT:
### here we can see that are the death events for sex ( 0 is used for male an 1 for female)
### and for age in our dataset.

### 7. Survival Analysis Based on Different Factors
### here we can see your pie chart diagrams for our categorical variables 
### and represantation of precents of survival and not survival for each categaries
### 7.1. Smoking and Survival
### Pie charts illustrate survival status based on smoking:
### 7.2. Sex and Survival
### Pie charts show survival status based on sex:
### 7.3. Diabetes and Survival
### Pie charts demonstrate survival status based on diabetes:
### 7.4. Anaemia and Survival
### Pie charts show survival status based on anaemia:
### 7.5. High Blood Pressure and Survival
### Pie charts show survival status based on high blood pressure:

### 8. Data Preprocessing and Model Training
### 8.1. Feature Selection and Target Variable
### The features (X) and target variable (y) are selected:
### for x are used our categorical variables 
### for y are used our death event
### for trainning data we will use 30% data
### after that we have to make a Data Scalling 
### that will be acomplished bt using StandardScaler 
### with our x_train and x_test data

### 9. Training and Evaluating Machine Learning Models
### Several machine learning models are trained, and their performance is evaluated:

### First one that we are using is Logistic Regression:
### this model working witb binary data and provide us our accuracy score (which means how fast is the model with provided data from us.)

### Secound one that we are using is Support Vector Classifier (SVC):
### this model will make classification and will separate our data and will seek for the best hyperplane on our data and will provide us accuracy score

### The third one is  K-Nearest Neighbors (KNN):
### that model will seek for best neighbor and when we find whom is it will use it for continues 
### prediction and clasification for our data and provide us accuracy score as well as prevous ones.

### The fourth one is Naive Bayes
### will use our data for liniar classifcation of our trained data and will provide accuracy score for our data.

### The fifth one which is the final one that we are using is Random Forest
### combines the output of multiple decision trees to reach a single result. Its ease of use and flexibility have fueled its adoption, as it handles both classification and regression problems and provide us ccuracy score for our data.

### 10. Comparison of Model Accuracies
### that will provide us which model provide better accuracy_score and that means which is fastter than other ones on our case.


### Summary
### The code performs an end-to-end analysis of heart failure clinical data. It includes loading the dataset, exploring it, performing data visualization, and implementing several machine learning models to predict the survival of patients based on various clinical features. The performance of different models is then compared using accuracy as the metric.

