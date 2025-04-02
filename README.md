# A Stock analysis

### Group Members
Marry Shintaku, Kirsten Formento, David Jian, Cindy Duong

### Details of the Project:
We are a group of data analysts seeking to understand stock price data by performing a fixed-window, technical analysis on a group of stocks. 

Fixed-Window & Technical Analysis:
We acknowledge that each company for each stock may be from different industries and/or run their operations uniquely. While we cannot compare each company by how they are operated, we can perform a technical analysis of the historical data and draw conclusions based on the stock data. Please note that our API data was pulled as of January 30, 2025. The time frame of our analysis will be between the last quarter of 2024 and the first month of 2025. We understand that our analysis of the data will be restricted to this time frame (fixed-window analysis) and that the stock performance may have changed between the time we pulled the data to when we present the information. 

### Selecting 8 stocks:
On January 30, 2025, we pulled a list of the stock market's top 20 gainers and the bottom 20 losers for that day. Each group member selected 1 gainer stock and 1 loser stock from that list and performed a technical comparison of their chosen stock.
Gainer List: NVDA, YIBO, DWTX, AKRO
Loser List: WOK, AVGX, ELAB, NRO

Technical comparison: NVDA vs. WOK, YIBO vs. AVGX, DWTX vs. ELAB, AKRO vs. NRO

### Which of these 8 stocks will be in the top 4?
### Which of these 8 stocks is the best one to invest in as a long-term investor?
### Analysis Metrics:
- Price trend stability and consistency
- Price volatility and liquidity

### Database used: MongoDB
### Python Library used (not covered in class): MPLFinance 

# <ins> Please see Final Folder: </ins>
- see [stock_data_retreival](https://github.com/cindyd97/A_Stock_Analysis/blob/main/Final%20Folder/stock_data_retrieval.ipynb) for our code to make the api call and retrieve the data for the top 20 gainer stocks and bottom 20 loser stocks where we selected 8 stocks from that list. The notebook also shows our code making another api call for the stock data of each stock and storing it into MongoDB. The stock data is in .json format including open, high, low, close, volume, date, and symbol. Our code also reformats the json data into a more readable format where we can edit and perform analysis. There are comments within the code as well as descriptions in the markdowns of this notebook describing the details.
- see [nvda_wok_analysis](https://github.com/cindyd97/A_Stock_Analysis/blob/main/Final%20Folder/nvda_wok_analysis.ipynb), [avgx_yibo_analysis](https://github.com/cindyd97/A_Stock_Analysis/blob/main/Final%20Folder/avgx_yibo_analysis.ipynb), [dwtx_elab_analysis](https://github.com/cindyd97/A_Stock_Analysis/blob/main/Final%20Folder/dwtx_elab_analysis.ipynb), and [nro_akro_analysis.ipynb](https://github.com/cindyd97/A_Stock_Analysis/blob/main/Final%20Folder/nro_akro_analysis.ipynb) for our code comparing our selected stocks against eachother. Within each of these notebooks, there are comments and descriptions written in markdowns describing our code approach as well our observations of results. We utilized mplfinance to plot candlestick charts for each stock. We calculated standard deviation as well as rolling standard deviation for each stock and compared the pairs based on volatility. We pulled market index data (SP500) to compare each stock to the market and calculated the beta of each stock. Discussion of analysis and observations are written in detail within the markdowns of each notebook. The analysis also discusses the metrics and how we concluded why one stock should be preferred over the other. This ultimately brings our analysis to the top 4 stocks (AVGX, NRO, NVDA, DWTX) out of the 8. [nro_akro_data_cleanup](https://github.com/cindyd97/A_Stock_Analysis/blob/main/Final%20Folder/nro_akro_data_cleanup.ipynb) and [dwtx_elab_data_cleanup.ipynb](https://github.com/cindyd97/A_Stock_Analysis/blob/main/Final%20Folder/dwtx_elab_data_cleanup.ipynb) are supplemental notebooks that include code to prepare the data for analysis.
- see [avgx_nro_top4_analysis](https://github.com/cindyd97/A_Stock_Analysis/blob/main/Final%20Folder/avgx_nro_top4_analysis.ipynb) and **nvda_dwtx_top4_analysis** for our code comparing AVGX vs. NRO and NVDA vs. DWTX. Within each of these notebooks, there are comments and descriptions written in markdowns describing our code approach as well our observations of results.The analysis also discusses the metrics and how we concluded why one stock should be preferred over the other. This ultimately brings our analysis to the top 2 stocks (AVGX and NVDA) out of the top 4.
- see **winner_analysis.ipynb** for our code comparing AVGX vs. NVDA. Within each of these notebooks, there are comments and descriptions written in markdowns describing our code approach as well our observations of results.The analysis also discusses the metrics and how we concluded why one stock should be preferred over the other. This ultimately brings our analysis to the 'winner', NVDA. We provide discussion on the winner as well as additional information within the markdowns.
- see **all_8_stocks_analysis.ipynb** for our code analyzing all 8 stocks and comparing them against eachother based on stock price trend and standard deviation. This notebook is supplemental to our analysis.
- see **Slide deck presentation folder** for a pdf copy of our slide deck presentation.
- see **Stock_data folder** for the json data that we pulled from the api as well as our reformatted versions of the json file.
- see **Visuals folder** for the graphs and charts that we created in python (downloaded as png images).
- see **Website code** for the code html code to run our website design. Open the folder and run the html file named "Home.html" on live server. This will take you to the website homepage where you can see a main bar with click options to bring you to our visuals as well as other descriptions.
  
### Website Breakdown: 
Our website was coded in HTML with Bootstrap as the base of the framework. We have created a total of four main pages that consists of a home page, a Big Question page, a visualizationg page, and key insights. Our home page shows an introduction to our project. The Big question page presents the questions we are answering. And the visualization page contains a javascript powered visualization tool called plotly. Using the tool, we plotted the price trend of each of our stock starting from Q4 2024 to Jan 2025. This interactive tool allows users to hover over each candlestick point and see the open, high, low, and close price given for that date. And right between the x-axis and title of the graphs, there is a smaller graph that shows a simplified version of the price trend. Users can interactive with this bar to select the range they want to view at the top main graph. Plotly also provides many more features that includes but not limited to zoom or pan in the top left. The Key Insights page shows the stock on the left and then a beta graph on the right that shows a comparison of the stock to the market. Each page follows a consistency layout and colors. At the top of each page, we included a navbar allowing quick access between the page. Also in the navbar, we created a dropdown menu that lets you click through the different beta line graph for the different stocks

### Data Sources:
Alpha Vantage. (n.d.). Alpha Vantage API. https://www.alphavantage.co/
