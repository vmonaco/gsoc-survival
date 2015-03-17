# GSoC 2015 proposal: Multivariate Survival analysis
Test results and proposal for GSoC 2015

See the [proposal](proposal/Monaco-gsoc2015.pdf?raw=true). The completed test is reproduced below.

Simulation results
==================

Simulations were performed with R version 3.1.3 running in an Ubuntu 12.04 desktop with AMD Phenom 9550 Quad-Core 2.20 GHz Processor. All of the simulation results are obtained using penalized partial likelihood estimation, namely the coxph function in the survival package with the Breslow method. Each simulation was repeated 500 times to obtain the empirical mean and SD. The empirical censorship and runtime (in seconds) are also reported. For more information, see Section [sub:Simulation].

[h] Ignoring the clustered data: A constant frailty is assumed when the actual frailty is either gamma or log-normal. The coefficients are consistently biased, as this model ignores the clustered data and underestimates the effect of the coefficient. The bias is less severe with greater censorship, likely the result of decreased clustering. There is more diversity at 80% censorship due to fewer individual from the same family being selected, though this conjecture has not been verified.[tab:Assume-constant-frailty]

[Gamma frailty]

l|c|c|c|

4c$\beta^{0}=\log2$, $N(130,15^{2})$ censoring2-4 & $\hat{\beta}$ & Censoring & Runtime1|l|Emp. mean & 0.342 & 0.379 & 0.0171|l|Emp. SD & 0.056 & 0.024 & 0.0011l & 1c & 1c & 1c4c$\beta^{0}=\log2$, $N(60,15^{2})$ censoring2-4 & $\hat{\beta}$ & Censoring & Runtime1|l|Emp. mean & 0.565 & 0.883 & 0.0161|l|Emp. SD & 0.128 & 0.013 & 0.0011l & 1c & 1c & 1c4c$\beta^{0}=\log3$, $N(130,15^{2})$ censoring2-4 & $\hat{\beta}$ & Censoring & Runtime1|l|Emp. mean & 0.541 & 0.390 & 0.0171|l|Emp. SD & 0.061 & 0.025 & 0.0011l & 1c & 1c & 1c4c$\beta^{0}=\log3$, $N(60,15^{2})$ censoring2-4 & $\hat{\beta}$ & Censoring & Runtime1|l|Emp. mean & 0.846 & 0.868 & 0.0161|l|Emp. SD & 0.127 & 0.014 & 0.001

[Log-normal frailty]

l|c|c|c|

4c$\beta^{0}=\log2$, $N(130,15^{2})$ censoring2-4 & $\hat{\beta}$ & Censoring & Runtime1|l|Emp. mean & 0.393 & 0.199 & 0.0161|l|Emp. SD & 0.049 & 0.019 & 0.0011l & 1c & 1c & 1c4c$\beta^{0}=\log2$, $N(60,15^{2})$ censoring2-4 & $\hat{\beta}$ & Censoring & Runtime1|l|Emp. mean & 0.507 & 0.796 & 0.0161|l|Emp. SD & 0.094 & 0.018 & 0.0011l & 1c & 1c & 1c4c$\beta^{0}=\log3$, $N(130,15^{2})$ censoring2-4 & $\hat{\beta}$ & Censoring & Runtime1|l|Emp. mean & 0.630 & 0.219 & 0.0171|l|Emp. SD & 0.056 & 0.019 & 0.0011l & 1c & 1c & 1c4c$\beta^{0}=\log3$, $N(60,15^{2})$ censoring2-4 & $\hat{\beta}$ & Censoring & Runtime1|l|Emp. mean & 0.787 & 0.781 & 0.0161|l|Emp. SD & 0.091 & 0.019 & 0.001

Gamma frailty with a single covariate: The model behaves as anticipated, and correctly estimates the coefficient and frailty distribution variance within error. One confound is the the SD for ${\bf Z}\sim\mathcal{U}(0,1)$ is closer to that found in \cite{gorfine2006prospective}, yet their simulation used covariates from a standard normal.

[Standard normal covariate, ]

l|c|c|c|c|

