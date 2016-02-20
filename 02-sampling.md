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
 [1] "591" "690" "110" "479" "168" "567" "564" "742" "346" "617" "12" 
[12] "741" "182" "311" "962" "260" "542" "3"   "599" "287" "711" "212"
[23] "903" "917" "845" "908" "227" "284" "529" "260" "520" "151" "628"
[34] "4"   "980" "69"  "779" "109" "398" "317" "655" "194" "876" "102"
[45] "97"  "524" "585" "266" "108" "563"

~~~

The first argument to `sample()` is the sampleFrame, the vector with the ID of each sample unit. The second argument size indicates the number of units to sample. The first argument describes whether the sample is drawn with replacement or not.
