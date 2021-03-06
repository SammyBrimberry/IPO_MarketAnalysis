
# Objective
I used the software packages pandas, numpy, plotly and matplotlib to analyze IPO market data from 2014-01-10 to 2020-09-30. The analysis provides a high-level overview of the following areas:

* Key industries

* Key geographies

* Summary statistics and correlation of IPO's capital raised, post-money valuation and opening price per share

* Volatility experienced over the period

* Trend and noise experienced in IPO's capital raised, post-money valuation and opening price per share over the period

# Market Findings
After cleaning, our data represented 6,739 global companies that released an IPO over 2014-01-10 to 2020-09-30 (please view the *Loading CSV & Data Cleaning* section of the python notebook to review the data cleaning process). 

* Our sample represents companies from 7 different verticals; Healthcare (30%), IT (22%) and B2B (18%) are the industry’s most IPO companies operated in over the period. The industry sectors who raised the most capital (mUSD) over the period were Financial Services, Consumer Products and Services and Energy. Indicating the acknowledgment from the investment community that these sectors are primed for long-term growth, facilitated by the adoption of digital transformation and related technologies

* Our sample represents companies from 68 countries; United States (39%), China (20%), UK (6%) had the largest share of IPO's over the period. Yet the United States (21th), China (20th), and UK (14th) do not hold the largest share of capital raised. Luxembourg (1st), Vietnam (2nd) and Austria (3rd) were the countries that raised the most capital (mUSD) over the period

* Over the period, the mean capital raised was $228m with a standard deviation of $545.6m. The mean Post-money valuation of IPO companies was $1,333m with a standard deviation of $6,981m. The company to IPO with the highest post-money valuation was Rayhoo at $330,903m (Saudi Aramco was dropped from this data set during the cleaning process, most likely to containing NaN values)

* Using the quant variables (i.e. capital raised, opening price per share, etc.) we observed that capital raised and post-money valuation were positively correlated at 0.5; deal number and capital raised were positively correlated at 0.26

* IPO's capital raised, post-money valuation and opening price per share varied widely between companies. After decomposing trend and noise from the variables mentioned above, we were able to corroborate the highly volatile nature of the IPO market. Compared to 2017, IPO opening price per share seems to be trending higher as of 2020; IPO's capital raised and most-money valuation seem to be trending similar or slightly lower in 2020 than in 2017

# Formulas/Functions Used
The python workbook leverages several built in functions from several software packages; including: pandas, plotly, datetime, statsmodels.api, matplotlib, etc.
Below I detail the most frequently used functions:

* Pandas - a software package for dataframe manipulation: copy(), dropna(), isnull(), value_counts(), astype(), std(), corr(), info(), describe(), groupby(), unique(), etc.

* Statsmodels - an API with various stats functions: HP filter

* Matplotlib - visualization package that works inline with pandas: plot()

* Plotly - interactive visualization package: hvplot()
