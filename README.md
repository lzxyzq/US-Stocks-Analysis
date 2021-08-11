# US-Stocks-Analysis

- Pandas : used to organize and format complex data in table structures called DataFrames.
- Pandas-datareader : used to access public financial data from the Internet and import it into Python as a DataFrame.

## Importing data via Datareader

The API document : https://www.alphavantage.co/documentation/

## Two Key measurements: Rolling Mean and Logarithmic Return Rate
- Rolling Mean (Moving Average) — to determine trend
- Logarithmic Return — to determine risk and return

### Rolling mean/Moving Average (MA) 

smooths out price data by creating a constantly updated average price. This is useful to cut down “noise” in our price chart. Furthermore, this Moving Average could act as “Resistance” meaning from the downtrend and uptrend of stocks you could expect it will follow the trend and less likely to deviate outside its resistance point. -- window=100

![image](https://user-images.githubusercontent.com/16068206/128924172-f08199e8-1a52-4941-b31d-9116c1eaa30d.png)

The Moving Average makes the line smooth and showcase the increasing or decreasing trend of stocks price.

### Advantages of logarithmic return:

The equation for calculating the log return between two prices is as follows natural_log(current price/previous price)
```
def log_return(prices):
     return np.log(prices / prices.shift(1))
```
- The use of logarithmic returns prevents investment prices in models from becoming negative.
- Logarithmic Returns KERNEL PDF ESTIMATION(Probability Density Function)
![image](https://user-images.githubusercontent.com/16068206/128658945-fd4fb624-53ec-4fcd-86c6-2ced1a764393.png)
- Logarithmic Returns KERNEL CDF ESTIMATION(Cumulative Distribution Function)
![image](https://user-images.githubusercontent.com/16068206/128659026-f3670b6b-120c-45a7-b65f-96c60284cbbd.png)

## Analysing Competitors Stocks
- Analyse on how one company performs in relative with its competitor.
### Correlation Analysis
- Plot Apple and GE with Scatter-Plot to view their Logarithmic Returns distributions.
![image](https://user-images.githubusercontent.com/16068206/128937790-da5438df-6b73-4c77-91b6-2a8f5ec77be3.png)

There are slight positive correlations among GE logarithmic return and Apple logarithmic return. It seems like that the higher the Apple logarithmic return, the higher GE logarithmic return as well for most cases.

![image](https://user-images.githubusercontent.com/16068206/128953959-323af1bb-7344-4727-a24a-12312081141e.png)

- At the diagonal point, we will run Kernel Density Estimate (KDE). KDE is a fundamental data smoothing problem where inferences about the population are made, based on a finite data sample. It helps generate estimations of the overall distributions.
- we could see most of the distributions among stocks which approximately positive correlations.

![image](https://user-images.githubusercontent.com/16068206/128954159-605a94f3-d0fb-49f9-b04f-e05a5fd541d7.png)

- To prove the positive correlations, Use heat maps to visualize the correlation ranges among the competing stocks. Notice that the lighter the color, the more correlated the two stocks are.

### Stocks Returns and Risk

Analyse each stock’s risks and logarithmic return. In this case we are extracting the average of logarithmic return and the standard deviation of logarithmic return (Risk).

![image](https://user-images.githubusercontent.com/16068206/128956266-435d0e4e-e7aa-41c6-9578-b49d84142079.png)

I would like to minimize the risk and maximize returns. Therefore, I would like to draw the line for risk-return tolerance. Create the rules what stocks to buy and sell.

## Predicting Stocks Price
Use three machine learning models to predict stocks: 
- Simple Linear Analysis
- Quadratic Discriminant Analysis (QDA)
- K Nearest Neighbor (KNN).
### Feature Engineering

### Simple Linear Analysis & Quadratic Discriminant Analysis
- Simple Linear Analysis shows a linear relationship between two or more variables. When we draw this relationship within two variables, we get a straight line.
- Quadratic Discriminant Analysis would be similar to Simple Linear Analysis, except that the model allowed polynomial (e.g: x squared) and would produce curves.
### K Nearest Neighbor (KNN)
- This KNN uses feature similarity to predict values of data points. This ensures that the new point assigned is similar to the points in the data set.

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

### Plotting the Prediction

![image](https://user-images.githubusercontent.com/16068206/128968246-a11a07ce-e7d7-45f3-ac39-c0c68b54c189.png)

### Future Improvements/ Challenges
- Analyse economic qualitative factors such as news (news sourcing and sentimental analysis)
