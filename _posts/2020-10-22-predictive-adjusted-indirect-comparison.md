---
layout: post
title: Predictive-adjusted indirect comparison
---

<p align="justify">My paper, <a href="https://arxiv.org/abs/2008.05951">Predictive-Adjusted Indirect Comparison: A Novel Method for Population Adjustment with Limited Access to Patient-Level Data</a>, 
co-authored with my PhD supervisors <a href="http://www.statistica.it/gianluca/">Gianluca Baio</a> and <a href="https://sites.google.com/site/annaheathstats/">Anna Heath</a>, 
is up on arXiv. In this article, we present a novel regression adjustment-based method, predictive-adjusted indirect comparison (PAIC), for population adjustment in indirect treatment comparisons. Population-adjusted indirect treatment comparisons such as matching-adjusted indirect comparison (MAIC) and simulated treatment comparison (STC) are 
increasingly used to compare treatments in health technology assessments. Such methods estimate treatment effects when there are differences in effect modifiers 
across studies and when access to patient-level data is limited.</p> 

<p align="justify">Currently available methods have some limitations. MAIC is based on propensity score weighting and is highly sensitive to poor covariate overlap, in which case it is prone 
to extreme weights, large reductions in effective sample size and imprecision, issues that are a pervasive problem in health technology appraisals.  Regression adjustment 
methods hold promise because they can extrapolate beyond the covariate space observed in the patient-level data where overlap is insufficient, using the linearity assumption
or other appropriate assumptions about the input space, and may increase precision and statistical power with respect to propensity score-based methodologies. 
Current regression adjustment approaches, e.g. STC, are systematically biased because they target a conditional treatment effect as opposed to a marginal or population-average
treatment effect, which should be the target estimand. This is problematic because it leads to the incompatibility of estimands in the indirect comparison where the 
measure of effect is non-collapsible. Most applications of population-adjusted indirect comparisons are in oncology and are typically concerned with non-collapsible 
measures of treatment effect such as (log) hazard ratios or (log) odds ratios.</p>  

<p align="justify">To overcome these limitations, we develop a novel method based on multiple imputation called predictive-adjusted indirect comparison (PAIC). The novelty 
of PAIC is that it is a regression adjustment method, which targets a marginal treatment effect. It proceeds by splitting the adjustment into two separate stages: the generation
of synthetic datasets and their analysis. We report on the results of a comprehensive simulation study, which extensively benchmarks the performance of two versions of PAIC 
against MAIC across 162 scenarios with binary outcomes and binary covariates, using the log-odds ratio as the measure of effect. Even though the sample sizes and the degree 
of overlap between the studies' covariate distributions are reasonable in the simulation scenarios, and MAIC is likely to perform well, PAIC achieves greater precision and 
accuracy than MAIC, and is generally unbiased. The differences between both methodologies in precision and accuracy are exacerbated when the scenarios are less favorable, 
e.g. where covariate overlap is poor and when sample sizes are small.</p> 

<p align="justify">PAIC is a timely addition which can be used where strong covariate imbalances lead to a marked loss of precision in MAIC.  PAIC and MAIC use different adjustment mechanisms and considering their results jointly may be helpful to evaluate the robustness of analyses. Even though PAIC has been developed in a very specific context, common in health technology assessment, where access to patient-level data is limited and an indirect comparison is required, its principles are applicable to estimate marginal or population-average treatment effects in any situation which requires generalizing or transporting the results of a randomized experiment to a specific target population. The generalization or transportability of marginal treatment effects across populations is an increasingly important research area in causal inference.</p> 

![PAIC-dag]({{site.baseurl}}/images/PAIC_dag.png "A directed acyclic graph representing predictive-adjusted indirect comparison and accounting for its two main
stages: (1) synthetic data generation; and (2) the analysis of synthetic datasets."){:class="img-responsive"}
![PAIC-mse]({{site.baseurl}}/images/PAIC_mse.png "Mean square error across all simulation scenarios."){:class="img-responsive"}
