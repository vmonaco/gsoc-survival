# GSoC 2015 proposal: Multivariate Survival analysis
Test results and proposal for GSoC 2015

See the [proposal](proposal/Monaco-gsoc2015.pdf?raw=true). The completed test is reproduced below.

## Simulation results (Appendix B in proposal)

Simulations were performed with R version 3.1.3 running in an Ubuntu 12.04 desktop with AMD Phenom 9550 Quad-Core 2.20 GHz Processor. All of the simulation results are obtained using penalized partial likelihood estimation, namely the coxph function in the survival package with the Breslow method. Each simulation was repeated 500 times to obtain the empirical mean and SD. The empirical censorship and runtime (in seconds) are also reported. For more information, see the [proposal](proposal/Monaco-gsoc2015.pdf?raw=true).

**Table 4** Ignoring the clustered data: A constant frailty is assumed when the actual frailty is either gamma or log-normal. The coefficients are consistently biased, as this model ignores the clustered data and underestimates the effect of the coefficient. The bias is less severe with greater censorship, likely the result of decreased clustering. There is more diversity at 80% censorship due to fewer individual from the same family being selected, though this conjecture has not been verified.

![Table 4](figures/table4.png)

**Table 5** Gamma frailty with a single covariate: The model behaves as anticipated, and correctly estimates the coefficient and frailty distribution variance within error. One confound is the the SD for \bfZ ~ U(0, 1) is closer to that found in [3], yet their simulation used covariates from a standard 

![Table 5](figures/table5.png)

**Table 6** Gamma frailty with two covariates: Again, the coefficients and frailty variance are correctly estimated within error.

![Table 6](figures/table6.png)

**Table 7** Log-normal frailty with a single covariate: With θ = 2, the log-normal has a heavier tail than the gamma, and thus more clustering. As a result, with high censorship, the coefficients and frailty variance tend to by slightly underestimated. Similar to the gamma frailty, the error for uniformly-distributed individual covariates is higher than standard normal individual covariates.

![Table 7](figures/table7.png)

**Table 8** Assuming the wrong frailty: When the true frailty is log-normal and we assume a gamma distribution, the coefficients are underestimated. This effect is pronounced for higher censorship. This is a result of underestimating how much the data are clustered, since the log-normal has a heavier tail and produces more clustered data. Underestimation is not as severe when the true frailty is gamma and a log-normal is assumed. In this case, we assume the data is more clustered that it actually is.

![Table 8](figures/table8.png)

