# GSoC 2015 proposal: Multivariate Survival analysis
Test results and proposal for GSoC 2015

See the [proposal](proposal/Monaco-gsoc2015.pdf?raw=true). The completed test is reproduced below.

Simulation results
==================

Simulations were performed with R version 3.1.3 running in an Ubuntu 12.04 desktop with AMD Phenom 9550 Quad-Core 2.20 GHz Processor. All of the simulation results are obtained using penalized partial likelihood estimation, namely the coxph function in the survival package with the Breslow method. Each simulation was repeated 500 times to obtain the empirical mean and SD. The empirical censorship and runtime (in seconds) are also reported. For more information, see Section [sub:Simulation].

See Appendix B of the [proposal](proposal/Monaco-gsoc2015.pdf?raw=true). Tables will be reproduced here soon...

<h1 class="Section">
<a class="toc" name="toc-Appendix-B">B</a> Simulation results
</h1>
<div class="Unindented">
Simulations were performed with R version 3.1.3 running in an Ubuntu 12.04 desktop with AMD Phenom 9550 Quad-Core 2.20 GHz Processor. All of the simulation results are obtained using penalized partial likelihood estimation, namely the coxph function in the survival package with the Breslow method. Each simulation was repeated 500 times to obtain the empirical mean and SD. The empirical censorship and runtime (in seconds) are also reported. For more information, see Section <a class="Reference" href="#sub:Simulation">2.2↑</a>.
</div>
<div class="Indented">
<div class="float">
<a class="Label" name="tab:Assume-constant-frailty"> </a><div class="multitable">
<div class="caption">
Table 4 Ignoring the clustered data: A constant frailty is assumed when the actual frailty is either gamma or log-normal. The coefficients are consistently biased, as this model ignores the clustered data and underestimates the effect of the coefficient. The bias is less severe with greater censorship, likely the result of decreased clustering. There is more diversity at 80% censorship due to fewer individual from the same family being selected, though this conjecture has not been verified.
</div>
<span class="hfill"> </span><span class="float">
<div class="table">
<div class="caption">
(a) Gamma frailty
</div>
<div class="center">
<table>
<tr>
<td align="left" valign="top" colspan="4">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.342
</td>
<td align="center" valign="top">
0.379
</td>
<td align="center" valign="top">
0.017
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.056
</td>
<td align="center" valign="top">
0.024
</td>
<td align="center" valign="top">
0.001
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="4">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.565
</td>
<td align="center" valign="top">
0.883
</td>
<td align="center" valign="top">
0.016
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.128
</td>
<td align="center" valign="top">
0.013
</td>
<td align="center" valign="top">
0.001
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="4">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.541
</td>
<td align="center" valign="top">
0.390
</td>
<td align="center" valign="top">
0.017
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.061
</td>
<td align="center" valign="top">
0.025
</td>
<td align="center" valign="top">
0.001
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="4">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.846
</td>
<td align="center" valign="top">
0.868
</td>
<td align="center" valign="top">
0.016
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.127
</td>
<td align="center" valign="top">
0.014
</td>
<td align="center" valign="top">
0.001
</td>

</tr>

</table>

</div>

</div>

</span>
<span class="hfill"> </span><span class="float">
<div class="table">
<div class="caption">
(b) Log-normal frailty
</div>
<div class="center">
<table>
<tr>
<td align="left" valign="top" colspan="4">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.393
</td>
<td align="center" valign="top">
0.199
</td>
<td align="center" valign="top">
0.016
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.049
</td>
<td align="center" valign="top">
0.019
</td>
<td align="center" valign="top">
0.001
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="4">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.507
</td>
<td align="center" valign="top">
0.796
</td>
<td align="center" valign="top">
0.016
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.094
</td>
<td align="center" valign="top">
0.018
</td>
<td align="center" valign="top">
0.001
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="4">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.630
</td>
<td align="center" valign="top">
0.219
</td>
<td align="center" valign="top">
0.017
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.056
</td>
<td align="center" valign="top">
0.019
</td>
<td align="center" valign="top">
0.001
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="4">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.787
</td>
<td align="center" valign="top">
0.781
</td>
<td align="center" valign="top">
0.016
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.091
</td>
<td align="center" valign="top">
0.019
</td>
<td align="center" valign="top">
0.001
</td>

</tr>

</table>

</div>

</div>

</span>
<span class="hfill"> </span>
</div>

</div>

