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
 [1] "434" "386" "360" "447" "279" "605" "586" "636" "824" "786" "630"
[12] "196" "301" "105" "690" "223" "251" "945" "843" "654" "859" "588"
[23] "458" "854" "270" "467" "504" "390" "452" "630" "318" "289" "352"
[34] "782" "797" "532" "676" "578" "498" "393" "448" "661" "792" "547"
[45] "962" "705" "498" "509" "788" "789"

~~~

The first argument to `sample()` is the sampleFrame, the vector with the ID of each sample unit. The second argument size indicates the number of units to sample. The first argument describes whether the sample is drawn with replacement or not.
