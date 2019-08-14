### Travis Status:
[![](https://travis-ci.org/ubco-mds-2018-labs/data533_lab4_Bindu_Wei.svg?branch=master)](https://travis-ci.org/ubco-mds-2018-labs/data533_lab4_Bindu_Wei)



Collaborative Software Development - Create Python Package.  

## Group Members:

__Bindu Joopally__, __Wei Tang__      

### Topic: Visualization 

Goal: To develop python functions to create graphs which help in variable selection after model fit. 

Given the data with predictors and response variable, the generated output will help to analyse the effect of each variable on the response through visualization and also to visualize correlation between variables and smooth line with quadratic spline algorithm. 

### Brief description of package contents:

This package contains two subpackages:

**1. With-without Analysis (Created by Bindu):**

This subpackage contains two functions:

- __create_buckets__: 

Inputs:   

A list with numeric values, number of buckets(has default value)

Outputs:   

A list with bucket number corresponding to each value in the input list 


- __addone__:
(uses inheritance from create_buckets function)

Inputs:  
A pandas dataframe, a list containing names of predictor variables, name of the response variable

Outputs:  
A graph for each predictor containing its bucket on the x-axis, the lines showing the linear regression model fit with and with-out the variable and the true value of response variable. 


**2. Subpackage Two (Created by Wei):**

This subpackage contains two functions:

- __correlation__:

Inputs:  
A pandas dataframe, a list containing names of variables among which user wants to see the correlation.(defaults to all)

Outputs:  
A heatmap with colors showing the extent of correlation between each pair of variables given in inputs. 

- __smoothing__: (uses inheritance)

Inputs:  
A pandas dataframe, a list containing names of predictor variables, name of the response variable

Outputs:  
A graph  

## Dependencies: 
`matplotlib`, `numpy`, `pandas`


Note: 
100% coverage could not be achieved as the functions are producing graphs for different ranges of numeric values in the data using if-else statements. But the test datasets used to cover all these conditions(especially edge cases) could not be found. The data satisfying each of the conditions can be simulated but it is a time-consuming process.
