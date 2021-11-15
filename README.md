# rainbow-trader
The Rainbow Trader bot trades daily based on sentiment from https://www.blockchaincenter.net/bitcoin-rainbow-chart/ combined with a strategy defined below. The account value and orders are posted daily on Twitter account https://twitter.com/Rainbow_trader

# Purpose
The sentiment from crypto folks is "DCA and HODL", meaning many do not have an exit strategy and no intention on trying to time the market. This trading robot is a funny attempt at trying to beat the market.

# Bootstraping
The initial input to the robot was 2 USDC for testing. 1 USD was used to buy BTC. Then added 8 additional USDC, for a total of **10 USDC on 12th Nov 2021**.

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
|Still cheap|Buy for 0.25 USDC|Buy for 2% of USDC|
|Accumulate|Buy for 0.50 USDC|Buy for 4% of USDC|
|BUY!|Buy for 0.75 USDC|Buy for 8% of USDC|
|Basically a Fire Sale|Buy for 1.00 USDC|Buy for 16% of USDC|

The "Absolute Strategy" is mostly in place to handle cases where the Percentage Strategy generates amounts too low to be traded.

# Value on selected dates:
13 Nov 2021:  Account value: 9.9819504422 USD. USD: 9.22, BTC: 0.00001194
