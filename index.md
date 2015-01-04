--- 
title       : Tooth Growth 
subtitle    : Some Exploratory Analysis
author      : Pilar Liria
job         : 
framework   : io2012        
highlighter : highlight.js 
hitheme     : tomorrow      
widgets     : [ggplot2, psych, datasets, reshape, xtable, RColorBrewer]  
ext_widgets : {rCharts: ["libraries/nvd3", "libraries/highlights"]} 
mode        : selfcontained # {standalone, draft}

--- .outfont

## Introduction 

The issue is to answer the next question: Vitamin C affects the growth of teeth?

The shiny app allows the user to choose some information as dose or supp or both and obtain the boxplot which describes the behaviour of the tooth length under these variables.  In addition the user can choose the option which describes general  statistics or statistitics of the length of the tooth (len) grouped by the doses and the way in which the supplement was administered (supp).

The shiny app is in: "https://mapilido74.shinyapps.io/ProjectFinal/".

Also in this presentation I show an interactive plot which related the 3 variables in study (len, dose and supp).

## Data

The data **ToothGrowth** in R package, consists in 60 observations of 3 variables related with guinea pigs and the growth of its tooth under the incluence of Vitamin C:

1. *len* which is tooth length (it is the *response variable*)
2. *supp* is the way in which the supplement was administered. The levels are *OJ (as orange juice)*, and *VC (as ascorbic acid)*.
3. *dose* of the supplement in miligrams (0.5, 1.0, and 2.0). 

--- 

### Processig Data: Tooth Length and the Effect of Vitamin C

<link rel='stylesheet' href=http://nvd3.org/assets/css/nv.d3.css>
<script type='text/javascript' src=http://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js></script>
<script type='text/javascript' src=http://d3js.org/d3.v3.min.js></script>
<script type='text/javascript' src=http://timelyportfolio.github.io/rCharts_nvd3_tests/libraries/widgets/nvd3/js/nv.d3.min-new.js></script>
<script type='text/javascript' src=http://nvd3.org/assets/lib/fisheye.js></script> 
 <style>
  .rChart {
    display: block;
    margin-left: auto; 
    margin-right: auto;
    width: 800px;
    height: 400px;
  }  
  </style>
