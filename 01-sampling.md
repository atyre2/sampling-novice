---
layout: page
title: Sampling
subtitle: The data life cycle?
minutes: 10
---
> ## Learning Objectives {.objectives}
>
> * Describe the four steps of the data life cycle

## The data life cycle [^1]

The fundamental workflow in science involves observing a quantity out in the world, recording it in some fashion,
thinking and writing about it, and then ensuring that others can use the same observation.
Rinse and Repeat. Thus, a modern scientific workflow has four steps:

* Collect the data
* Enter the data into a computer
* Analyse and present the data
* Archive the data

There are opportunities for errors to creep in at each of these four stages. Part of ensuring
our work is *credible*, that is, to be trusted by others, involves both documenting these 
four stages and working to minimize the errors. Ideally, the errors would be eliminated entirely. 
Unfortunately that is an unrealistic goal, but careful attention to each of these four
stages can reduce the errors. 

In the R lesson you have learned how to document and reduce errors in the analysis step. 
Primarily this involves using well organized project directories, data cleaning, exploration, 
analysis and presentation (figures and tables) steps documented with comments in scripts. 
Ideally, the development of those scripts was documented using version control.
These steps involve three things: attention to details, redundancy, and consistency.
The attention to details is the careful layout of your subdirectories and documenting everything with comments. Version control is 
giving you redundancy -- offsite backup combined with the ability to go back to previous 
versions when things stop working. Use of naming conventions
for variables and filenames gives you consistency which makes it easier for you to follow what you've done in the future.

The combination of these 3 items with each of the 4 stages of the data life cycle give you 
a powerful tool for thinking carefully about how to manage your data long before you ever 
get into the field to collect it. 

## Data Collection

The process of collecting data in the lab or field is the start of the entire 
process. Attention to details here means thinking carefully about what to put on your data sheets. Have you indicated the units to use and the precision? 
Consistency leads us to think about writing down a standard operating procedure
for data collection. If you couldn't be present, would a substitute be able to do exactly what you have done?
Have they used the same tools? Think about a fish measuring board.
What if a different board is used that has different units, or measures to a different precision, you 
could inadvertently affect your data. A scale with 
two sets of units (inches and mm), creates even more opportunities for errors. 
Redundancy in data collection involves two things. One, remember the adage "measure twice, cut once". 
Reading the weight of that nestling on your scale twice helps reduce "translation errors". 
Translation errors arise when you perceive something, or understand something, incorrectly. 
You write down what you heard from the angler, but you misunderstood what they were saying. 

The second thing is ensuring that you create a backup copy of your data at the earliest opportunity. Photocopying the datasheets is an old-school solution. How about taking a picture of a datasheet with a smart phone and storing the result in the cloud for an almost instant backup? 

## Data Entry

So now you've got your data back from the field or lab, and you want to get it into the computer so you can 
analyze it. Here are many more opportunities for human error to creep into your data set. 
The NGPC creel survey clerks record data from anglers across the state, and enter that data into 
a carefully constructed database that validates entries to ensure categorical variables 
are correct, date formats are consistent, etc. Nonetheless, the estimated error 
rate at data entry is around 5\%! Those are known as "transcription errors", because 
they occur as data is transcribed from one medium (data sheet or lab notebook) into another (digital file). 
There are two methods for reducing transcription errors: Validation and Verification. 

Validation methods involve using the computer to check data values as they are entered to 
make sure they are accurate. For example, a common error that arises when entering categorical data 
is misspellings, changes in capitilization, and even the inclusion of a trailing space! 
Invisible to a cursory inspection of your data, it renders that value different 
from others to a computer. These sorts of errors are even more common 
when different people enter data. 
Date and time fields are another source of headaches for computers. 
The use of software to do data validation on entry is the topic of another lesson. 

Verification is the process of ensuring that the data in a database match the data 
that were collected. Broadly there are two approaches. First, you can enter all 
the data twice. Yes, twice. Then check to see if the data match. Any record or 
field that doesn't match is an error. This is the gold-standard method. 

