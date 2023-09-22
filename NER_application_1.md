<h1 align="center"> Use of NER in financial wealth management/MF space </h1>

<!-- ### Here are some of the key uses of NER in the financial wealth management/MF space: -->

## 1. Market Sentiment Analysis:

    NER can extract entities related to market events, such as earnings reports, mergers and acquisitions, and economic indicators. Analyzing the sentiment associated with these entities can help wealth managers and users make informed investment decisions.

<!-- # Use case –  -->

## A. Problem - 

__Peyush Bansal__ has an account in __Zerodha__. He has 5 stocks (HCLTECH, ICICIBANK, TCS, ADANIPORTS, HDFCLIFE) in his portfolio. After purchasing these stocks, he is busy in his daily life and unaware about the ongoing market sentiment around the stocks in his portfolio. He doesn’t keep a track on news about these stocks. In order to have a good idea about the market, he has to -

- Analyze how the market is trending.

- look at a major index’s moving average (which shows the general trend in prices over a given period).

- pay attention to potential market-moving events.

- Pay attention to Federal Reserve policy meetings or earnings announcements regarding to company’s sector. 

But because of his daily schedule, he can’t keep track of all these things. As an investor, he would like to known a general rating or score about the stocks to get the overall idea about performance of his investment.

## B. Solution to above problem - 

## B1
To solve this problem, We will build a solution where we will read details of the stocks in Peyush’s portfolio. Those details will include - 

- Personal information:
  - Full name of stock holder
  - Date of Birth
  - Gender
  - Permanent address
  - Contact information (phone number, email address)

- Identification documents:
  - PAN number
  - Aadhaar number (Or any other gov. ID)
<!--        
- Bank account details
  - Bank name
  - Bank account number
  - IFSC code

- Demat account details 
  - Trading account number
  - Demat account number

- Income information
- Trading history
- KYC status -->
- Company information:
  - Company profile
  - Company financial statement
  - Management team
  - Corporate actions

## B2

In order to get the information mentioned in __B1__, there are some ways we thought -

- Brokers might have an __API__ available which can be used to fetch data from their database. List of some brokers with their API's - 
  - __Zerodha__: [Kite API](https://kite.trade/startups/) 
  - __Upstox__: [Upstox API](https://upstox.com/developer/api-documentation/)
  - __Angel One__: [Smart API](https://www.angelone.in/knowledge-center/smartapi/detailed-introduction-to-smartapi)
  - __ICICI Direct__: [Breeze API](https://api.icicidirect.com/apiuser/home)
  - __Sharekhan__: [Sharekhan API](https://www.sharekhan.com/trading-api)
  - __NSE(National stock exchange)__: [NSE/BSE Share market API](https://upstox.com/uplink/) (github - https://github.com/hi-imcodeman/stock-nse-india)

- Data Sharing agreement with brokers.
- If we can't get company data, then we can explicitly prepare a script to scrape the data about company through company's official website.
-  

## B3

Our system will also keep a track of leading Indian and Global stock market news websites such as - 

1. [moneycontrol.com](https://www.moneycontrol.com/)

2. [tradingeconimics.com](https://tradingeconomics.com/)

3. [money.reddif.com](https://money.rediff.com/news)

Using __NER__(Name Entity Recognition) technique for above websites, we aim to identify headlines related to the companies present in Peyush’s portfolio. The articles about the companies that are present in Peyush's portfolio will be flagged as __News of Interest__. 

We will specially keep an eye on news related to company’s major events like __company merger__, __news about CEO or major stakeholders of company__, __development within industry sector__, __government policy about the sector__, etc.

Once we get our __News of Interest__, we will run a sentiment analysis on the news article to find the general public sentiment around those stocks. We will generate a __confidence score__ based on sentiment analysis to judge the overall sentiment. This confidence score will be shared with Peyush Bansal.

**Advantage of sharing confidence score -**

- Peyush gets regular update about the stock performance and market sentiment.
- Peyush is happy as he do not have to waste his time just to get these updates.
- Peyush will be actively involved in the overall process.
- Peyush can take quick independent decisions based on confidence score.
  



<h2 align="center">Annexure</h2>

# Pseudocode - 

## A. Data Collection:
- __Step 1__: Use steps mentioned in __B2__ to get the data from broker
## B. Data preprocessing:
- __Step 1__: Inspect the data. (Check data size, structure, attributes, etc).
- __Step 2__: Check for missing values.
  - if missing values found:
    - __Step 2.1__: Decide whether to drop the row & column or fill blanks with information
    - if decide to fill the information:
      - __Step 2.1.1__: Calculate missing values using technique like mean, median, mode or other techniques like regression or interpolation.
    - else:
      - __Step 2.1.2__: Drop rows and columns of rows and columns.

## C. EDA (Exploratory data analysis)
- __Step 1__: Visualize the data and try to find patterns and outliers.
- __Step 2__: Try to eliminate outliers by methods such as data transformation.
## D. Entity Recognition:
- __Step 1__: Decide a way to do Entity recognition. There are many ways to do entity recognition. We can use open source libraries like __Spacy__, __NLTK__ to do this task. We can also use simple neural networks like __Perceptron neural netwrok__, __LSTM (Long Short term memory networks)__ to complex neural networks like __BiLSTM-CRM (Bidirectional LSTM Conditional Random fields)__
