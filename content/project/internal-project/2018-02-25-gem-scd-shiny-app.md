---
title: simhelpers
author: "Megha Joshi"
date: '2020-03-04'
slug: simhelpers
categories: [Project]
tags: [package, R]
description: 'A package to help with simulation studies'
---

Simulations are experiments to study the performance of statistical methods under known data-generating conditions (Morris, White & Crowther, 2018). Methodologists examine questions like: (1) how does ordinary least squares (OLS) regression perform if errors are heteroskedastic? (2) how does the presence of missing data affect treatment effect estimates from a propensity score analysis? (3) how does robust variance estimation perform when sample size is small? To answer such questions, we conduct experiments by simulating thousands of datasets from pseudo-random sampling (Morris et al., 2018). 

The goal of [`simhelpers`](https://meghapsimatrix.github.io/simhelpers/index.html) is to assist in running simulation studies. This package provides a set of functions that calculates various performance measures like bias, root mean squared error, rejection rates, and also calculates the associated Monte Carlo standard errors (MCSE). These functions are divided into broad four categories: absolute criteria, relative criteria, rejection rate, and confidence interval coverage. The functions are created to work with `tidyeval` practice using packages like `dplyr`. 

In addition to the set of functions that calculates performance measures and MCSE, the package also includes a function, `create_skeleton()`, that generates a skeleton outline of a simulation study that can be applied when designing and conducting one. Another function, `evaluate_by_row()` runs the simulation for each combination of conditions row by row and implements the `future_pmap()` function from the `furrr` package to run the simulation in parallel. The package also contains several datasets that contain results from example simulation studies. 


## Installation

You can install the development version from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("meghapsimatrix/simhelpers")
```