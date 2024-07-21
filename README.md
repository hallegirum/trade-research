Machine Learning Project

The first part of the code is creating descriptive statistics. Like a graph of the change in GDP, GDP per capita, imports and exports over time as well as the mean of these variables in each country is also plotted on a histogram. I also have to clean the data, and get rid of ceritain rows that are descriptions.
The second part of the code is creating the PCA variables. I use a standardizer to make sure the data is comparable and an imputer so that the PCA can handle missing values. I have two PCA constructed indexes one is the first principle component of exports and imports, the second index is the first principle componet of the tarrif data, and exports and imports. My last index is the traditional exports + imports/ GDP measure.

I also create dummy varaibles and split my data into training and testing sets in preperation of running a LASSO and OLS regression.

I create my lagged variables which are GDP growth and GDP per capita growth in t+1

I run Lasso regressions for each of the three trade openness indexes along with the control variables for both lagged GDP growth and lagged GDP per capita growth as the dependent variables.

I use grid search CV to run my Lasso regressions and use a for loop to validate that alpha score and plot graphs of Mean squared error vs lasso penalty term for each Lasso regression

I use the features selected in the Lasso regression to run OLS regressions for all the indexes paired with GDP growth and GDP per capita growth
The data folder in the repo holds all the csv files I used for my dataframes: the inputs file which are my control variables, the outputs file which are my dependent variables, the tarrifs which has my tarrif data for the trade openness index, and the trade openness index file which is the conventional measure of trade openness
