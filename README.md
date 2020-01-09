# NYSE_Price_Prediction

Using Machine learning to predict future stock prices.

## New York Stock Exchange

Long have analysts, traders, and investors tried to predict future stock prices. Even if you come up with a plan or model that works for a while, it is generally great until for some reason it doesn't work. Whether there was a break down in underlying correlations or new news of scandal caused stock prices to plummet. If you could crack the whole code you'd be a billionaire in about the same amount of time as it takes to click on your favorite Netflix program.

If any type of model is going to be able to finally do it, I would be willing to bet that model would fall into the deep learning category. So that is exactly what we are going to try to do. Additionally, through the course of the analysis I will answer another question: how much of today's closing price can be explained using previous closing prices of the same stock?

### The Data

The data set we will be working with is from the New York Stock Exchange (NYSE) and represent the historical prices and other fundamental data points of the S&P 500 from 2010 to the end of 2016. The original dataset can be found on Kaggle

I chose to take an in depth look at one stock, Google ("GOOG"), comparing it to its competitiors, and ultimately using its prices and a the only input variable over time in my models. Ultimately, I ended up at a model that explained more than a whole percentage point of price variation. I was very pleased with the outcome as I expected that the prices would explain even less. There will be further discussion after my explanation of the models used.

### The Process

This project is being completed to statisfy the fourth project requirement for the Data Science bootcamp at the Flatiron School. In General, we will follow the Data Science process, Cleaning, Exploring, and Analyzing iteratively until we arrive at a useable model.

Begining with exploration, there are a number of visualizations I created for exploratory purposes. For example, based on the below graph, the cheapest stock in the S&P 500 had a low of 1.50 per share and the most expensive stock for this time frame was 1,600.93 per share. Other than volume, we can see how the other metrics might be a little skewed given the standard deviation is actually greater than the mean price. With one stock trading at 1.50 and another over 1,600, that's not really comparing apples to apples! 

![volume]('Price_Prediction/images/Abs_vol.png)

Another interesting visual is a graph of the January effect. I chose to take a look at January 2015 and plotted the total trade volume by stock on each Friday in January. A pattern that I want to point out is the last Friday (and business day) of the month has the most volume. 

![january]('Price_Prediction/images/jan_effect.png')

## Google and the Tech Giants

At this point in the analysis I turn to Google and the other tech giants, Google's industry comparables. The first visual I created, shows 200 days of Google's opening price vs. Google's closing price. Generally, stocks close the day at a price that is near the open price. Here, though you can see some big changes during a few of these days. Often it's a day where there was big news regarding the company that either beat or fell short of expectations. This news can be anything from announcing a long rumored product to hit the shelves to financial reporting to something industry wide, like tariffs on a particular part for a product.

![google open close]('Price_Prediction/images/goog_o_c.png')

I did the same for Microsoft and Apple with the Google prices for the same day. Companies in the same sector, that are considered comparable, often react to the same news - including big changes to their competitors prices. Additionally, I reviewed these three companies' trade volume for the same period.

![g_m_a]('Price_Prediction/images/g_m_a_volume.png')

Both of these visualizations clearly show that the vast majority of the stocks trade in similar volumes and then outside of that we have those mega-stocks with wild daily trading activity. The daily volume tells us a few things. Firstly the size of the company, those outliers are multinational conglomerates who have had very large issuances and likely also a number of stock splits. Big companies don't often fail quickly; they have also often acheived 'cash cow' status. These factors make them attractive to the risk-averse investor (like institutional pension funds). Depending on industry trade winds, like those our 'FAANG' companies (Facebook, Apple, Amazon, Netflix and Google) are facing now, it can also be a signal that these companies may be subject to anti-trust legal action. Really it's up to the industry analyst to know about these sorts of things before making any recomendations.