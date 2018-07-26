# Robust-portfolio-selection
Distributionally robust mean variance portfolio selection with wasserstein distances

input:
historical monthly closing price for stocks (ever being)in S&P500 from 1990 to 2018
S&P500 monthly price (just for comparison to be used as a benchmark in plots)


the function delta gives numbers in range of (1/120) where 120 is the window size, but for the problems we face later in our constraints, we choose a much smaller delta for calculations 
And for the mentioned reason, we use the weight_optimizer function instead of Robust(to skip the calculation of alpha and delta)

for stocks to be used, they have to be in S&P from 1990 till 2000, and we stick to these stocks till the end
