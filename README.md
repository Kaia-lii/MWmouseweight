
<!-- README.md is generated from README.Rmd. Please edit that file -->

# MWMouseWeight

<!-- badges: start -->
<!-- badges: end -->

MWMouseWeight is an R package designed to streamline the data cleaning,
preparation, and initial analysis process for experimental datasets,
which in this case particularly involves mice body weight and treatment
outcomes. This package addresses common data inconsistencies, enables
efficient wrangling, and provides key visualizations and summaries for
further exploration.

Why Should I Use This Package? MW offers several benefits, including
automated cleaning to resolve typographical errors, correct non-numeric
entries, and standardize labels. This package facilitates consistent
wrangling, transforming datasets into analysis-ready formats with
intuitive functions. Another insightful tool included is visualizations
using plots, which allows users to quickly plot trends and summarize key
statistics, saving time and reducing errors in the preprocessing stage.

## About the data

Data was made available by Professor James Xenakis in Harvard’s
Statistics 108 course. The MWMouseWeight package cleans the data and
removes faulty mice, as detailed in the dataset.r file. Specifically,
with the data wrangling portion of MWMouseweight, the following concerns
are addressed: first, the inconsistencies of naming styles and data
collection was solved (for example, inconsistent naming of treatment
(‘Tmt’, Trmt) was standardized and made uniform across the mice. The
issues were prevalent throughout the dataset, including in the names of
columns. Next, ineligible mice (those who had died or experienced a body
weight decrease of 20 percent or more) were removed from the dataset.
Lastly, the scattered data was aggregated into one final dataset.
Ultimately, the MWMouseWeight contains four datasets. Ultimately, the
MWMouseWeight contains four datasets. While more information can be
found regarding the datasets in the documentation of the dataset, here
is a quick summary the datasets and what they contain:

The first dataset is called ‘birth_data’, and it contains mostly
identification information about the mice in the study.

The second dataset is ‘bodyweight_data’, which contains information on
how the mice’s bodyweight changed over the three checkpoints. It also
contains the dates of each checkpoint.

The third dataset is called ‘outcome_data’. Since MWMouseWeight
primarily focuses on the body weight of the mice, this dataset is not
the most relavent for the functionality of the dataset.

The fourth dataset is ‘merged_data’, which is all of these three
datasets joined on mouse ID.

## Installation

You can install the development version of MWMouseWeight like so:

``` r
install.packages("devtools")
devtools::install_github("yourusername/MWMouseWeight")
```

## Example

This is a basic example which shows you how to solve a common problem:

For visualization, you can use the `plot_mouse_weight()` function to
visualize body weight trends over time. More detailed examples and
extended analyses can be found in the package vignette.

``` r
library(MWMouseWeight)
## basic example code
plot_mouse_weight(merged_data)
```

<img src="man/figures/README-example-1.png" width="100%" />
