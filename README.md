# US-Stocks-Analysis

- Pandas : used to organize and format complex data in table structures called DataFrames.
- Pandas-datareader : used to access public financial data from the Internet and import it into Python as a DataFrame.

![image](https://user-images.githubusercontent.com/16068206/128658945-fd4fb624-53ec-4fcd-86c6-2ced1a764393.png)
![image](https://user-images.githubusercontent.com/16068206/128659026-f3670b6b-120c-45a7-b65f-96c60284cbbd.png)

## Importing data via Datareader

## Two Key measurements: Rolling Mean and Return Rate
- Rolling Mean (Moving Average) — to determine trend
- Return Deviation — to determine risk and return

## Predicting Stocks Price
### Feature Engineering
### Pre-processing & Cross Validation
- Drop missing value
- Separating the label here, we want to predict the AdjClose
- Scale the X so that everyone can have the same distribution for linear regression
- Finally We want to find Data Series of late X and early X (train) for model generation and evaluation
- Separate label and identify it as y
- Separation of training and testing of model by cross validation train test split

### Model Generation
- Simple Linear Analysis & Quadratic Discriminant Analysis
- K Nearest Neighbor (KNN)

### Evaluation

### Plotting the Prediction
