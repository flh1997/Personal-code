# Yield Curve Spread Trades
some homework project
A yield curve spread is the yield differential between two different maturities of a bond issuer i.e. 10 yr U.S. Treasury yield - 2 yr U.S. Treasury yield. The later maturity leg of the trade is referred to as the back leg and the trade leg maturing earlier is called the front leg. Two primary yield curve spread strategies are the flattener and the steepener. The risk measure for yield curve spread trades is DV01 (dollar value of a basis point), As the back leg DV01 is greater than the front leg DV01, one must calculate a hedge ratio to result in a DV01 neutral position.

In this project, you will evaluate the performance of the 10 yr - 2 yr U.S. Treasury yield curve spread trade.
1. You can choose either the 10yr - 2yr U.S. Treasury attener or steepener strategy to analyze and stay with this strategy throughout the sample.
2. Download the daily U.S. Treasury yield curve from here. That file has the daily parameters for the Nelson-Siegel-Svensson yield curve model discussed in class. With
those parameters, you can calculate the yield of any maturity. For simplicity, you will trade zero-coupon bonds and you can assume that a bond of any maturity is available
to trade.
3. On 12/30/1983, you start with $1 million in initial capital. Set up a DV01-neutral yield curve spread trade. Fixed income investments can be highly levered. Assume
that you have a 10% capital requirement on your trading positions. For example, if you are long $10 mm and short $5 mm you need to hold $1.5 mm in capital.
4. Calculate the size of the cash position. This is the value of the short position minus the value of the long position plus the amount of capital you hold against those positions.
5. Each week (hint ?xts::endpoints), rebalance to maintain the DV01-neutral position. This involves the following steps:
(a) Calculate the new prices of the bonds using that day's yield curve. A 10-year bond last week is a 9-year 358-day bond today and a 2-year bond last week is a 1-year 358-day bond today.
(b) Calculate the interest earned or paid on the cash you hold. You can assume that you receive and pay the one-week Treasury yield.
(c) Close out the positions, calculate your total capital, and reinvest in the spread trade given your capital and the margin requirements. For a 2s10s trade, this would involve a new 10-year and a new 2-year bond.
(d) Calculate your weekly return.
6. Unwind your trade on June 30, 2019.
Questions
1. Plot the cumulative return for your trading strategy.
2. Although the spread trade is DV01-neutral, there is unhedged convexity. Calculate the convexity risk of the spread trade for a 10 basis point change in yields for a constant
$1mm (in terms of face value) position in the 10 yr Treasury. Plot the convexity risk over time.
3. Each week, calculate the duration and convexity for each leg of your trading strategy. Given your risk metrics, the changes in yields, and the size of your positions, decompose the weekly return into the following components:
(a) Spread return: the return due to changes in the yield spread using DV01.
(b) Convexity return: the return due to changes in the yield from convexity.
(c) Time return: the return due to the passage of time and interest on the cash
position.
(d) Residual: the difference between the total return and the sum of the spread return, convexity return, and time return.
Create a plot of the cumulative total return, spread return, convexity return, time return, and the residual. How much did each component contribute to the total return?
4. How does a 2% margin requirement impact the cumulative return of your trading strategy? Plot the cumulative total return of the 2% margin requirement compared to
the 10% margin requirement. You should submit two files: one pdf document and one .R file. Your pdf document should be a report discussing the results of your analysis. It should include the following sections: Executive Summary, Introduction, Discussion (broken into several sections), and a Conclusion. You can put the figures and tables either at the end of you document or throughout.
No .R template is provided for this assignment. The .R file should be clearly documented. You cannot use any packages other than data.table, lubridate, magrittr, tidyverse, xts and any of their dependencies.
