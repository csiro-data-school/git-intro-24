---
title: "In-browser session"
teaching: 20
exercises: 0
---

:::::::::::::::::::::::::::::::::::::: questions 

- Where are we heading?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- See an existing repository in action.
- Browse the history.
- See the big picture first before we dive into details.

::::::::::::::::::::::::::::::::::::::::::::::::

# In-browser session

- We will explore and visualize an **existing Git repository** on BitBucket.
- The goal of this episode is not to teach BitBucket, but rather to get a glimpse of the 
wider picture before going into the details.
  

## Why?

- Often our first contact with Git is an existing repository.
- It's good to see the social aspect to know what our end goal is.
- Don't worry about the details of the steps here, just investigate what we can learn about an existing repository.
  

## Bitbucket demo

We'll start with a very simple 
[existing repository](https://bitbucket.csiro.au/projects/DAT/repos/programmatic-data-example/)
that contains a brief history from a couple of different people.

![](fig/bitbucket/example-repo.png){alt='BitBucket example screen' width=75%}

- History
  - Explore the [repository](https://bitbucket.csiro.au/projects/DAT/repos/programmatic-data-example/).
  - Explore the history and [commits](https://bitbucket.csiro.au/projects/DAT/repos/programmatic-data-example/commits).
  - Note that there are [branches](https://bitbucket.csiro.au/plugins/servlet/network/DAT/programmatic-data-example).
- Reproducibility
  - Explore the ['blame' feature](https://bitbucket.csiro.au/projects/DAT/repos/programmatic-data-example/browse/scripts/visualise-data.R).
- Collaboration
  - You can refer to [code portions](https://bitbucket.csiro.au/projects/DAT/repos/programmatic-data-example/browse/scripts/visualise-data.R#5-7)
    (so much simpler to send a link rather than describe which file to open and where to scroll to).
  - Note the [contributors](https://bitbucket.csiro.au/projects/DAT/repos/programmatic-data-example/commits).
- As a file source
  - We can create a local copy of all files in a repository through a **clone**
  - `git clone https://bitbucket.csiro.au/scm/dat/programmatic-data-example.git`


These features are all based on the core underlying Git system, that works independently of Bitbucket and is shared
by other sites such as GitHub and GitLab.

## GitHub demo

[These lessons](https://github.com/csiro-data-school/git-intro-24) are themselves tracked through Git, but stored on 
GitHub (making use of the automatic webpage generation feature GitHub Pages).  
Note that GitHub looks very different to BitBucket, but all of the same information and features may be found, with 
a click around. 
  
This version of Git Intro lessons is a modified 
["fork"](https://github.com/csiro-data-school/git-intro-23/network/members) of an older version, which was itself a "fork"
of other older versions. 
A **fork** is a full copy of a repository into a new repository, which retains full history but allows it to branch 
in its own separate direction, under separate control. We'll discuss forks further later.  

The bulk of these lessons are thanks to the [Code Refinery](https://github.com/coderefinery/git-intro) and 
[Software Carpentry](https://github.com/swcarpentry/git-novice) Git lessons, also in their own Git repositories.  
  
::::::::::::::::::::::::::::::::::::: keypoints 

- There are multiple online repositories for storing projects that all use the underlying Git framework
- Bitbucket is one such service, using Git to provide functionality to collaborate with other people
- We can browse the history of the contents of repositories and see who made which changes
- Other platforms like Github look different by employ the same fundamentals

::::::::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
