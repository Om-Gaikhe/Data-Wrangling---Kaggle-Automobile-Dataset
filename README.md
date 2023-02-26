# Data-Wrangling---Kaggle-Automobile-Dataset
This is data science project that focuses on data wrangling of the Automobile dataset sourced from Kraggle. 

## Data Wrangling
The procedure for data wrangling involves various steps.This can include handling missing data, correcting data formats, standardizing and normalizing data, binning and creating indicator variables. 
First, missing values are handled by replacing the "?" symbol with NaN and evaluating for any more missing data. The missing data is then dealt with by either dropping the entire row or replacing it with mean or frequency values. Data format is then corrected by converting data types to their proper format. 

## Standardization
It involves transforming data into a common format, allowing for meaningful comparison.
Standardization is performed on fuel consumption columns to transform mpg into L/100km. In my dataset, the fuel consumption columns "city-mpg" and "highway-mpg" are represented by mpg (miles per gallon) unit. Assume we are developing an application in a country that accepts the fuel consumption with L/100km standard. We will need to apply data transformation to transform mpg into L/100km. The formula for unit conversion is: L/100km = 235.215 / mpg.

## Normalization
Normalization is another technique used in data wrangling that involves transforming values of several variables into a similar range. It is also applied to variables such as "length", "width" and "height" by scaling them to a value range of 0 to 1. Normalized these variables so their value ranges from 0 to 1. Approach: replace original value by (original value)/(maximum value)
 
## Binning
It is a process of grouping continuous numerical variables into discrete categories for easier analysis. This can be particularly useful when analyzing large datasets with a high number of unique values. Binning is used to transform continuous numerical variables into discrete categorical "bins". In this dataset "horsepower" is a real valued variable ranging from 48 to 288 and it has 57 unique values. What if we only care about the price difference between cars with high horsepower, medium horsepower, and little horsepower (3 types)? Can we rearrange them into three ‘bins' to simplify analysis? I used the pandas method 'cut' to segment the 'horsepower' column into 3 bins.
Bins Visualization - Here, I visualized the bins created above to see there distributions

## Dummy Variables 
Finally, indicator variables or dummy variables are used to convert categorical variables into numerical values for regression analysis.
