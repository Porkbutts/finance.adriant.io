---
layout: post
title: Easy way to think about vertial spreads
categories: trading
tags: options
---

As a beginner in options trading, you're likely to start out only buying calls and puts. Selling naked calls or puts is extremely risky and an easy way to blow up your account, while other basic strategies like the covered call and cash covered put require larger amounts of capital. Buying calls and puts is an easy way to get your feet wet with the options trading game, and requires a relatively small amount of capital compared to the potential gains.

Position sizing is also an important aspect of risk management in options trading. In other words, you should be comfortable losing some maximum dollar amount for a single options trade. Since options prices are proportional to their underlying stock prices, buying options for higher priced stocks can disproportionately expose the portfolio to increased risk toward these higher priced stocks.

To illustrate this point let's look at an example. Slack (WORK) is currently trading around $35, and its at-the-money calls expiring next week are trading between $2 and $3, whereas Chipotle (CMG) is currently trading around $1050, and its at-the-money calls expiring next week are valued between $10 and $15. In this case, you would have to spend between $200 to $300 to buy the WORK call, but you would be looking at between $1000 to $1500 to buy the CMG call. The options prices would increase even more when you start looking at options with expiration dates further out.

So what's the answer here? You can't buy less than one options contract, or a fraction of a contract. You could stick to only buying options contracts that are within your budget. But there's a better option here (no pun intended) and it is the **vertical spread**.

<!--more-->

## Vertical Spread

Spreads don't have to be complicated, but they may feel that way after looking at all the variations and charts depicting profit-loss potential. There is actually a really easy way to reason about spreads which is this:

> A **debit spread** is basically like buying an option but at a discount, in exchange for capping profit potential.

> A **credit spread** is basically like selling an option but at a discount, in exchange for capping loss potential.

So when thinking about whether I want to trade a spread, I start with thinking about whether I want to buy or sell a particular option. If I want to buy an option but it's too expensive, I'll use a debit spread to discount the purchase while accepting that my max profit will be capped. If I want to sell an option, I'll use a credit spread, accepting that my initial credit is reduced in exchange for putting a cap on my maximum loss.

Let's take a look at a **debit spread** as an example.

### Debit Spread

A **debit** means that the end result is that you bought or paid for something. Think about a debit spread as buying an option at a discount, in exchange for putting a cap on your maximum profit. To construct the debit spread, buy one option and sell a further out-the-money option with the same expiration date. You basically discount the long call by the price of the short call. The maximum profit is the difference in strike prices, less the debit paid.

Consider the following example.

{% include image.html file="cmg-bull-call-spread.png" %}

Suppose I have bullish outlook on CMG and I want to buy the CMG 1055 call expiring next week for $14.50. The cost for the call option is $1450, more than I am comfortable with for a single position, so I'm going modify this trade by turning it into a debit call spread, also known as a bull call spread.

To create a spread, I might buy the 1055 call for $14.50 and sell the 1065 call for $9.30. My net debit would then be **$520** = ($14.50 - $9.30) x 100. My maximum profit would be **$480** = ($1065 - $1055) x 100 - $520. Since I am basically long the debit spread, my max loss is just the premium paid.

A debit put spread, or bear put spread is basically the same idea as the debit call spread, where you find a put option you want to buy and then modify it into a debit put spread by selling a further OTM put.

### Credit Spread

A **credit** means that you receive money when you open the position. Your profit would be determined by whether you can close out that position for less than you initially received. A credit spread is a selling strategy, just like selling a call or a put. Selling strategies allow you to take advantage of time decay and can be more attractive than buying strategies when premiums are higher than they should be. Unfortunately, selling naked options will expose your portfolio to the risk of substantial losses, and the only other basic selling strategies, the covered call and cash-covered put, require much more capital than buying strategies.

The credit spread addresses both of these drawbacks, allowing us to consider sell strategies while maintaining lower capital outlays. To construct a credit spread, sell one option and buy a further out-the-money option with the same expiration date. You can think of the long option as a kind of insurance which caps your losses if the stock price moves against you. The maximum profit of the trade is the net credit received from the trade and is only realized when both the options expire worthless. The maximum loss of this strategy is the difference in strike prices less the credit received.

Let's take a look an example with CMG again.

{% include image.html file="cmg-bear-call-spread.png" %}

Suppose we have a bearish outlook on CMG and are looking to sell the June 1st 1040 call to receive a premium of $99. We would receive a $9900 credit, but we would also be exposing our portfolio to substantial losses if CMG stock price moves up significantly. To limit those losses, we could pair the short call with a further out-the-money long call like the 1060 call for $88.70. Our net credit would be reduced to **$1030** = ($99 - $88.70) x 100, but our max loss would also be capped to **$970** = ($1060-$1040) x 100 - $1030.

A bull put spread could be similarly constructed by selling a put and buying a further OTM put.

## Summary

There are essentially four basic ways to trade spreads. Remember that each spread strategy is simply an extension of buying or selling a call or put. This table summarizes which spread corresponds to which unmodified strategy.

|             | paired with            | spread            | credit or debit |
|:------------|:-----------------------|:------------------|:----------------|
| long call   | short further otm call | bull call spread  | debit           |
| long put    | short further otm put  | bear put spread   | debit           |
| short call  | long further otm call  | bear call spread  | credit          |
| short put   | long further otm put   | bull put spread   | credit          |