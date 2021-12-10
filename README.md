# Stochastic Trend Reversal
These scripts are meant to help spot trend reversals in the price of an instrument.

These script are built in Amibroker Formula Language (AFL). The scripts are:
1. Trend Reversal System
2. Trend Reversal Indicator

The scripts primarily use the Fisher Transform as the base.

The Fisher Transform is calculated as:

Fisher Transform = ½ * ln [(1 + X) / (1 – X)]

Where:

ln denotes the shorthand form of the natural logarithm.

X represents the transformation of price to a level between -1 and 1

The Fisher Transform transfigures price into a Gaussian normal distribution. The indicator is typically used to identify “overbought” and “oversold” market conditions and thus is designed to ascertain potential reversal points in the market.

The Fisher Transform alone is not enough and may appear noisy. 

In order to make it less noisy and more accurate, we will look:
1. Plot the trend
2. Detect a change in the trend

A change in trend is determined by comparing the current value with the previous value using a Linear Regression Slope function.
The change in trend is used as a first potential point of an impending reversal in the price or movement.
A confirmation is then obtained when the trend crosses the moving average.

Outcomes
----------
1. Probaility of reversal is higher at the extremes
2. Probability of trend being maintained is higher during periods of high volume or high activity
3. Not all changes in trend lead to a crossover confirmation
4. Divergences seen in an indicator when coupled with breakouts and breakdowns in price lead to a higher probability of profit
5. Targets will be open ended. Close of a trade is indicated by a reversal or crossover in the opposite direction

Downsides / Risks
------------------
1. Not all trades will be profitable. Position sizing and risk management is key to handling risk
2. Instrument prices are not usually normally distributed, so there is a risk of unreliable signals

![Screenshot](https://github.com/satishnarasimhan/stochastic-trend-reversal/blob/main/stochreversal.jpg)
