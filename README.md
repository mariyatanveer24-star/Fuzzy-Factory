# Fuzzy-Factory
Fuzzy Factory: Power BI Analysis of an Online Toy Store
I built this report to answer a simple question: where does this store make money, and where does it lose it?
The data is from Maven Analytics (the "Fuzzy Factory" e-commerce dataset). It covers about 473,000 website visits and 32,000 orders from March 2012 to March 2015.

Questions I set out to answer----
Which marketing channels bring in the most visitors?
How many visitors actually buy, and does that change by channel or device?
How did revenue and profit change over time?
Which products earn the most profit?
How much money is lost to refunds, and on which products?
Do customers add extra items to their order?


What I found----
The store had a conversion rate of 6.83% (visits that turned into an order).
Desktop visitors convert at about 8.5% and mobile visitors at about 3.1%. Desktop brings in roughly 86% of revenue.
Google nonbrand search is the biggest source of traffic and revenue. Social has the lowest conversion, around 3.2%.
Gross margin is about 62.7%. After about $85K in refunds, net profit is about $1.13M.
About 4.3% of items sold are refunded. The Birthday Sugar Panda has the highest refund rate (6.04%) and the Hudson River Mini Bear the lowest (1.28%).


What I would recommend---
Improve the mobile experience before spending more to bring in mobile traffic.
Avoid depending on one channel. Review the budget for social, which converts the least.
Look into why the Birthday Sugar Panda is refunded so often. In my what-if model, cutting refunds by 20% adds roughly $17,000 in profit.
Test product suggestions at checkout to raise items per order.


How I built it----
Power Query: fixed date formats, replaced "NULL" text, set data types, and created a marketing channel column from the source and campaign fields.
Data model: 5 tables plus a calendar table, connected with one-to-many relationships (a star schema).
DAX: measures for revenue, gross profit, net profit, conversion rate, refund rate, average order value, items per order, year-over-year change, and rolling 3-month revenue.
Report features: drill-through to a product page, a tooltip page, a field parameter to switch metrics, a what-if slider for refund reduction, a decomposition tree, and key influencers.


Data source----
Maven Analytics, Fuzzy Factory e-commerce dataset. I did not upload the raw data. You can download it from the Maven Analytics data playground.
Customers buy only 1.24 items per order, so cross-selling is an open opportunity.
About 17% of visits come from repeat visitors.