</div>
<div class="Indented">
<div class="float">
<a class="Label" name="Table-5"> </a><div class="multitable">
<div class="caption">
Table 5 Gamma frailty with a single covariate: The model behaves as anticipated, and correctly estimates the coefficient and frailty distribution variance within error. One confound is the the SD for <span class="formula"><span class="unknown">\bf</span><i>Z</i> ~ <span class="scriptfont">U</span>(0, 1)</span> is closer to that found in <span class="bibcites">[<a class="bibliocite" name="cite-3" href="#biblio-3"><span class="bib-index">3</span></a>]</span>, yet their simulation used covariates from a standard normal.
</div>
<span class="hfill"> </span><span class="float">
<div class="table">
<div class="caption">
(a) Standard normal covariate, 
</div>
<div class="center">
<table>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.686
</td>
<td align="center" valign="top">
1.977
</td>
<td align="center" valign="top">
0.379
</td>
<td align="center" valign="top">
0.199
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.086
</td>
<td align="center" valign="top">
0.276
</td>
<td align="center" valign="top">
0.024
</td>
<td align="center" valign="top">
0.018
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.691
</td>
<td align="center" valign="top">
1.802
</td>
<td align="center" valign="top">
0.883
</td>
<td align="center" valign="top">
0.061
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.169
</td>
<td align="center" valign="top">
1.011
</td>
<td align="center" valign="top">
0.013
</td>
<td align="center" valign="top">
0.009
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
1.090
</td>
<td align="center" valign="top">
1.978
</td>
<td align="center" valign="top">
0.390
</td>
<td align="center" valign="top">
0.191
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.102
</td>
<td align="center" valign="top">
0.277
</td>
<td align="center" valign="top">
0.025
</td>
<td align="center" valign="top">
0.017
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
1.090
</td>
<td align="center" valign="top">
1.879
</td>
<td align="center" valign="top">
0.868
</td>
<td align="center" valign="top">
0.066
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.187
</td>
<td align="center" valign="top">
0.921
</td>
<td align="center" valign="top">
0.014
</td>
<td align="center" valign="top">
0.009
</td>

</tr>

</table>

</div>

</div>

</span>
<span class="hfill"> </span><span class="float">
<div class="table">
<div class="caption">
(b) Uniform covariate
</div>
<div class="center">
<table>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.699
</td>
<td align="center" valign="top">
1.961
</td>
<td align="center" valign="top">
0.320
</td>
<td align="center" valign="top">
0.229
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.246
</td>
<td align="center" valign="top">
0.274
</td>
<td align="center" valign="top">
0.024
</td>
<td align="center" valign="top">
0.020
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.746
</td>
<td align="center" valign="top">
1.837
</td>
<td align="center" valign="top">
0.863
</td>
<td align="center" valign="top">
0.063
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.443
</td>
<td align="center" valign="top">
0.866
</td>
<td align="center" valign="top">
0.015
</td>
<td align="center" valign="top">
0.009
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
1.101
</td>
<td align="center" valign="top">
1.959
</td>
<td align="center" valign="top">
0.294
</td>
<td align="center" valign="top">
0.244
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.248
</td>
<td align="center" valign="top">
0.265
</td>
<td align="center" valign="top">
0.024
</td>
<td align="center" valign="top">
0.020
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
1.146
</td>
<td align="center" valign="top">
1.843
</td>
<td align="center" valign="top">
0.841
</td>
<td align="center" valign="top">
0.069
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.430
</td>
<td align="center" valign="top">
0.729
</td>
<td align="center" valign="top">
0.016
</td>
<td align="center" valign="top">
0.010
</td>

</tr>

</table>

</div>

</div>

</span>
<span class="hfill"> </span>
</div>

</div>

</div>
<div class="Indented">
<div class="float">
<a class="Label" name="Table-6"> </a><div class="multitable">
<div class="caption">
Table 6 Gamma frailty with two covariates: Again, the coefficients and frailty variance are correctly estimated within error.
</div>
<span class="hfill"> </span><span class="float">
<div class="table">
<div class="caption">
(a) Standard normal covariate
</div>
<div class="center">
<table>
<tr>
<td align="left" valign="top" colspan="6">
<span class="formula"><i>β</i><sub>0</sub> = log2</span>, <span class="formula"><i>β</i><sub>1</sub> = log3</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i><sub>0</sub></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i><sub>1</sub></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.692
</td>
<td align="center" valign="top">
1.099
</td>
<td align="center" valign="top">
1.959
</td>
<td align="center" valign="top">
0.395
</td>
<td align="center" valign="top">
0.264
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.086
</td>
<td align="center" valign="top">
0.100
</td>
<td align="center" valign="top">
0.281
</td>
<td align="center" valign="top">
0.024
</td>
<td align="center" valign="top">
0.021
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="6">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>β</i><sub>1</sub> = log3</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i><sub>0</sub></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i><sub>1</sub></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.687
</td>
<td align="center" valign="top">
1.100
</td>
<td align="center" valign="top">
1.857
</td>
<td align="center" valign="top">
0.860
</td>
<td align="center" valign="top">
0.082
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.161
</td>
<td align="center" valign="top">
0.176
</td>
<td align="center" valign="top">
0.873
</td>
<td align="center" valign="top">
0.015
</td>
<td align="center" valign="top">
0.013
</td>

