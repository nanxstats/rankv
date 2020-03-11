# vaers-ebgm <img src="https://i.imgur.com/pDHoFo7.png" align="right" alt="logo" height="180" width="180" />

[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
![License: MIT](https://img.shields.io/github/license/nanxstats/bcpm-msaenet.svg)

Detecting Potential Safety Signals in 30 Years of VAERS Data with openEBGM. Solution for the precisionFDA "[Gaining New Insights by Detecting Adverse Event Anomalies Using FDA Open Data challenge](https://precision.fda.gov/challenges/9)" using [openEBGM](https://cran.r-project.org/package=openEBGM).

This solution verifies the concept that by harnessing the power of open data and high-quality open source data analysis software, we can quickly develop new analytical approaches and flexible pipelines for extracting new insights from public health information, and present both of the process and the results to the community, thus increase computational transparency and reproduciblity.

## Model

This solution features the following model and data to detect safety signals and adverse event anomalies from the [Vaccine Adverse Event Reporting System (VAERS)](https://vaers.hhs.gov/):

- All domestic VAERS data, year 1990 - 2019 (until 2019-12-14).
- Signal detection with the Gamma-Poisson Shrinker (GPS) model ([Xiao and Xu, 2015](https://www.tandfonline.com/doi/full/10.1080/00949655.2015.1016944)).
- A DEoptim method ([Meinshausen and Bühlmann, 2010](https://doi.org/10.1111/j.1467-9868.2010.00740.x))  was used to optimize the parameters

## Reproduce the results

- To run the code for generating the submission, open `run.R` and follow the steps. All R packages dependencies can be installed from CRAN directly.
- To compile the [website](https://nanx.me/vaers-ebgm/), use `rmarkdown::render_site()`. Alternatively, open the project in RStudio and click "Build Website" in the "Build" panel.
