# mfishtools

R functions for gene selection and analysis of mFISH data

mfishtools includes many functions that are used for analysis of data for the CZI SpaceTx 
project, and mostly relies on correlation-based analysis with filtering.

Install using:
```
devtools::install_github("AllenInstitute/mfishtools",auth_token="802976690281f1483c40de46d0a07e9d01a3de08")
```










#### Notes for package generation:

1) Github.  
== Get an AllenInstitute account  
== Build a blank repository  
== Add an authentication token for your personal account (check the "repo" box)  

2) Reading.
== Rstudio package with git: https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN  
== roxygen2 https://cran.r-project.org/web/packages/roxygen2/vignettes/roxygen2.html  
== building an R package: https://www.r-bloggers.com/building-a-package-in-rstudio-is-actually-very-easy/ (quick)  
== building an R package: http://r-pkgs.had.co.nz/ (complete)  

3) Start an R Studio project with version control (see top link in #2)  
== Link this package to the blank repo from #1  
== Note that if you want to use a network drive on windows, you need to map it  
   first (https://www.laptopmag.com/articles/map-network-drive-windows-10)  

4) Copy all of your relevant functions to the R directory  

5) Format your function annotations correctly so roxygen2 can make all the man files for you.  For example:  
```
#' Confusion matrix
#'
#' This function returns a table of the top confused clusters (assigned clusters incorrectly mapped)
#'
#' @param confusionProp confusion matrix (e.g., output from getConfusionMatrix).
#' @param count number of top confusions to show
#'
#' @return a 3 x count matrix of the top confused pairs of clusters with the three columns corresponding
#'   to mapped cluster, assigned cluster, and fraction of cells incorrectly mapped, respectively.
#'
confusion <- function()
{
  # function code here
}
```

6) Build the package  