Second, you can look at the data and compare it to the datasheet to see if 
the entered values match what was written down. This is sometimes done as a random
spot check rather than an exhaustive comparison. However if you check 10\% 
of your observations and you have a 5\% error rate you will only catch 10\% of the errors. 
There are some software based strategies to employ at this stage to help
identify erroneous entries. For example, plot numeric data on a graph 
where you have a known relationship (e.g. weight vs. length). Points that are 
a long distance from the majority of points are probably errors and should be checked. 
Another strategy for numeric variables is to sort a data set by that variable 
and check the smallest and largest *n* rows. Range errors will show up 
in this type of check. 
For categorical variables, tabulate the number of observations in each category. This will quickly 
identify the typo based errors discussed above. 

These two steps are essential parts of a data management plan. 
They are sometimes referred to as Quality Assurance (Validation) and 
Quality Control (Verification). The difference is in making sure errors do not arise 
in the first place (QA), and finding errors after the fact (QC).  

## Data Archiving

This step is the one most often ignored and is rarely documented. The basic idea is to ensure
that those who follow after you, perhaps long after you, can access the data you have 
invested so much effort into. 

> ## Is it available? {.challenge}
>
> Go to your advisor or supervisor and ask for the data underlying any of their published 
> papers more than 5 years old. If they have it, can you read it into R without errors? 
> If you don't have an advisor, do this exercise with one of your OWN papers! 

Funding agencies, particularly federal agencies in the USA, are starting to require documentation of 
this step. Many journals now require the deposition of data in a usable form for published 
articles. From a redundancy perspective,  having the data for a paper archived by the publisher
is good. But what about the data that didn't make it into the paper? What happens if that 
publisher goes out of business?

Paying attention to details at this stage revolves around two things: the format the data 
are stored in, and the media that they are stored on. 

The first is harder than you might 
think. If you have used a Microsoft Access database to enter your data, the file format is
a proprietary (that is, owned by Microsoft) binary format. Programs from other software 
companies may or may not be able to read that format directly. Or perhaps you used SAS to 
analyze your data, and the data files are stored in SAS data files. There is no guarantee
that even a future version of that same software will be able to read those files! Often the 
file format that is convenient for the earlier stages of the data lifecycle may not be the 
best choice for the final stage. The most reliable format is some kind of plain text file, e.g. CSV
file. These are easily readable by many different types of software, can also be read by humans, and are unlikely to 
change significantly over time. There may be *export* options from your software that will 
provide text files that also have information about variable types and the relationships between the
files. 

The media used for storage are important and also difficult to think about long term. Not that
long ago data were stored on paper punch cards! Good luck finding a working punch card reader.
After that came magnetic floppy disks and audio tape. Now we have optical disks, CDs and DVDs, 
but even those have a limited lifespan. They degrade with time, and like the punch card and floppy 
disks, the machinery to read them may go out of style. Already many Macintosh computers do
not come standard with optical drives. 

In the future, we might be able to use [holographic storage that will outlast the lifetime 
of the sun][holographic], but 
for now the standard answer is "put it in the cloud". Cloud storage refers to services like
[dropbox][] or [Google Drive][]. These systems use
massively redundant storage so that when a harddrive fails, it is just unplugged and replaced, 
and the system carries on storing data and serving it up with no losses. Your data could
be effectively stored in multiple geographic locations, all without your knowledge! The advantage
of these services is that files can be easily shared across the internet, and there is 
usually some kind of limited version control. Perhaps the biggest risk with these services is ensuring security
and controlling access to data -- making sure that modifications to the data are not made 
inadvertently or maliciously. Also the concern about long term viability of the service is
a real one. Big companies like Google or Amazon are unlikely to go away, but they may decide
to chance how the service is offered or even what services are offered. 

Attention to details and consistency for data archiving are really extensions of the same things you've already been doing. 
By using a consistent organization of subdirectories, filename conventions and providing metadata for 
your data you ensure that future you, as well as others
will be able to access and use your hard won data. 


--- possibly including [definitions](reference.html#definitions) ---

~~~ {.r}
some code:
    to be displayed
~~~

and:

~~~ {.output}
output
from
program
~~~

and:

~~~ {.error}
error reports from programs (if any)
~~~

and possibly including some of these:

> ## Callout Box {.callout}
>
> An aside of some kind.



[^1]: This idea of the four stages and 3 steps in the data lifecycle is entirely due 
to Keith Hurley, Nebraska Game and Parks Commission. Any errors or falsehoods are due to 
my poor memory and misinterpretation.

[holographic]: http://phys.org/news/2016-02-eternal-5d-storage-history-humankind.html
[dropbox]: https://dropbox.com "Dropbox"
[Google Drive]: https://drive.google.com "Google Drive"