5c$\beta^{0}=\log2$, $N(130,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.686 & 1.977 & 0.379 & 0.1991|l|Emp. SD & 0.086 & 0.276 & 0.024 & 0.0181l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log2$, $N(60,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.691 & 1.802 & 0.883 & 0.0611|l|Emp. SD & 0.169 & 1.011 & 0.013 & 0.0091l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log3$, $N(130,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 1.090 & 1.978 & 0.390 & 0.1911|l|Emp. SD & 0.102 & 0.277 & 0.025 & 0.0171l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log3$, $N(60,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 1.090 & 1.879 & 0.868 & 0.0661|l|Emp. SD & 0.187 & 0.921 & 0.014 & 0.009

[Uniform covariate]

l|c|c|c|c|

5c$\beta^{0}=\log2$, $N(130,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.699 & 1.961 & 0.320 & 0.2291|l|Emp. SD & 0.246 & 0.274 & 0.024 & 0.0201l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log2$, $N(60,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.746 & 1.837 & 0.863 & 0.0631|l|Emp. SD & 0.443 & 0.866 & 0.015 & 0.0091l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log3$, $N(130,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 1.101 & 1.959 & 0.294 & 0.2441|l|Emp. SD & 0.248 & 0.265 & 0.024 & 0.0201l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log3$, $N(60,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 1.146 & 1.843 & 0.841 & 0.0691|l|Emp. SD & 0.430 & 0.729 & 0.016 & 0.010

Gamma frailty with two covariates: Again, the coefficients and frailty variance are correctly estimated within error.

[Standard normal covariate]

l|c|c|c|c|c|

6c|$\beta_{0}=\log2$, $\beta_{1}=\log3$, $N(130,15^{2})$ censoring2-6 & $\hat{\beta}_{0}$ & $\hat{\beta}_{1}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.692 & 1.099 & 1.959 & 0.395 & 0.2641|l|Emp. SD & 0.086 & 0.100 & 0.281 & 0.024 & 0.0211l & 1c & 1c & 1c & 1c & 1c6c$\beta^{0}=\log2$, $\beta_{1}=\log3$, $N(60,15^{2})$ censoring2-6 & $\hat{\beta}_{0}$ & $\hat{\beta}_{1}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.687 & 1.100 & 1.857 & 0.860 & 0.0821|l|Emp. SD & 0.161 & 0.176 & 0.873 & 0.015 & 0.013

Log-normal frailty with a single covariate: With $\theta=2$, the log-normal has a heavier tail than the gamma, and thus more clustering. As a result, with high censorship, the coefficients and frailty variance tend to by slightly underestimated. Similar to the gamma frailty, the error for uniformly-distributed individual covariates is higher than standard normal individual covariates.

[Standard normal covariate]

l|c|c|c|c|

5c$\beta^{0}=\log2$, $N(130,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.671 & 1.808 & 0.199 & 0.1961|l|Emp. SD & 0.071 & 0.296 & 0.019 & 0.0141l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log2$, $N(60,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.600 & 1.130 & 0.796 & 0.0541|l|Emp. SD & 0.105 & 0.265 & 0.018 & 0.0061l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log3$, $N(130,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 1.061 & 1.802 & 0.219 & 0.1841|l|Emp. SD & 0.085 & 0.292 & 0.019 & 0.0121l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log3$, $N(60,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.953 & 1.162 & 0.781 & 0.0581|l|Emp. SD & 0.106 & 0.269 & 0.019 & 0.006

[Uniform covariate]

l|c|c|c|c|

5c$\beta^{0}=\log2$, $N(130,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.683 & 1.889 & 0.141 & 0.2231|l|Emp. SD & 0.224 & 0.296 & 0.017 & 0.0161l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log2$, $N(60,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.630 & 1.164 & 0.763 & 0.0621|l|Emp. SD & 0.347 & 0.253 & 0.020 & 0.0071l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log3$, $N(130,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 1.084 & 1.922 & 0.120 & 0.2341|l|Emp. SD & 0.227 & 0.304 & 0.015 & 0.0181l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log3$, $N(60,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.989 & 1.199 & 0.733 & 0.0681|l|Emp. SD & 0.331 & 0.252 & 0.021 & 0.008

Assuming the wrong frailty: When the true frailty is log-normal and we assume a gamma distribution, the coefficients are underestimated. This effect is pronounced for higher censorship. This is a result of underestimating how much the data are clustered, since the log-normal has a heavier tail and produces more clustered data. Underestimation is not as severe when the true frailty is gamma and a log-normal is assumed. In this case, we assume the data is more clustered that it actually is.[tab:Assume-the-wrong]

[Gamma frailty, assume log-normal]

l|c|c|c|c|

5c$\beta^{0}=\log2$, $N(130,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.615 & 2.050 & 0.379 & 0.1391|l|Emp. SD & 0.077 & 0.291 & 0.024 & 0.0121l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log2$, $N(60,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.620 & 0.866 & 0.883 & 0.0411|l|Emp. SD & 0.140 & 0.304 & 0.013 & 0.0031l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log3$, $N(130,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.979 & 2.111 & 0.390 & 0.1361|l|Emp. SD & 0.091 & 0.304 & 0.025 & 0.0111l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log3$, $N(60,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.962 & 0.962 & 0.868 & 0.0441|l|Emp. SD & 0.143 & 0.287 & 0.014 & 0.004

[Log-normal frailty, assume gamma]

l|c|c|c|c|

5c$\beta^{0}=\log2$, $N(130,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.665 & 1.188 & 0.199 & 0.2131|l|Emp. SD & 0.073 & 0.249 & 0.019 & 0.0211l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log2$, $N(60,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 0.671 & 1.891 & 0.796 & 0.0791|l|Emp. SD & 0.121 & 0.653 & 0.018 & 0.0121l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log3$, $N(130,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 1.044 & 1.149 & 0.219 & 0.1971|l|Emp. SD & 0.085 & 0.168 & 0.019 & 0.0161l & 1c & 1c & 1c & 1c5c$\beta^{0}=\log3$, $N(60,15^{2})$ censoring2-5 & $\hat{\beta}$ & $\hat{\theta}$ & Censoring & Runtime1|l|Emp. mean & 1.053 & 1.693 & 0.781 & 0.0811|l|Emp. SD & 0.129 & 0.562 & 0.019 & 0.011


