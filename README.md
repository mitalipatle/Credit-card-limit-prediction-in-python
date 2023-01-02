# Credit-card-limit-prediction

## Introduction:
Credit card plays an important part of everyone's life as it is not only the safer option than carrying cash but also protects an individual from fraud or scams, where
the maximum amount of money or credit that a financial institution can lend to a credit card customer or client at once is known as the credit limit. These banks consider a number of crucial aspects when determining a client's credit limit, including income, payment history, and debts. As a result, they grant larger credit limits to lower-risk borrowers and vice versa. It is necessary to develop a system that can predict the client's credit limit based on a variety of features because the credit limit is susceptible to vary depending on the client's behavior and expenditure which could make this process challenging and time consuming.

## Scope:
The project aims to solve the regression problem by applying machine learning models to predict credit card limit.
Below is the breif overview of the project workflow:
##### 1). Loading the essential libraries and importing and reading the dataset.
##### 2). Cleaning the dataset to remove irrelevant and missing information using data cleaning and manipulation techniques.
##### 3). Visualising the dataset using graphs, charts and figures to gain better understaning of the data.
##### 4). Detecting and removing oultiers using outliers removal technique.
##### 5). Feature selection using backward elimination approach and performing transformation on response variable(credit limit).
##### 6). Applying multiple machine learning algorithms to train the models and evaluate their performance using different metrics and visualisation.

## Data Description:
The data file Credit_Card_Dataset.csv is a data set of credit card customers from a large bank. The data dictionary is given below.
| Variable | Description |
| --- | --- |
| `CLIENTNUM` | Client ID (not for analysing!) |
| `Attrition_Flag` | Whether or not the customer has left the bank in the last 12 months(**yes or no**) |
| `Customer_Age` | Age of customer in years |
| `Gender` | Gender of customer (**male or female**) |
| `Dependent_count` | Number of dependents (**children**) of the customer |
| `Education_Level` | Education level attained by the customer(**primary, secondary or third level**)|
| `Marital_Status` | **divorced, married/living with partner or single**  |
| `Income_Category` | Yearly income in Euro (to nearest 1k, grouped **<30k, 31-50k,51-70k,71-110k or 111k+**)|
| `Card_Category` | Type of credit card (**Blue or Gold**) |
| `Months_on_book` | Number of months as credit card customer |
| `Credit_Limit` | Credit card limit |
| `Avg_Utilization_Ratio` | A measure of how often the credit card is used |
| `Pay_on_time` | Whether or not the monthly balance on the credit card paid off( **yes or no**) |
|`Random_numbers`| Random Numbers |

## Importing Libraries and Data Cleaning:
Importing some essential libraries, such as data manipulation libraries that offer a wide variety of capabilities to help with a range of actions on data, such as organizing or performing mathematical operations.Similarly, data visualization libraries assist in gaining important insight into the data through various graphical representations by revealing hidden patterns and trends and data modelling librabries which helps in building different statistical or machine learning models.

<img src="https://github.com/mitalipatle/Credit-card-limit-prediction/blob/main/Images/Libraries.png" width=60% height=60%>

Importing the dataset to the notebook using the github link:

<img src="https://github.com/mitalipatle/Credit-card-limit-prediction/blob/main/Images/Importing%20dataset.png" >


Cleaning the dataset:

1). Upon exploring the dataset, it was found that the null values present in the dataset has string datatype and thus need to be converted to null values.

<img src ="">

2). 217 rows found to have missing values and thus needs to be removed using `dropna()` function.

<img src ="">
<img src ="">

3). Columns like CLIENTNUM that is unique for each customer , Random_numbers, Attrition_Flag does not add any value to credit limit analysis and thus these irrelevant columns can be dropped. 

<img src ="">

4).One duplicate value was found and dropped from the dataframe and datatypes of the features were found correct which later will need label encoding due to the presence of objects during the model fitting. 

<img src ="">

