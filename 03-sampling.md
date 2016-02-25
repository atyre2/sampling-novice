---
layout: page
title: Sampling
subtitle: Generate a random sample
minutes: 10
---



> ## Learning Objectives {.objectives}
>
> * Explore the use of the R function `sample()`


Once you have decided to use simple random sampling to choose your sites, how do you do it? There are two steps.

* Create or obtain a vector of all possible sampling units
* Use `sample()` to select the units you will use. 

In the following we load the list of 3rd order HUCs found in Nebraska, and draw a random sample of 50 of them with replacement.


~~~{.r}
# code to be exectued
sampleFrame <- as.character(1:1000)
sampleIndex <- sample(sampleFrame, size = 50, replace = TRUE)
sampleIndex
~~~



~~~{.output}
 [1] "140" "335" "265" "881" "489" "126" "758" "619" "610" "570" "22" 
[12] "497" "132" "252" "243" "729" "198" "716" "290" "874" "508" "576"
[23] "234" "629" "412" "325" "479" "967" "477" "600" "948" "190" "98" 
[34] "315" "26"  "981" "431" "704" "868" "385" "757" "951" "880" "867"
[45] "296" "85"  "735" "210" "201" "542"

~~~

The first argument to `sample()` is the sampleFrame, the vector with the ID of each sample unit. The second argument size indicates the number of units to sample. The first argument describes whether the sample is drawn with replacement or not.