</tr>

</table>

</div>

</div>

</span>
<span class="hfill"> </span>
</div>

</div>

</div>
<div class="Indented">
<div class="float">
<a class="Label" name="Table-7"> </a><div class="multitable">
<div class="caption">
Table 7 Log-normal frailty with a single covariate: With <span class="formula"><i>θ</i> = 2</span>, the log-normal has a heavier tail than the gamma, and thus more clustering. As a result, with high censorship, the coefficients and frailty variance tend to by slightly underestimated. Similar to the gamma frailty, the error for uniformly-distributed individual covariates is higher than standard normal individual covariates.
</div>
<span class="hfill"> </span><span class="float">
<div class="table">
<div class="caption">
(a) Standard normal covariate
</div>
<div class="center">
<table>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.671
</td>
<td align="center" valign="top">
1.808
</td>
<td align="center" valign="top">
0.199
</td>
<td align="center" valign="top">
0.196
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.071
</td>
<td align="center" valign="top">
0.296
</td>
<td align="center" valign="top">
0.019
</td>
<td align="center" valign="top">
0.014
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.600
</td>
<td align="center" valign="top">
1.130
</td>
<td align="center" valign="top">
0.796
</td>
<td align="center" valign="top">
0.054
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.105
</td>
<td align="center" valign="top">
0.265
</td>
<td align="center" valign="top">
0.018
</td>
<td align="center" valign="top">
0.006
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
1.061
</td>
<td align="center" valign="top">
1.802
</td>
<td align="center" valign="top">
0.219
</td>
<td align="center" valign="top">
0.184
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.085
</td>
<td align="center" valign="top">
0.292
</td>
<td align="center" valign="top">
0.019
</td>
<td align="center" valign="top">
0.012
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.953
</td>
<td align="center" valign="top">
1.162
</td>
<td align="center" valign="top">
0.781
</td>
<td align="center" valign="top">
0.058
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.106
</td>
<td align="center" valign="top">
0.269
</td>
<td align="center" valign="top">
0.019
</td>
<td align="center" valign="top">
0.006
</td>

</tr>

</table>

</div>

</div>

</span>
<span class="hfill"> </span><span class="float">
<div class="table">
<div class="caption">
(b) Uniform covariate
</div>
<div class="center">
<table>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.683
</td>
<td align="center" valign="top">
1.889
</td>
<td align="center" valign="top">
0.141
</td>
<td align="center" valign="top">
0.223
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.224
</td>
<td align="center" valign="top">
0.296
</td>
<td align="center" valign="top">
0.017
</td>
<td align="center" valign="top">
0.016
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.630
</td>
<td align="center" valign="top">
1.164
</td>
<td align="center" valign="top">
0.763
</td>
<td align="center" valign="top">
0.062
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.347
</td>
<td align="center" valign="top">
0.253
</td>
<td align="center" valign="top">
0.020
</td>
<td align="center" valign="top">
0.007
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
1.084
</td>
<td align="center" valign="top">
1.922
</td>
<td align="center" valign="top">
0.120
</td>
<td align="center" valign="top">
0.234
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.227
</td>
<td align="center" valign="top">
0.304
</td>
<td align="center" valign="top">
0.015
</td>
<td align="center" valign="top">
0.018
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.989
</td>
<td align="center" valign="top">
1.199
</td>
<td align="center" valign="top">
0.733
</td>
<td align="center" valign="top">
0.068
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.331
</td>
<td align="center" valign="top">
0.252
</td>
<td align="center" valign="top">
0.021
</td>
<td align="center" valign="top">
0.008
</td>

</tr>

</table>

</div>

</div>

</span>
<span class="hfill"> </span>
</div>

</div>

