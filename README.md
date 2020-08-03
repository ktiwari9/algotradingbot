# Algorithmic Trading

Algorithmic Trading is a tool for automating the trading process by executing the orders when pre-programming trading conditions are met.

## Why algorithmic trading?
If you are one of the old school folks, you would have been in the investing and trading game for long enough that most of the process would have become muscle memory. But, have you considered the possibility of having a bot automate it all?

Why, you ask? Well, here are some of many benefits:
1. It frees up your own bandwidth so you can do matters the most to you ( Trading and Investing also matters but I am referring to social life and other facets of life).
2. Often trading decisions are biased by emotions- both, yours and that of fellows in the market. E.g., if a new product is launched and it gets bad reviews. Slowly, this tends towards becoming a common consensus amongst the masses. This would in-turn affect the perceived reputation of the company and hence (negatively) affects the stock prices. But this is all sentimental. 
3. Order execution is nearly instant and increases the chances of execution at the best possible prices. The markets move very fast and time is always of the essence in this game.
4. Reduced risk of manual errors stemming from fatigue, stress, distractions or a number of other factors should you wish to be doing this process manually.
5. You can backtest your strategies on historical data and fine tune your approach before you set out to test the waters.

## What does the algorithm encode?
The algorithm is a pre-programmed set of instructions that monitors variables such as time, price, and volume. There are several well-known strategies that investors often use and the scope of this project is to cover only the strategies for retail investors.

In other words, you may come across the term *high-frequency trading (HFT)* which is a form of algorithmic trading but involves high turnover and high order-to-trade ratios. Hence, this is better suited for investors such as banks, hedge funds and other high ticket investors.

## What stragies are covered here?
- Trading ahead of index fund rebalancing
- Pairs trading
- Delta-neutral strategies
- Arbitrage
- Mean reversion
- Scalping
- Transaction cost reduction
- Market timing
- Sentiment Analysis: This strategy predicts the trends for a particular commodity based on market sentiments stemming from top new articles.
- Moving Average Crossover
	- *Dual Moving Average Crossover*
		- The strategy here is to monitor two moving averages- one over the long-term and one over the shorter-term. When the short-term average crosses over the long-term average, it represents a good time buy. Otherwise, it represents a good time to sell.  
	- *Moving Average Convergence/ Divergence (MACD) Crossover*
		- The strategy here is to evaluate the difference between the short-term and long-term exponential moving averages. This is called MACD and when this cross over the signal, it represents a good time to buy stocks and sell otherwise.
    - *Three Moving Average Crossover*
    	- The strategy here is to evaluate short-term, mid-term and long-term exponential moving averages and compare the short to mid and mid to long-term signals to evaluate whether it is a good time to buy or sell. Thus, there are multiple cases that represent an opportune time to buy or sell when using this strategy. 


## What stock was analyzed?
For the purpose of this project, Apple stocks were analyzed. These stocks were extracted from Yahoo Finance and span a period from Oct 2006- July 2020. The CSV file (APPL.CSV) is provided in the repository.

## How to run the code?
You can either download the repository to your desktop/local machine if you have Python installed. Otherwise, you can simply click on the button that says "Open with Colab" at the very top when you open the Jupyter Notebook. 

Once you click on it, the entire notebook will open in Google Colaboratory. To access the CSV file, 

you can simply replace the following command:
```
AAPL = pd.read_csv('AAPL.csv')
```

with the following:
```
url = https://raw.githubusercontent.com/ktiwari9/algotradingbot/master/AAPL.csv?token=ABMFOHKA4GSLLP4QJTICQPK7E5RFO # customize to correct RAW file path
AAPL = pd.read_csv('url')
```

The repository must be made public to access the CSV file via a URL like this. Otherwise, for a private repository, you would need a Personal Access Token (PAT) and you can find the details on how to access the file in this case, [here](https://medium.com/towards-entrepreneurship/importing-a-csv-file-from-github-in-a-jupyter-notebook-e2c28e7e74a5).

## Aim
With this repository, the aim of the author is to help the absolute beginners who know Python programming. All the automated trading strategies described herewith are being released publicly under the [GNU GPL V3.0 license](https://github.com/ktiwari9/algotradingbot/blob/master/LICENSE). Getting to grips with the technicalities of this domain was quite a challenge for the author but he decided to use his programming skills to get to grips with it. This approach helped him greatly and thus, he is making this repository open-source. Before using, please read the **DISCLAIMER** very carefully. Use the strategies at your own risk.

# Disclaimer
This project purely meant for education purpose and for self-learning. The investors intending to use this repository and the codebases presented herewith should do so purely at their own risk. The author neither recommends any particular stock (Apple stocks used herewith were purely for example) nor any particular strategy. The aim of the author was purely to help the absolute beginners harness their programming acumen to better tame the beast of trading and investing. Any profits or losses incurred owing to the direct utilizations of the strategies described herewith are 100% sole responsibility of the end-user and the author has absolutely no role in such outcomes. So, choose wisely and think twice before lunging for anything. Stock markets can do more harm than good if you make uneducated gusses.
