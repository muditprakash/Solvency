
# Loan prediction app 

This mini project addresses a classic use case in the banking sector: deciding whether to grant a loan to a customer based on various parameters. The app takes input data and uses a machine learning classification algorithm to assist banks in making informed decisions about lending money to a particular customer.

# Technical diagram and explaination

This diagram shows the number of steps involved in the development of this app.

![Capture](https://github.com/muditprakash/loan_approval_prediction_app/assets/75181670/72be6db2-9eaf-4afd-ade6-c317a8f5d300)


#### Saved Data

The data used in the creation of the app consists of two CSV files named "train" and "test." The training set has 464 rows and 13 columns, while the test dataset has 123 rows and 13 columns.

#### Data Preprocessing

In this step, we changed some of the columns' data types and identified and treated null values.

#### EDA

We used different libraries like Matplotlib and Seaborn to visualize the data and studied the relationships between various columns and our predictor variable.

#### Feature Engineering

We converted all categorical variables into numerical ones using the one-hot encoding method.

#### Train-Test Split

We split the data with a ratio of 70% for training the model and 30% for testing the model's performance.

#### Model Development

We used the XGBoost model for this task, employing methods like k-fold cross-validation and grid search CV to train the model and obtain the best performance parameters.

#### Model Validation

We used the validation dataset to test the model's performance. Our aim is to achieve at least 80% accuracy. If the model fails to meet this threshold, we will reiterate the model development process.

#### Model Deployment

Once validation is complete, we save the model using the pickle method. Although we are saving the model locally, we plan to deploy and test the model on the cloud. We establish a connection with the cloud, install the necessary requirements, and test the model there.

#### Model Serving

Once the model is deployed, we need to determine how users can interact with it. We use Flask API for this purpose.

## Running it locally

To run this project locally first clone this repo

```bash
  git clone https://github.com/muditprakash/loan_approval_prediction_app.git
```
Once this is done install requirements.txt file as 

```
pip install -r requirements.txt

```

And then run app.py file as 

```
python app.py

```

Once done you will see a UI powered by flask running inyour browser something like this : 

![app](https://github.com/muditprakash/loan_approval_prediction_app/assets/75181670/8eadd0e4-7e2f-4e9b-bfb7-7a677afb179f)

And once you filled the suitable information you will see the result like this : 

![prediction](https://github.com/muditprakash/loan_approval_prediction_app/assets/75181670/4fe457fa-2a57-4ed3-be8c-eb1e975bafa1)