</div>
<div class="Indented">
<div class="float">
<a class="Label" name="tab:Assume-the-wrong"> </a><div class="multitable">
<div class="caption">
Table 8 Assuming the wrong frailty: When the true frailty is log-normal and we assume a gamma distribution, the coefficients are underestimated. This effect is pronounced for higher censorship. This is a result of underestimating how much the data are clustered, since the log-normal has a heavier tail and produces more clustered data. Underestimation is not as severe when the true frailty is gamma and a log-normal is assumed. In this case, we assume the data is more clustered that it actually is.
</div>
<span class="hfill"> </span><span class="float">
<div class="table">
<div class="caption">
(a) Gamma frailty, assume log-normal
</div>
<div class="center">
<table>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.615
</td>
<td align="center" valign="top">
2.050
</td>
<td align="center" valign="top">
0.379
</td>
<td align="center" valign="top">
0.139
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.077
</td>
<td align="center" valign="top">
0.291
</td>
<td align="center" valign="top">
0.024
</td>
<td align="center" valign="top">
0.012
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.620
</td>
<td align="center" valign="top">
0.866
</td>
<td align="center" valign="top">
0.883
</td>
<td align="center" valign="top">
0.041
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.140
</td>
<td align="center" valign="top">
0.304
</td>
<td align="center" valign="top">
0.013
</td>
<td align="center" valign="top">
0.003
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.979
</td>
<td align="center" valign="top">
2.111
</td>
<td align="center" valign="top">
0.390
</td>
<td align="center" valign="top">
0.136
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.091
</td>
<td align="center" valign="top">
0.304
</td>
<td align="center" valign="top">
0.025
</td>
<td align="center" valign="top">
0.011
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.962
</td>
<td align="center" valign="top">
0.962
</td>
<td align="center" valign="top">
0.868
</td>
<td align="center" valign="top">
0.044
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.143
</td>
<td align="center" valign="top">
0.287
</td>
<td align="center" valign="top">
0.014
</td>
<td align="center" valign="top">
0.004
</td>

</tr>

</table>

</div>

</div>

</span>
<span class="hfill"> </span><span class="float">
<div class="table">
<div class="caption">
(b) Log-normal frailty, assume gamma
</div>
<div class="center">
<table>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.665
</td>
<td align="center" valign="top">
1.188
</td>
<td align="center" valign="top">
0.199
</td>
<td align="center" valign="top">
0.213
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.073
</td>
<td align="center" valign="top">
0.249
</td>
<td align="center" valign="top">
0.019
</td>
<td align="center" valign="top">
0.021
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log2</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
0.671
</td>
<td align="center" valign="top">
1.891
</td>
<td align="center" valign="top">
0.796
</td>
<td align="center" valign="top">
0.079
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.121
</td>
<td align="center" valign="top">
0.653
</td>
<td align="center" valign="top">
0.018
</td>
<td align="center" valign="top">
0.012
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(130, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
1.044
</td>
<td align="center" valign="top">
1.149
</td>
<td align="center" valign="top">
0.219
</td>
<td align="center" valign="top">
0.197
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.085
</td>
<td align="center" valign="top">
0.168
</td>
<td align="center" valign="top">
0.019
</td>
<td align="center" valign="top">
0.016
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>
<td align="center" valign="top">

</td>

</tr>
<tr>
<td align="left" valign="top" colspan="5">
<span class="formula"><i>β</i><sup>0</sup> = log3</span>, <span class="formula"><i>N</i>(60, 15<sup>2</sup>)</span> censoring
</td>

</tr>
<tr>
<td align="left" valign="top">

</td>
<td align="center" valign="top">
<span class="formula"><i>β̂</i></span>
</td>
<td align="center" valign="top">
<span class="formula"><i>θ̂</i></span>
</td>
<td align="center" valign="top">
Censoring
</td>
<td align="center" valign="top">
Runtime
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. mean
</td>
<td align="center" valign="top">
1.053
</td>
<td align="center" valign="top">
1.693
</td>
<td align="center" valign="top">
0.781
</td>
<td align="center" valign="top">
0.081
</td>

</tr>
<tr>
<td align="left" valign="top">
Emp. SD
</td>
<td align="center" valign="top">
0.129
</td>
<td align="center" valign="top">
0.562
</td>
<td align="center" valign="top">
0.019
</td>
<td align="center" valign="top">
0.011
</td>

</tr>

</table>

</div>

</div>

</span>
<span class="hfill"> </span>
</div>

</div>

</div>
<div class="Indented">
<p><br/>
</p>

</div>
