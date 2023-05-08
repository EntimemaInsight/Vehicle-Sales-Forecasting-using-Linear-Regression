# Vehicle-Sales-Forecasting-Linear-Regression-Python-Model
This project uses linear regression to forecast the sales price of vehicles based on various features such as mileage, engine volume, brand, body type, and more. The dataset used in this project is taken from a CSV file containing information on used cars sold in the European market.

# Installation
Python 3.6+
Jupyter Notebook
Required packages can be installed using pip install -r requirements.txt

# Usage
1. Open the Jupyter Notebook file Vehicle Sales Price Forecasting using Linear Regression.ipynb
2. Run each cell in order to import libraries, preprocess data, perform exploratory data analysis, build the model, and evaluate its performance.
3. Make sure to adjust the file path to the CSV data file accordingly.

# Data Preprocessing
1. This section explains the steps taken to preprocess the dataset used in the project. Data preprocessing is a critical step in the data analysis pipeline, as it ensures that the data is ready for use in the linear regression model.
2. The dataset used in the project contained missing values and outliers, which were dealt with using various techniques. The steps taken to preprocess the dataset are as follows:
3. Exploring the descriptive statistics of the variables: Descriptive statistics such as mean, standard deviation, and quartiles were calculated for each variable in the dataset. This step provided an overview of the range and distribution of each variable and helped to identify any potential issues with the data.
4. Determining the variables of interest: The variable "Model" was dropped from the dataset, as it was not relevant to the analysis.
5. Dealing with missing values: The number of missing values in each variable was calculated, and rows with missing values were dropped from the dataset. This step ensured that the remaining data was complete and could be used in the linear regression model.
6. Exploring the probability density functions (PDFs): PDFs were used to visualize the distribution of each variable in the dataset. This step helped to identify potential issues such as non-normality or outliers.
7. Dealing with outliers: Outliers were removed based on quantiles. This step ensured that extreme values did not bias the linear regression model.
8. Relaxing the assumptions: The OLS assumptions were checked, and the variables were transformed to better fit the linear regression assumptions. The variable "Price" was transformed using a logarithmic transformation, as the relationship between the independent variables and the dependent variable was not linear.
9. Dealing with multicollinearity: Multicollinearity was checked using variance inflation factors (VIFs), and the variable "Year" was dropped from the dataset to mitigate the issue.
10. Creating dummy variables: Dummy variables were created for categorical variables to ensure that they could be used in the linear regression model.
11. Rearranging the dataset: The preprocessed dataset was rearranged so that the dependent variable "Price" was at the beginning of the dataset and the independent variables followed.
