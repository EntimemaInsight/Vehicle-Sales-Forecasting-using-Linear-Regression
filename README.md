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
This section explains the steps taken to preprocess the dataset used in the project. Data preprocessing is a critical step in the data analysis pipeline, as it ensures that the data is ready for use in the linear regression model.

The dataset used in the project contained missing values and outliers, which were dealt with using various techniques. The steps taken to preprocess the dataset are as follows:

1. Exploring the descriptive statistics of the variables: Descriptive statistics such as mean, standard deviation, and quartiles were calculated for each variable in the dataset. This step provided an overview of the range and distribution of each variable and helped to identify any potential issues with the data.
2. Determining the variables of interest: The variable "Model" was dropped from the dataset, as it was not relevant to the analysis.
3. Dealing with missing values: The number of missing values in each variable was calculated, and rows with missing values were dropped from the dataset. This step ensured that the remaining data was complete and could be used in the linear regression model.
4. Exploring the probability density functions (PDFs): PDFs were used to visualize the distribution of each variable in the dataset. This step helped to identify potential issues such as non-normality or outliers.
5. Dealing with outliers: Outliers were removed based on quantiles. This step ensured that extreme values did not bias the linear regression model.
6. Relaxing the assumptions: The OLS assumptions were checked, and the variables were transformed to better fit the linear regression assumptions. The variable "Price" was transformed using a logarithmic transformation, as the relationship between the independent variables and the dependent variable was not linear.
7. Dealing with multicollinearity: Multicollinearity was checked using variance inflation factors (VIFs), and the variable "Year" was dropped from the dataset to mitigate the issue.
8. Creating dummy variables: Dummy variables were created for categorical variables to ensure that they could be used in the linear regression model.
9. Rearranging the dataset: The preprocessed dataset was rearranged so that the dependent variable "Price" was at the beginning of the dataset and the independent variables followed.

# Exploratory Data Analysis
This section explains the exploratory data analysis (EDA) techniques used to gain insights into the dataset and identify any potential issues with the data. EDA is an important step in the data analysis pipeline, as it helps to guide further preprocessing and modeling decisions.

The dataset used in the project contained variables such as vehicle brand, mileage, engine type, and registration status. Descriptive statistics, probability density functions (PDFs), and scatterplots were used to explore the data and gain insights into the relationships between variables.

Descriptive statistics such as mean, standard deviation, and quartiles were calculated for each variable in the dataset. This step provided an overview of the range and distribution of each variable and helped to identify any potential issues with the data.

PDFs were used to visualize the distribution of each variable in the dataset. This step helped to identify potential issues such as non-normality or outliers. For example, the PDF of the variable "Price" showed that the data was right-skewed, indicating that a transformation may be needed to better fit the linear regression assumptions.

Scatterplots were used to visualize the relationships between variables. For example, scatterplots were used to explore the relationship between "Year" and "Price", "EngineV" and "Price", and "Mileage" and "Price". These scatterplots were used to check for linearity and to identify any potential issues with heteroscedasticity.

In addition to these techniques, dummy variables were created for categorical variables to ensure that they could be used in the linear regression model. VIFs were used to check for multicollinearity, and the variable "Year" was dropped from the dataset to mitigate the issue.

By using these EDA techniques, potential issues with the data were identified and addressed, ensuring that the preprocessed dataset was ready for use in the linear regression model. These techniques also provided insights into the relationships between the independent variables and the dependent variable, guiding further modeling decisions.

# Linear Regression Modeling
This section explains the steps taken to build and evaluate the linear regression model used in the project. Linear regression is a widely used method for modeling the relationships between a dependent variable and one or more independent variables.

The preprocessed dataset was split into training and testing datasets using the train_test_split() function from the sklearn.model_selection library. The independent variables were standardized using the StandardScaler() function from the sklearn.preprocessing library to ensure that each variable had equal weight in the model.

The LinearRegression() function from the sklearn.linear_model library was used to create the linear regression model. The model was trained on the training dataset using the fit() method and used to predict the dependent variable values for the testing dataset using the predict() method.

The performance of the linear regression model was evaluated using several metrics. The R-squared value, which represents the proportion of variance in the dependent variable that can be explained by the independent variables, was calculated using the score() method. The closer the R-squared value is to 1, the better the model fits the data.

The weights and bias of the linear regression model were also calculated using the coef_ and intercept_ attributes, respectively. These values represent the slope and intercept of the regression line and can be used to make predictions for new data.

The predictions made by the linear regression model were compared to the actual values in the testing dataset to evaluate the accuracy of the model. The predictions and actual values were plotted using a scatterplot to visualize the relationship between them.

Finally, the difference between the predictions and actual values, or the residuals, were calculated and used to evaluate the performance of the model. The residuals were plotted using a histogram and a normal probability plot to check for normality and ensure that the model was not biased towards certain values.

By following these steps, a linear regression model was built and evaluated on the preprocessed dataset. The performance of the model was evaluated using several metrics and visualizations, ensuring that the model was accurate and could be used to gain insights into the relationships between the independent variables and the dependent variable.

