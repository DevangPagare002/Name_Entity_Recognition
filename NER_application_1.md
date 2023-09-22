<h1 align="center"> Use of NER in financial wealth management/MF space </h1>

<!-- ### Here are some of the key uses of NER in the financial wealth management/MF space: -->

## 1. Market Sentiment Analysis:

    NER can extract entities related to market events, such as earnings reports, mergers and acquisitions, and economic indicators. Analyzing the sentiment associated with these entities can help wealth managers and users make informed investment decisions.

<!-- # Use case –  -->

## Problem - 

    __Peyush Bansal__ has an account in __Zerodha__. He has 5 stocks (HCLTECH, ICICIBANK, TCS, ADANIPORTS, HDFCLIFE) in his portfolio. After purchasing these stocks, he is busy in his daily life and unaware about the ongoing market sentiment around the stocks in his portfolio. He doesn’t keep a track on news about these stocks. In order to have a good idea about the market, he has to -

    - Analyze how the market is trending.

    - look at a major index’s moving average (which shows the general trend in prices over a given period).

    - pay attention to potential market-moving events.

    - Pay attention to Federal Reserve policy meetings or earnings announcements regarding to company’s sector. 

    But because of his daily schedule, he can’t keep track of all these things. As an investor, he would like to known a general rating or score about the stocks to get the overall idea about performance of his investment.

## Solution to above problem - 

    To solve this problem, We will build a solution where we will read details of the stocks in Peyush’s portfolio. Those details will include - 
        - Name of stock holder
        
        - Name of stock, etc.

    Our system will also keep a track of leading Indian and Global stock market news websites such as - 

        1. [moneycontrol.com](https://www.moneycontrol.com/)

        2. [tradingeconimics.com](https://tradingeconomics.com/)

        3. [money.reddif.com](https://money.rediff.com/news)

    Using __NER__(Name Entity Recognition) technique for above websites, we aim to identify headlines related to the companies present in Peyush’s portfolio. These articles will be flagged as __News of Interest__. We will specially keep an eye on news related to company’s major events like company merger, news about CEO or major stakeholders of company, development within industry sector, government policy about the sector, etc.

    Once we get our __News of Interest__, we will run a sentiment analysis on the news article to find the general public sentiment around those stocks. We will generate a __confidence score__ based on sentiment analysis to judge the overall sentiment. This confidence score will be shared with Peyush Bansal.

    **Advantage of sharing confidence score - **

        - Peyush gets regular update about the stock performance and market sentiment.
        - Peyush is happy as he do not have to waste his time just to get these updates.
        - Peyush will be actively involved in the overall process.
        - Peyush can take quick independent decisions based on confidence score.
  


