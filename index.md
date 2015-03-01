---
title       : Statistical Computing using R
subtitle    : 
author      : Joe Bragg
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## R in Industry

[Gartner Survey Reveals That 73 Percent of Organizations Have Invested or Plan to Invest in Big Data in the Next Two Years](http://www.gartner.com/newsroom/id/2848718)

[Microsoft to acquire R language powerhouse Revolution Analytics](http://www.infoworld.com/article/2874853/big-data/microsoft-to-acquire-r-language-powerhouse-revolution-analytics.html)
 
[Big data: The next frontier for competition](http://www.mckinsey.com/features/big_data)

--- .class #id 

## Uses of R in Supply Chain

Here are just a few potential uses for R in Supply Chain

- Process improvement including support for Six Sigma  
- Forecasting & inventory planning
- Supplier analysis
- Finding & reducing sources of churn
- Identifying root causes for delays & issues

---.segue .dark

## Overview of R

---

## Commonly used R Packages - Data Manipulation

Package       | Description
------------- | -------------
data.table    | Fast aggregation of large data, fast ordered joins, fast add/modify/delete of columns by group using no copies at all, list columns and a fast file reader.
plyr          | Set of tools that solves a common set of problems: you need to break a big problem down into manageable pieces, operate on each pieces and then put all the pieces back together.
reshape2      | Restructure and aggregate data using just two functions: melt and dcast (or acast).
Hmisc         | Functions useful for data analysis, high-level graphics, utility operations, functions for computing sample size and power, importing datasets, imputing missing values, advanced table making, variable clustering, character string manipulation, conversion of R objects to LaTeX code, and recoding variables.

---

## Commonly used R Packages - Date/Time Formating

Package       | Description
------------- | -------------
lubridate     |Provides functions to identify and parse date-time data, extract and modify components of a date-time (years, months, days, hours, minutes, and seconds), perform accurate math on date-times, handle time zones and Daylight Savings Time.

---

## Commonly used R Packages - Graphics

Package       | Description
------------- | -------------
lattice       | high-level data visualization system, with an emphasis on multivariate data, that is sufficient for typical graphics needs, and is also flexible enough to handle most nonstandard requirements.
ggplot2       | An implementation of the grammar of graphics in R. It combines the advantages of both base and lattice graphics: conditioning and shared axes are handled automatically, and you can still build up a plot step by step from multiple data sources. It also implements a sophisticated multidimensional conditioning system and a consistent interface to map data to aesthetic attributes.

---

## Commonly used R Packages - Machine Learning

Package       | Description
------------- | -------------
caret         | Functions for training and plotting classification and regression models.

---

## Basic Data Types


```r
c(1,2,5.3,6,-2,4) # numeric vector
```

```
## [1]  1.0  2.0  5.3  6.0 -2.0  4.0
```

```r
c("one","two","three") # character vector
```

```
## [1] "one"   "two"   "three"
```

```r
c(TRUE,TRUE,TRUE,FALSE,TRUE,FALSE) #logical vector
```

```
## [1]  TRUE  TRUE  TRUE FALSE  TRUE FALSE
```

---

## Matrices


```r
matrix(c(1,2,3,4,5,6,7,8,9), nrow=3, ncol=3, byrow=FALSE, dimnames=list(c("Row1","Row2","Row3"), c("Col1","Col2","Col3")))
```

```
##      Col1 Col2 Col3
## Row1    1    4    7
## Row2    2    5    8
## Row3    3    6    9
```

---

## Data.Frames


```r
d <- c(1,2,1/0,NaN)
e <- c("red", "white", "blue", NA)
f <- c(TRUE,TRUE,TRUE,FALSE)
mydata <- data.frame(d,e,f)
names(mydata) <- c("ID","Color","Passed") # variable names
mydata
```

```
##    ID Color Passed
## 1   1   red   TRUE
## 2   2 white   TRUE
## 3 Inf  blue   TRUE
## 4 NaN  <NA>  FALSE
```

---

## Lists


```r
list(colors=e, numbers=d, mydf=mydata, bam="tada")
```

```
## $colors
## [1] "red"   "white" "blue"  NA     
## 
## $numbers
## [1]   1   2 Inf NaN
## 
## $mydf
##    ID Color Passed
## 1   1   red   TRUE
## 2   2 white   TRUE
## 3 Inf  blue   TRUE
## 4 NaN  <NA>  FALSE
## 
## $bam
## [1] "tada"
```

---

## Command Syntax


```r
plot(cars)
```

![plot of chunk unnamed-chunk-5](assets/fig/unnamed-chunk-5-1.png) 

---.segue .dark

## RStudio Navigation

