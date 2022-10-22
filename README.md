# Cognizant-AI-Virtual-Experience-Program
Cognizant-AI-Virtual-Experience-Program
Enrolled in 'Artificial Intelligence Virtual Experience Program' by Cognizant as a 'Data Scientist' with affiliation to Forage. Worked on a business problem statement with 'Gala Groceries' by implementing Exploratory Data Analysis (EDA), Data Modeling, Model Building and Interpretation, Machine Learning Production & Quality Assurance. Also, gained insights for optimizing the required business problem while contributing recommendations for the given business problem.

Built a Unified Modelling Language (UML) Diagram for business strategic planning.
Incorporated data exploration, data cleaning & data Merging (Data Wrangling).
Performed feature engineering & used k-fold cross validation.
Implemented data modelling by utilizing Random Forest Regressor model for prediction.
Computed accuracy using mean absolute error (MAE).
Performed Feature importance to check relevant features in the dataset.
Made alluring & comprehensible presentations for the client.


Exploratory Data Analysis (EDA)
After collecting the data, EDA is performed using Python (Jupiter Notebook and google colab) and its libraries such as pandas, numpy, seaborn, etc . Brief information aobut this task as below.

Dataset consists of following details:
Data columns (total 9 columns):

Looking at the output of the .info() method, we can intepret each column as follows:
1.	transaction_id = this is a unique ID that is assigned to each transaction,
2.	timestamp = this is the datetime at which the transaction was made,
3.	product_id = this is an ID that is assigned to the product that was sold. Each product has a unique ID,
4.	category = this is the category that the product is contained within
5.	customer_type = this is the type of customer that made the transaction
6.	unit_price = the price that 1 unit of this item sells for
7.	quantity = the number of units sold for this product within this transaction
8.	total = the total amount payable by the customer
9.	payment_type = the payment method used by the customer





Visualisation
I looked at the distributions of the data and value counts for various categorical variables. Below are some visualizations from EDA.

![image](https://user-images.githubusercontent.com/112246352/197334973-1caec0e6-fd1b-47e1-97d9-52d09aad6acf.png)


![image](https://user-images.githubusercontent.com/112246352/197334980-bd221048-7f98-4636-952a-6c2a9dee1b73.png)


![image](https://user-images.githubusercontent.com/112246352/197334991-983bb625-19ac-4f5f-a3c8-e2159a9faf95.png)


![image](https://user-images.githubusercontent.com/112246352/197334999-91448297-1ad4-4775-871f-dc56fecf2b7f.png)


The column named 'timestamp' appears to be categorical but it's a date column. So, I converted timestamp to datetime format. Created a 'hour' column for further analysis.








Data Modeling, Model Building and Interpretation, Machine Learning Production & Quality Assurance:

After EDA, Model building performed using Python (Jupiter Notebook and google colab) and its libraries such as pandas, numpy, sci-kit learn, etc on datasets provided. Brief information aobut this task as below.

1. Data cleaning:
Now, 3 datasets successfully loaded, we need to ensure that the data is clean. Data cleaning can be a very intense task, so for this exercise, we will focus just on ensuring that the correct datatypes are present for each column, and if not, correcting them.

Everything looks fine for the 3 datasets apart from the timestamp column in each dataset. Using the same helper function as before, converted this to the correct type for each dataset.



2. Merge Data
Currently we have 3 datasets. In order to include all of this data within a predictive model, we need to merge them together into 1 dataframe.The client indicates that they want the model to predict on an hourly basis. Looking at the data model, we can see that only column that we can use to merge the 3 datasets together is timestamp.

So, we must first transform the timestamp column in all 3 datasets to be based on the hour of the day, then we can merge the datasets together.


3. Feature Engineering:
Now, I have cleaned and merged data. Now I wll transform this data so that the columns are in a suitable format for a machine learning model.

First Engineered timestamp column but it's not useful to MLmodel due to datetime datatype.

The next column that we can engineer is the category column. In its current form it is categorical. We can convert it into numeric by creating dummy variables from this categorical column.

Then dropped non numeric columns.




4. Modelling
I assined target variable y and independent variabes X.

Typically, I should leave at least 20-30% of the data for testing.

For this exercise, I'm going to use a RandomForestRegressor model, which is an instance of a Random Forest. These are powerful tree based ensemble algorithms and are particularly good because their results are very interpretable, also applying 10 K fold stategy fpr better accuracy.

Finally, I got the accuracy in terms of Average Mean Absolute Error(MAE)=24%


Finally obtained a graph shows features vs relative importance.
![image](https://user-images.githubusercontent.com/112246352/197336161-177763b4-eeb4-4c4e-9e8f-9ed880e96a31.png)


This feature importance visualisation tells us:

The product categories were not that important

The unit price and temperature were important in predicting stock

The hour of day was also important for predicting stock





Resources Used:
https://www.theforage.com/virtual-internships
