# Robust-portfolio-selection
Distributionally robust mean variance portfolio selection with wasserstein distances

input:
historical monthly closing price for stocks (ever being)in S&P500 from 1990 to 2018
S&P500 monthly price (just for comparison to be used as a benchmark in plots)


the function delta gives numbers in range of (1/120) where 120 is the window size, but for the problems we face later in our constraints, we choose a much smaller delta for calculations 
And for the mentioned reason, we use the weight_optimizer function instead of Robust(to skip the calculation of alpha and delta)

for stocks to be used, they have to be in S&P from 1990 till 2000, and we stick to these stocks till the end



problems:
some times the cov matrix is not possitive negative, this has to be resolved by the near_psd but seems like this is not doing a good job
V0 in alpha ? so alpha is taken as 0.8ro or 0.9ro
the constraint in the robust optimization is not satisfied with the delta of O(n^-1) this can be seen and checked in the last section for new frontier
the optimizer for robust should give the same result as markowitz with delta=0 and alpha=ro but its a little far off. (seems like the reason is the Tolerance for termination of the minimizer)
the input data is highly biased
the efficient frontier is suspiciously higher than monte carlo version(same for new frontier)

