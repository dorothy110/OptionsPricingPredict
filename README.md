# OptionsPricingPredict
Second Prize: Gaussian Cup National College Students Mathematical Modeling Challenge 2020 
 - [paper(code in the end of the pages)](https://github.com/dorothy110/OptionsPricingPredict/blob/main/D%E7%BB%84-C%E9%A2%98.pdf)
 
Based on the option data of Shanghai Stock Exchange 50ETF, this paper uses Monte Carlo method to build a scientific option pricing model.

First, according to the option pricing formula
```
S_(t+∆t)=S_t exp⁡[(r-σ^2/2)dt+σε√dt]
```

Find out all the influence factors, according to the variables contained in our original data to filter collation. 

The initial price, the price due, the holding period, the risk-free rate of return and the price volatility of the four 10002568.SH  were combined based on the quotes of the four intermediaries. At the same time to determine two of the 4 put options, two call options, and in the model classification design: long call options and long put options two payoffs.

Then we chose to use the Monte Carlo method to simulate multiple price movements, and each of the four intermediaries explored 10,000 possible stock movements under the table, in order to make our calculations faster, we Log the pricing formula. Using the difference between the initial price and our exercise price, we find a positive result when we discuss call options, and average the profits after summing, and the opposite when we discuss put options. 

After obtaining the average profit, use the formula to figure out the real option value.
```
c=E(C_T ) e^(-r(T-t))
```

Finally, we can achieve the required precision by increasing the number of randomization greatly, using MSE size and grey correlation to check whether there is a small error between the average result of our Monte Carlo Calculation and the actual option price.

It was found that the price trend charts derived from the Monte Carlo method simulations were very similar to the contract price trend charts. The MSE was smaller, indicating less error, and was a successful model.