<div id = 'chart1' class = 'rChart nvd3'></div>
<script type='text/javascript'>
 $(document).ready(function(){
      drawchart1()
    });
    function drawchart1(){  
      var opts = {
 "dom": "chart1",
"width":    800,
"height":    400,
"x": "dose",
"y": "len",
"group": "supp",
"type": "multiBarChart",
"id": "chart1" 
},
        data = [
 {
 "len":            4.2,
"supp": "VC",
"dose": "0.5" 
},
{
 "len":           11.5,
"supp": "VC",
"dose": "0.5" 
},
{
 "len":            7.3,
"supp": "VC",
"dose": "0.5" 
},
{
 "len":            5.8,
"supp": "VC",
"dose": "0.5" 
},
{
 "len":            6.4,
"supp": "VC",
"dose": "0.5" 
},
{
 "len":             10,
"supp": "VC",
"dose": "0.5" 
},
{
 "len":           11.2,
"supp": "VC",
"dose": "0.5" 
},
{
 "len":           11.2,
"supp": "VC",
"dose": "0.5" 
},
{
 "len":            5.2,
"supp": "VC",
"dose": "0.5" 
},
{
 "len":              7,
"supp": "VC",
"dose": "0.5" 
},
{
 "len":           16.5,
"supp": "VC",
"dose": "1" 
},
{
 "len":           16.5,
"supp": "VC",
"dose": "1" 
},
{
 "len":           15.2,
"supp": "VC",
"dose": "1" 
},
{
 "len":           17.3,
"supp": "VC",
"dose": "1" 
},
{
 "len":           22.5,
"supp": "VC",
"dose": "1" 
},
{
 "len":           17.3,
"supp": "VC",
"dose": "1" 
},
{
 "len":           13.6,
"supp": "VC",
"dose": "1" 
},
{
 "len":           14.5,
"supp": "VC",
"dose": "1" 
},
{
 "len":           18.8,
"supp": "VC",
"dose": "1" 
},
{
 "len":           15.5,
"supp": "VC",
"dose": "1" 
},
{
 "len":           23.6,
"supp": "VC",
"dose": "2" 
},
{
 "len":           18.5,
"supp": "VC",
"dose": "2" 
},
{
 "len":           33.9,
"supp": "VC",
"dose": "2" 
},
{
 "len":           25.5,
"supp": "VC",
"dose": "2" 
},
{
 "len":           26.4,
"supp": "VC",
"dose": "2" 
},
{
 "len":           32.5,
"supp": "VC",
"dose": "2" 
},
{
 "len":           26.7,
"supp": "VC",
"dose": "2" 
},
{
 "len":           21.5,
"supp": "VC",
"dose": "2" 
},
{
 "len":           23.3,
"supp": "VC",
"dose": "2" 
},
{
 "len":           29.5,
"supp": "VC",
"dose": "2" 
},
{
 "len":           15.2,
"supp": "OJ",
"dose": "0.5" 
},
{
 "len":           21.5,
"supp": "OJ",
"dose": "0.5" 
},
{
 "len":           17.6,
"supp": "OJ",
"dose": "0.5" 
},
{
 "len":            9.7,
"supp": "OJ",
"dose": "0.5" 
},
{
 "len":           14.5,
"supp": "OJ",
"dose": "0.5" 
},
{
 "len":             10,
"supp": "OJ",
"dose": "0.5" 
},
{
 "len":            8.2,
"supp": "OJ",
"dose": "0.5" 
},
{
 "len":            9.4,
"supp": "OJ",
"dose": "0.5" 
},
{
 "len":           16.5,
"supp": "OJ",
"dose": "0.5" 
},
{
 "len":            9.7,
"supp": "OJ",
"dose": "0.5" 
},
{
 "len":           19.7,
"supp": "OJ",
"dose": "1" 
},
{
 "len":           23.3,
"supp": "OJ",
"dose": "1" 
},
{
 "len":           23.6,
"supp": "OJ",
"dose": "1" 
},
{
 "len":           26.4,
"supp": "OJ",
"dose": "1" 
},
{
 "len":             20,
"supp": "OJ",
"dose": "1" 
},
{
 "len":           25.2,
"supp": "OJ",
"dose": "1" 
},
{
 "len":           25.8,
"supp": "OJ",
"dose": "1" 
},
{
 "len":           21.2,
"supp": "OJ",
"dose": "1" 
},
{
 "len":           14.5,
"supp": "OJ",
"dose": "1" 
},
{
 "len":           27.3,
"supp": "OJ",
"dose": "1" 
},
{
 "len":           25.5,
"supp": "OJ",
"dose": "2" 
},
{
 "len":           26.4,
"supp": "OJ",
"dose": "2" 
},
{
 "len":           22.4,
"supp": "OJ",
"dose": "2" 
},
{
 "len":           24.5,
"supp": "OJ",
"dose": "2" 
},
{
 "len":           24.8,
"supp": "OJ",
"dose": "2" 
},
{
 "len":           30.9,
"supp": "OJ",
"dose": "2" 
},
{
 "len":           26.4,
"supp": "OJ",
"dose": "2" 
},
{
 "len":           27.3,
"supp": "OJ",
"dose": "2" 
},
{
 "len":           29.4,
"supp": "OJ",
"dose": "2" 
},
{
 "len":             23,
"supp": "OJ",
"dose": "2" 
} 
]
  
      if(!(opts.type==="pieChart" || opts.type==="sparklinePlus" || opts.type==="bulletChart")) {
        var data = d3.nest()
          .key(function(d){
            //return opts.group === undefined ? 'main' : d[opts.group]
            //instead of main would think a better default is opts.x
            return opts.group === undefined ? opts.y : d[opts.group];
          })
          .entries(data);
      }
      
      if (opts.disabled != undefined){
        data.map(function(d, i){
          d.disabled = opts.disabled[i]
        })
      }
      
      nv.addGraph(function() {
        var chart = nv.models[opts.type]()
          .width(opts.width)
          .height(opts.height)
          
        if (opts.type != "bulletChart"){
          chart
            .x(function(d) { return d[opts.x] })
            .y(function(d) { return d[opts.y] })
        }
          
         
        chart
  .margin({
 "left":    100 
})
  .reduceXTicks(false)
  .color([ "orange", "lightblue" ])
          
        chart.xAxis
  .staggerLabels(true)
  .axisLabel("Dose")

        
        
        chart.yAxis
  .axisLabel("Tooth Length")
      
       d3.select("#" + opts.id)
        .append('svg')
        .datum(data)
        .transition().duration(500)
        .call(chart);

       nv.utils.windowResize(chart.update);
       return chart;
      });
    };
