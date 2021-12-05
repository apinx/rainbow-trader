# rainbow-trader
The Bitcoin Rainbow Trader Bot trades daily based on sentiment from https://www.blockchaincenter.net/bitcoin-rainbow-chart/ combined with a strategy defined below.

# Actual beginning
10 USD on 26th Nov, 2021.

# Strategy
Every day at 00.00 UTC: 
1) React to sentiment from the Bitcoin rainbow chart
2) Trade for MAX of the below two strategies

| Sentiment |Absolute Strategy | Percentage Strategy |
|---|---|---|
|Maximum Bubble Territory|Sell 1.00 USD worth of BTC|Sell 16% of BTC|
|Sell. Seriously, SELL!|Sell 0.75 USD worth of BTC|Sell 8% of BTC|
|FOMO intensifies|Sell 0.50 USD worth of BTC|Sell 4% of BTC|
|Is this a bubble?|Sell 0.25 USD worth of BTC|Sell 2% of BTC|
|HODL!|0|0|
|Still cheap|Buy for 0.25 USD|Buy for 2% of USD|
|Accumulate|Buy for 0.50 USD|Buy for 4% of USD|
|BUY!|Buy for 0.75 USD|Buy for 8% of USD|
|Basically a Fire Sale|Buy for 1.00 USD|Buy for 16% of USD|

The "Absolute Strategy" is mostly in place to handle cases where the Percentage Strategy generates amounts too low to be traded.

The price of the limit orders created will be current price * 0.99 for buys and 1.01 for sells.

# Value on selected dates:
26 Nov 2021:  Account value: 10.00 USD. USD: 10.00, BTC: 0.00
