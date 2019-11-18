# Soybean Price Prediction / Winning solution / MinneAnalytics Data Science Challenge

## The Challenge

The [MinneAnalytics 2019 challenge](http://minneanalytics.org/minnemudac/) involved forecasting Soybean futures so as to help local soy farmers make informed decisions about when to sell their crops. A decision on what price to sell at, especially in the volatile market of 2019, is critical. Our work involved collecting data including but not limited to **commodity prices, financial indexes, Google News trends, and tweets of policy makers**. This was followed by an extensive implementation of predictive modeling methods including **ensemble methods and recurrent neural networks**. Our model achieved a prediction error of ~5.6 cents (< 1%).

![1574100030540](https://github.com/guptapiyush340/Soybean-Price-Prediction---MinneMUDAC-winning-solution/blob/master/1.png)

More than 100 teams presented at the Optum Technology Center in Minneapolis on November 9th and our team was awarded first place in the Graduate Student division. 

Team: [Harsh Seksaria](https://www.linkedin.com/in/harsh-seksaria/), [Piyush Gupta](https://www.linkedin.com/in/piyushguptads/), [Hamed Khoojinian](https://www.linkedin.com/in/hamedian/), [Yassine Manane](https://www.linkedin.com/in/yassine-manane/), [Pushkar Vengulekar](https://www.linkedin.com/in/pvengurlekar/)


<blockquote class="twitter-tweet" data-conversation="none"><p lang="en" dir="ltr">Congratulations to <a href="https://twitter.com/CarlsonNews?ref_src=twsrc%5Etfw">@CarlsonNews</a> for taking home First Prize in the Graduate division <a href="https://twitter.com/hashtag/MinneMUDAC?src=hash&amp;ref_src=twsrc%5Etfw">#MinneMUDAC</a> <a href="https://t.co/t6AJMA40jM">pic.twitter.com/t6AJMA40jM</a></p>&mdash; MinneAnalytics (@MinneAnalytics) <a href="https://twitter.com/MinneAnalytics/status/1195404197602054144?ref_src=twsrc%5Etfw">November 15, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


Winner across divisions - http://minneanalytics.org/announcing-the-winners-of-the-minnemudac-2019-student-data-science-challenge/

## Process Overview

### Data Collection

We are as much commodity traders as we are farmers, so first we went looking at peer reviewed journals for expert research. We came away with the understanding that prices and their interactions were the most important category of data sources we could consider, So starting from the most important price: the price of recent soybean futures, we added other prices we felt important. We added metrics to capture the behavior, and instability, of traders and the exchange itself as well as social media and news trends to capture public sentiment. 

![1574100207862](https://github.com/guptapiyush340/Soybean-Price-Prediction---MinneMUDAC-winning-solution/blob/master/3.png)

### Machine Learning Journey

**We experimented with multiple prediction algorithms**

1. [ARIMA](https://github.com/guptapiyush340/Soybean-Price-Prediction-Winning-solution-MinneAnalytics-Data-Science-Challenge/blob/master/ARIMA.ipynb)
2. [Prophet](https://github.com/guptapiyush340/Soybean-Price-Prediction-Winning-solution-MinneAnalytics-Data-Science-Challenge/blob/master/Prophet.ipynb)
3. [XGBoost](https://github.com/guptapiyush340/Soybean-Price-Prediction---MinneMUDAC-winning-solution/blob/master/MinneMUDAC%20Final%20Model%20-%20XGBoost%20with%20Hyper-parameter%20tuning.ipynb)
4. [LSTM](https://github.com/guptapiyush340/Soybean-Price-Prediction-Winning-solution-MinneAnalytics-Data-Science-Challenge/blob/master/LSTM.ipynb)
5. [Seq2Seq](https://github.com/guptapiyush340/Soybean-Price-Prediction-Winning-solution-MinneAnalytics-Data-Science-Challenge/blob/master/Seq2Seq.ipynb)

The three approaches - XGBoost, LSTM and Seq2Seq are really good and give comparable performance. But as per our research Neural Networks need lot of data to train with which we don’t have for this problem statement. 

In addition to this, our focus was on generating insights along with predictions, so we decided to finalize with XGBoost because it provides interpretation in terms of feature importance. 

![1574100414202](https://github.com/guptapiyush340/Soybean-Price-Prediction---MinneMUDAC-winning-solution/blob/master/4.png)

**Most Important Features**

![1574100723594](https://github.com/guptapiyush340/Soybean-Price-Prediction---MinneMUDAC-winning-solution/blob/master/5.png)

### Profitability for the farmer

Let’s say farmer Joe has to sell 6400 bushels of soybean. He could make the decision of holding or selling the futures based on his intuition of looking at the previous trend, or he could use our analysis. 

On the 4th, our model recommends him to sell the bushels as the price would drop the next day, and it did!  For each day of the week last week, the farmer could have profited by making a SELL or HOLD decision using our Machine Learning approach and saved $372 on an average.

![1574100794635](https://github.com/guptapiyush340/Soybean-Price-Prediction---MinneMUDAC-winning-solution/blob/master/6.png)

In a volatile market, a data driven SELL or HOLD decision could have saved the farmer $7366 dollars!

![1574100879786](https://github.com/guptapiyush340/Soybean-Price-Prediction---MinneMUDAC-winning-solution/blob/master/7.png)
