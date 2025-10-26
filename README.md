# project-week-3
Mini project - Fashion Data

Presentation can be found at: https://www.canva.com/design/DAG2aiY8P-w/6QUpcdXwRbrosKZihAo6Mg/edit

Green Is the New Black?
How is sustainability performance of fashion brands related to their business growth over the last 5 years?

Our Goal
To analyze whether fashion brands that are hanked at the Lyst Index perform better in sustainability ratings (from Good On You) show stronger business performance — measured by their stock price growth.

Data Sources
1. Define hottest brands from the last Lyst Index 
Source: https://www.lyst.com/the-lyst-index/the-lyst-index-q2-25/ 
Method: Web Scraping 

2. Get data about sustantibily rating for the listed brands
Source: https://directory.goodonyou.eco/ 
Method: Web Scraping + Selenium

3. Get data about stock prices and markets exchanges
Sources: https://uk.finance.yahoo.com/quote/LLOY.L/, https://algotrading101.com/learn/yahoo-finance-api-guide/, https://site.financialmodelingprep.com/developer/docs, https://site.financialmodelingprep.com/developer/docs

5. Get historical finance data for the last 5 years
Source: yfinance library 

6. Conclusion. 

This is just a preliminary, limited analysis, and there are important gaps and biases that are important to notice. Major limitations:

6.1. Brand vs holding-company mismatch
    Many brands are private or held within larger publicly traded groups. Your stock data are for holding companies (e.g., Kering covers Gucci, Balenciaga, Saint Laurent), not brand-level financials.
    Mapping holding-company returns to individual brands assumes brand performance moves with the parent company — a strong assumption that can bias results.

6.2. Private brands
    Several brands are private (no ticker). Those brands are excluded from any stock-based analysis → sample bias (only publicly listed or part of public groups remain).

6.3. Small effective sample size
    Out of 20 brands we have usable stock-return observations for only ~10–12 tickers. That small number limits statistical power and generalizability.

6.4. Sustainability ratings are a single point in time
    Good On You ratings are a snapshot. To study "related to their business growth over the last 5 years" we ideally want time-varying sustainability measures or at least to ensure the rating corresponds to the same timeframe as the growth metric (e.g., rating in 2020 vs growth 2020–2025 vs rating in 2025, which in don’t have.
    Using a single, recent rating to explain five years of historical growth risks reverse causality (growth may have influenced ratings) or misalignment.

6.5. Stock price as proxy for business growth
    Stock price returns capture investor sentiment, market cycles, macro shocks, FX, liquidity, and corporate actions — not only organic business growth (revenue, profit, stores).

6.6. Currency / FX issues
    Tickers trade in different currencies. Comparing absolute price changes across currencies is invalid. Percent returns are more comparable, but FX moves still affect USD-equivalent returns. Ideally convert to a common currency (or use percent returns in local currency and subtract a local benchmark).

6.7. Confounders / omitted variables
    Growth is affected by brand size, region, product mix, macro environment, marketing, acquisitions — all potential confounders. You need control variables (market cap, revenue, region, sector/subsector) where possible.

We were unable to compare the relationship between a company’s market value and its sustainability rating. 
The rating applies to brands, while a single company may own multiple brands.
We didn't have enough data to analyze the dynamics of sustainability ratings over the past five years.