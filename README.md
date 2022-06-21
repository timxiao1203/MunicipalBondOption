# Municipal Bond Option


Municipal Bond Options are European-style vanilla options on coupon bonds. The Municipal Bond Option Pricing Model is used for daily calculations of P&amp;L and risk numbers.

These options are of vanilla European type. Black’s model (Black-76 model) is applied in the bond option pricing model. The discount curve is composed of a set of short tern rates, LIBORs up to two years and a set of medium to long term (2 years – 30 years) AAA yields with linear interpolation. 

Bond yield volatilities consist of one month (30 days) and one year (252 days) volatilities for a sequence of bond maturities with two dimensional linear interpolation. All those parameters are market observable. In application of Black’s model to price bond option, an option tenor should be much shorter than the term of an underlying bond.

Let T be the maturity of a European vanilla bond option, K be the strike price and V T  denote the underlying bond price at option’s maturity, then the payoff for a call option is max(V T - K, 0) ; correspondingly, the payoff for a put option is max( K - V T, 0) . The forward bond price at time t can be determined where L is the face value of the bond, c is the coupon payment, t i,  i = 1, ..., N is the i-th coupon date with the last one at bond maturity and df (x, y) denotes the discount function for the period between x and y with 0 < x ≤ y .

In the Black’s model, the fair price for a bond call option with time to expiry T , risk-free interest rate r , bond current forward price 0 , strike price F K and price volatility σ is given where N(⋅) denotes the cumulative distribution function (cdf) for a standard normal random variable and

A bond put option with the same specifications has a fair value given where n(⋅) denotes the probability density function (pdf) for a standard normal random variable.

The yield volatilities of the underlying bonds are interpolated from a sequence of AAA yield volatilities with maturities ranging from half a year to 30 years, as a result, the time to maturity of an underlying bond should not be less than half a year. Moreover, as the option tenor approaches the bond maturity, randomness in the bond price is dampened and the underlying assumptions in the Black’s model become less valid, therefore, we require that the ration of the option tenor versus the bond maturity be no more than 25%.


Reference:

https://finpricing.com/lib/EqCallable.html

https://zenodo.org/record/6617864#.Yp5YuagpBD8

https://zenodo.org/record/6617864/files/mmBasisCurve.pdf
