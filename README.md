
# Cognizant-AI-Virtual-Experience-Program Internship Overview 

* Built a Unified Modelling Language (UML) Diagram for business strategic planning.

* Incorporated data exploration, data cleaning & data Merging (Data Wrangling).

* Performed feature engineering & used k-fold cross validation.

* Implemented data modelling by utilizing Random Forest Regressor model for prediction.
Computed accuracy using mean absolute error (MAE).

* Performed Feature importance to check relevant features in the dataset.

* Made alluring & comprehensible presentations for the client.


## Dataset:
Worked on 3 datasets.
'Sales' Dataset consists of following details (7829 rows x 9 columns):

Looking at the output of the .info() method, I can intepret each column as follows:
1.	transaction_id = this is a unique ID that is assigned to each transaction,
2.	timestamp = this is the datetime at which the transaction was made,
3.	product_id = this is an ID that is assigned to the product that was sold. Each product has a unique ID,
4.	category = this is the category that the product is contained within
5.	customer_type = this is the type of customer that made the transaction
6.	unit_price = the price that 1 unit of this item sells for
7.	quantity = the number of units sold for this product within this transaction
8.	total = the total amount payable by the customer
9.	payment_type = the payment method used by the customer


'Sensor_stock_levels' Dataset consists of following details (7829 rows x 9 columns):
* id	
* timestamp	
* product_id	
* estimated_stock_pct

'Sensor_storage_temperature' Dataset consists of following details (7829 rows x 9 columns):
* id
* timestamp
* temperature



## Data Cleaning
After collecting the data, I needed to clean it up so that it was usable for our model. I made the following changes and created the following variables:

*	Dropping unnecessary unnamed 0 column from dataset
* The column named 'timestamp' appears to be categorical but it's a date column. So, I converted timestamp to datetime format. Created a 'hour' column for further analysis
* Merged 3 datasets appropriately into 1 dataframe
*	And made many more changes which can be viewed in the pre-processed data csv


## Exploratory Data Analysis (EDA)
Performed EDA on the cleaned data and got various insights, relationships, etc, few of them are as below.

![image](https://user-images.githubusercontent.com/112246352/197334973-1caec0e6-fd1b-47e1-97d9-52d09aad6acf.png)


![image](https://user-images.githubusercontent.com/112246352/197334980-bd221048-7f98-4636-952a-6c2a9dee1b73.png)


![image](https://user-images.githubusercontent.com/112246352/197334991-983bb625-19ac-4f5f-a3c8-e2159a9faf95.png)


![image](https://user-images.githubusercontent.com/112246352/197334999-91448297-1ad4-4775-871f-dc56fecf2b7f.png)


## Feature Engineering and Model Building

### Feature Engineering:
* Now, I have cleaned and merged data. Now I wll transform this data so that the columns are in a suitable format for a machine learning model.

* First Engineered timestamp column but it's not useful to MLmodel due to datetime datatype.

* The next column that we can engineer is the category column. In its current form it is categorical. We can convert it into numeric by creating dummy variables from this categorical column.

* Then dropped non numeric columns.


### Model Building

* I assined target variable y and independent variabes X.

* Typically, I should leave at least 20-30% of the data for testing.

* For this exercise, I have used the RandomForestRegressor model, which is an instance of a Random Forest. These are powerful tree based ensemble algorithms and are particularly good because their results are very interpretable, also applying 10 K fold stategy fpr better accuracy.

Finally obtained a graph shows features vs relative importance.
![image](https://user-images.githubusercontent.com/112246352/197336161-177763b4-eeb4-4c4e-9e8f-9ed880e96a31.png)


This feature importance visualisation tells us:
* The product categories were not that important

* The unit price and temperature were important in predicting stock

* The hour of day was also important for predicting stock 


## Model performance
The Random Forest Regression model performed on the test and validation sets. 
*	**RandomForestRegressor** : MAE = 24%



## Code and Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, numpy, sklearn, matplotlib

**Cognizant_Forage website**
https://www.theforage.com/virtual-internships