</script>

The graph shows some kind of trend. It looks like as the dose is increased , the tooth length is bigger. When the dose is 0.5 miligrams or 1 miligrams, the length of the tooth with OJ supplement  looks  bigger. However if the supplement is 2.0 miligrams, the contrary occurs.

--- 

### Summary Data: describeBy

<!-- html table generated in R 3.1.2 by xtable 1.7-4 package -->
<!-- Wed Dec 31 13:13:16 2014 -->
<table border=1>
<tr> <th>  </th> <th> item </th> <th> group1 </th> <th> group2 </th> <th> vars </th> <th> n </th> <th> mean </th> <th> sd </th> <th> median </th>  </tr>
  <tr> <td align="right"> 11 </td> <td> 1 </td> <td> 0.5 </td> <td> OJ </td> <td align="right"> 1.00 </td> <td align="right"> 10.00 </td> <td align="right"> 13.23 </td> <td align="right"> 4.46 </td> <td align="right"> 12.25 </td> </tr>
  <tr> <td align="right"> 12 </td> <td> 2 </td> <td> 1 </td> <td> OJ </td> <td align="right"> 1.00 </td> <td align="right"> 10.00 </td> <td align="right"> 22.70 </td> <td align="right"> 3.91 </td> <td align="right"> 23.45 </td> </tr>
  <tr> <td align="right"> 13 </td> <td> 3 </td> <td> 2 </td> <td> OJ </td> <td align="right"> 1.00 </td> <td align="right"> 10.00 </td> <td align="right"> 26.06 </td> <td align="right"> 2.66 </td> <td align="right"> 25.95 </td> </tr>
  <tr> <td align="right"> 14 </td> <td> 4 </td> <td> 0.5 </td> <td> VC </td> <td align="right"> 1.00 </td> <td align="right"> 10.00 </td> <td align="right"> 7.98 </td> <td align="right"> 2.75 </td> <td align="right"> 7.15 </td> </tr>
  <tr> <td align="right"> 15 </td> <td> 5 </td> <td> 1 </td> <td> VC </td> <td align="right"> 1.00 </td> <td align="right"> 10.00 </td> <td align="right"> 16.77 </td> <td align="right"> 2.52 </td> <td align="right"> 16.50 </td> </tr>
  <tr> <td align="right"> 16 </td> <td> 6 </td> <td> 2 </td> <td> VC </td> <td align="right"> 1.00 </td> <td align="right"> 10.00 </td> <td align="right"> 26.14 </td> <td align="right"> 4.80 </td> <td align="right"> 25.95 </td> </tr>
   </table>

The table above shows that the length of the tooth in the case of 0.5 mg. and 1 mg. doses is bigger if the way that the supplement is taken is orange juice. However if the dose is 2 mg, the difference between acid ascorbic and orange juice is not as bigger as before. 

---

### Summary Data: summary

This table shows general statistics

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


## Conclusions

The next step (not in this presentation) is to apply different techniques to verify if these differences in length are real!! (hypothesis testing, confidence intervals, .. ).  In addition we need to verify that the data meet the requirements to apply these techniques. 

