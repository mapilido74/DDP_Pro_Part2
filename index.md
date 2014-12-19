--- 
title       : Tooth Growth 
subtitle    : Some Exploratory Analysis
author      : Pilar Liria
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [ggplot2, psych, datasets, xtable, RColorBrewer]  
ext_widgets : {rCharts: libraries/nvd3} 
mode        : selfcontained # {standalone, draft}
--- 

## Introduction

This document analyzes the **ToothGrowth** data in the R datasets pacakage. The goal of  this report is to show the effect of vitamina C on Tooth Growth in guinea pigs. 

The document includes multiBarchar (instead of Boxplot)  and some summary reports related with the data. 

## Data

The data **ToothGrowth**, consists in 60 observations of 3 variables. The variables are:

1. *len* which is tooth length (it is the *response variable*)
2. *supp* is the way in which the supplement was administered. The levels are *OJ (as orange juice)*, and *VC (as ascorbic acid)*.
3. *dose* of the supplement in miligrams (0.5, 1.0, and 2.0)

---

### MultiBarChart: Tooth Length and the Effect of Vitamin C

<iframe src=' assets/fig/unnamed-chunk-1-1.html ' scrolling='no' frameBorder='0' seamless class='rChart nvd3 ' id=iframe- chart17682a91e00 ></iframe> <style>iframe.rChart{ width: 100%; height: 400px;}</style>

The graph shows some kind of trend. It looks like as the dose is increased , the tooth length is bigger. When the dose is 0.5 miligrams or 1 miligrams, the length of the tooth with OJ supplement  looks  biger. However if the supplement is 2.0 miligrams, the contrary occurs. 

---

### Summary: describeBy

<!-- html table generated in R 3.1.2 by xtable 1.7-4 package -->
<!-- Fri Dec 19 13:34:03 2014 -->
<table border=1>
<tr> <th>  </th> <th> item </th> <th> group1 </th> <th> group2 </th> <th> vars </th> <th> n </th> <th> mean </th> <th> sd </th> <th> median </th>  </tr>
  <tr> <td align="right"> 11 </td> <td> 1 </td> <td> OJ </td> <td> 0.5 </td> <td align="right"> 1.00 </td> <td align="right"> 10.00 </td> <td align="right"> 13.23 </td> <td align="right"> 4.46 </td> <td align="right"> 12.25 </td> </tr>
  <tr> <td align="right"> 12 </td> <td> 2 </td> <td> VC </td> <td> 0.5 </td> <td align="right"> 1.00 </td> <td align="right"> 10.00 </td> <td align="right"> 7.98 </td> <td align="right"> 2.75 </td> <td align="right"> 7.15 </td> </tr>
  <tr> <td align="right"> 13 </td> <td> 3 </td> <td> OJ </td> <td> 1 </td> <td align="right"> 1.00 </td> <td align="right"> 10.00 </td> <td align="right"> 22.70 </td> <td align="right"> 3.91 </td> <td align="right"> 23.45 </td> </tr>
  <tr> <td align="right"> 14 </td> <td> 4 </td> <td> VC </td> <td> 1 </td> <td align="right"> 1.00 </td> <td align="right"> 10.00 </td> <td align="right"> 16.77 </td> <td align="right"> 2.52 </td> <td align="right"> 16.50 </td> </tr>
  <tr> <td align="right"> 15 </td> <td> 5 </td> <td> OJ </td> <td> 2 </td> <td align="right"> 1.00 </td> <td align="right"> 10.00 </td> <td align="right"> 26.06 </td> <td align="right"> 2.66 </td> <td align="right"> 25.95 </td> </tr>
  <tr> <td align="right"> 16 </td> <td> 6 </td> <td> VC </td> <td> 2 </td> <td align="right"> 1.00 </td> <td align="right"> 10.00 </td> <td align="right"> 26.14 </td> <td align="right"> 4.80 </td> <td align="right"> 25.95 </td> </tr>
   </table>
<!-- html table generated in R 3.1.2 by xtable 1.7-4 package -->
<!-- Fri Dec 19 13:34:03 2014 -->
<table border=1>
<tr> <th>  </th> <th> trimmed </th> <th> mad </th> <th> min </th> <th> max </th> <th> range </th> <th> skew </th> <th> kurtosis </th>  </tr>
  <tr> <td align="right"> 11 </td> <td align="right"> 12.82 </td> <td align="right"> 4.30 </td> <td align="right"> 8.20 </td> <td align="right"> 21.50 </td> <td align="right"> 13.30 </td> <td align="right"> 0.44 </td> <td align="right"> -1.37 </td> </tr>
  <tr> <td align="right"> 12 </td> <td align="right"> 8.01 </td> <td align="right"> 3.56 </td> <td align="right"> 4.20 </td> <td align="right"> 11.50 </td> <td align="right"> 7.30 </td> <td align="right"> 0.13 </td> <td align="right"> -1.81 </td> </tr>
  <tr> <td align="right"> 13 </td> <td align="right"> 23.15 </td> <td align="right"> 3.93 </td> <td align="right"> 14.50 </td> <td align="right"> 27.30 </td> <td align="right"> 12.80 </td> <td align="right"> -0.68 </td> <td align="right"> -0.68 </td> </tr>
  <tr> <td align="right"> 14 </td> <td align="right"> 16.45 </td> <td align="right"> 1.70 </td> <td align="right"> 13.60 </td> <td align="right"> 22.50 </td> <td align="right"> 8.90 </td> <td align="right"> 0.93 </td> <td align="right"> 0.08 </td> </tr>
  <tr> <td align="right"> 15 </td> <td align="right"> 25.91 </td> <td align="right"> 2.08 </td> <td align="right"> 22.40 </td> <td align="right"> 30.90 </td> <td align="right"> 8.50 </td> <td align="right"> 0.37 </td> <td align="right"> -1.09 </td> </tr>
  <tr> <td align="right"> 16 </td> <td align="right"> 26.12 </td> <td align="right"> 4.60 </td> <td align="right"> 18.50 </td> <td align="right"> 33.90 </td> <td align="right"> 15.40 </td> <td align="right"> 0.16 </td> <td align="right"> -1.23 </td> </tr>
   </table>

---

### Summary: summary

<!-- html table generated in R 3.1.2 by xtable 1.7-4 package -->
<!-- Fri Dec 19 10:33:10 2014 -->
<table border=1>
<tr> <th>  </th> <th>      len </th> <th> supp </th> <th>      dose </th>  </tr>
  <tr> <td align="right"> 1 </td> <td> Min.   : 4.20   </td> <td> OJ:30   </td> <td> Min.   :0.500   </td> </tr>
  <tr> <td align="right"> 2 </td> <td> 1st Qu.:13.07   </td> <td> VC:30   </td> <td> 1st Qu.:0.500   </td> </tr>
  <tr> <td align="right"> 3 </td> <td> Median :19.25   </td> <td>  </td> <td> Median :1.000   </td> </tr>
  <tr> <td align="right"> 4 </td> <td> Mean   :18.81   </td> <td>  </td> <td> Mean   :1.167   </td> </tr>
  <tr> <td align="right"> 5 </td> <td> 3rd Qu.:25.27   </td> <td>  </td> <td> 3rd Qu.:2.000   </td> </tr>
  <tr> <td align="right"> 6 </td> <td> Max.   :33.90   </td> <td>  </td> <td> Max.   :2.000   </td> </tr>
   </table>



