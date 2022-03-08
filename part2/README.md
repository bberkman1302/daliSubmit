### Part 2

## Code
Here is the link to the Kaggle notebook I did my work in: https://www.kaggle.com/brendangberkman/wine-type-prediction/notebook
Here is the link to the data set: https://www.kaggle.com/brendangberkman/wine-type-prediction/data

## Metrics Used
The dataset I used has 13 variables: 12 independent variables, each measuring some chemical coponent of wine, and 1 dependent variable, whether that wine is red or white. Each one of those independent variables is suggestive of whether the wine is red or white. Because the output is binary, either red or white, I decided to use a logistic regression model. 

## Cleaning
Because the column with with the type of wine initially held values of either "red" or "white," I used pd.getDummies to convert those values to "1" or "0" in a new column labeled type_white. 

## Assumptions
In making this model, I assumed the 12 independent variables given were not correlated with each other. To test this, I analyzed the correlation between each of the independent variables, and found that there was indeed little correlation between the variables. 

I also assumed that the size of the data set (6463, 13) was large enought to build a strong model. 

## Outliers
To remove outliers, I analyzed the skew, median, and histograms of each of the independent variables. For variables that had a skew in either direction greater than 1.5, I looked to the histogram to confirm that there could be outliers. Upon doing this, I trimmed the data set to only include rows that, for each of those variables, fell in a certain quantile range that would eliminate outliers on either end of the spectrum. 

## Accuracy
Upon running the model several times, I found that the performance accuracy ranged between 98.04% and 99.46%.