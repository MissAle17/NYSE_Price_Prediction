# NYSE_Price_Prediction
Using Machine learning to predict future stock prices.


## New York Stock Exchange

Long have analysts, traders, and investors tried to predict future stock prices. Even if you come up with a plan or model that works for a while, it is generally great until for some reason it doesn't work. Whether there was a break down in underlying correlations or new news of scandal caused stock prices to plummet. If you could crack the whole code you'd be a billionaire in about the same amount of time as it takes to click on your favorite Netflix program. 

If any type of model is going to be able to finally do it, I would be willing to bet that model would fall into the deep learning category. So that is exactly what we are going to try to do.  Additionally, through the course of the analysis I will answer another question: how much of today's closing price can be explained using previous closing prices of the same stock?  


### The Data
The data set we will be working with is from the New York Stock Exchange (NYSE) and represent the historical prices and other fundamental data points of the S&P 500 from 2010 to the end of 2016.  The original dataset can be found on [Kaggle](https://www.kaggle.com/dgawlik/nyse)


### The Process

This project is being completed to statisfy the fourth project requirement for the Data Science bootcamp at the Flatiron School.  In General, we will follow the Data Science process, Cleaning, Exploring, and Analyzing iteratively until we arrive at a useable model.  

Begining with exploration, there are a number of visualizations I created for exploratory purposes.  For example, based on the below graph, the cheapest stock in the S&P 500 had a low of 1.50 per share and the most expensive stock for this time frame was 1,600.93 per share. Other than volume, we can see how the other metrics might be a little skewed given the standard deviation is actually greater than the mean price. With one stock trading at 1.50 and another over 1,600, that's not really comparing apples to apples!
![volume]("Price_Prediction/images/Abs_vol.png")

