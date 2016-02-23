---
layout: page
title: Sampling
subtitle: Why Worry?
minutes: 10
---
> ## Learning Objectives {.objectives}
>
> * Explain what can happen when sampling is not random.
> * Describe the four steps of the data life cycle

## The data life cycle [*][footnote1]

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
These steps involve three things: attention to details, redundancy, and 
The attention to details is the careful layout of your subdirectories, use of naming conventions
for variables and filenames, and documenting everything with comments. Version control is 
giving you redundancy -- offsite backup combined with the ability to go back to previous 
versions when things stop working. 

The combination of these 3 items with each of the 4 stages of the data life cycle give you 
a powerful tool for thinking carefully about how to manage your data long before you ever 
get into the field to collect it. 

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
of the sun](http://phys.org/news/2016-02-eternal-5d-storage-history-humankind.html), but 
for now the standard answer is "put it in the cloud". Cloud storage refers to services like
(dropbox)[www.dropbox.com] or (Google Drive)[https://drive.google.com]. These systems use
massively redundant storage so that when a harddrive fails, it is just unplugged and replaced, 
and the system carries on storing data and serving it up with no losses. Your data could
be effectively stored in multiple geographic locations, all without your knowledge! The advantage
of these services is that files can be easily shared across the internet, and there is 
usually some kind of limited version control. Perhaps the biggest risk with these services is ensuring security
and controlling access to data -- making sure that modifications to the data are not made 
inadvertently or maliciously. Also the concern about long term viability of the service is
a real one. Big companies like Google or Amazon are unlikely to go away, but they may decide
to chance how the service is offered or even what services are offered. 



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

and one or more of these at the end:

> ## Challenge Title {.challenge}
>
> Description of a single challenge,
> separated from the title by a blank line.
> There may be several challenges;
> they should all come at the end of the file,
> and each should have a short, meaningful title.

[footnote1] This idea of the four stages and 3 steps in the data lifecycle is entirely due 
to Keith Hurley, Nebraska Game and Parks Commission. Any errors or falsehoods are due to 
my poor memory and misinterpretation. 