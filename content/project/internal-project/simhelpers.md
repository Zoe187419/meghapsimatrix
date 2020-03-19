---
title: simhelpers
author: "Megha Joshi"
date: '2020-03-04'
slug: simhelpers
categories: [Project]
tags: [package, R]
description: 'A package to help with simulation studies'
---

[Here](https://meghapsimatrix.github.io/simhelpers/index.html) is the website for the package. 

Simulations are experiments to study the performance of statistical methods under known data-generating conditions (Morris, White & Crowther, 2018). Methodologists examine questions like: (1) how does ordinary least squares (OLS) regression perform if errors are heteroskedastic? (2) how does the presence of missing data affect treatment effect estimates from a propensity score analysis? (3) how does cluster robust variance estimation perform when the number of clusters is small? To answer such questions, we conduct experiments by simulating thousands of datasets from pseudo-random sampling (Morris et al., 2018). 

The goal of `simhelpers` is to assist in running simulation studies. This package provides a set of functions that calculates various performance measures like bias, root mean squared error, rejection rates, and also calculates the associated Monte Carlo standard errors (MCSE). These functions are divided into three major categories of performance criteria: absolute criteria, relative criteria, and criteria to evaluate hypothesis testing. The functions are created to work with the [`tidyeval`](https://tidyeval.tidyverse.org/index.html) practice. 

In addition to the set of functions that calculates performance measures and MCSE, the package also includes a function, `create_skeleton()`, that generates a skeleton outline of a simulation study that can be applied when designing and conducting one. Another function, `evaluate_by_row()`, runs the simulation for each combination of conditions row by row and implements the [`future_pmap()`](https://davisvaughan.github.io/furrr/reference/future_map2.html) function from the [`furrr`](https://davisvaughan.github.io/furrr/) package to run the simulation in parallel. The package also contains several datasets that contain results from example simulation studies. 


## Installation

You can install the development version from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("meghapsimatrix/simhelpers")
```