---
title: "Making git citable"
teaching: 20
exercises: 20
---

:::::::::::::::::::::::::::::::::::::: questions 

- How can we make a particular git commit citable?
- How can version control help reproduceable science?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Learn how to tag a particular git commit
- Consider for version control contributes to open science

::::::::::::::::::::::::::::::::::::::::::::::::

## Citing code

One of the major benefits of using code for data analysis is reproducibility and enabling 
transparency about the way data was manipulated and analysed. Using a version control system 
like git takes that to another level by enabling the sharing of the history of the code, as 
well allowing collaboration on code. 

But because by its very nature the code may change over time, it's necessary to be able to 
point to a particular point of history when we want to cite the code, such as in a research paper. 

::::::::::::::::::::::::::::::::::::::::  discussion

## Discussion  
The old way of sharing a particular version of code was to upload a text file as supplementary 
material.  
- What are some of the shortcomings of this approach?  
- With your new expertise with git, what would be a better way?  

::::::::::::::::::::::::::::::::::::::::::::::::::::

  
## Referring to particular commits

To enable us to accurately refer to a particular commit, we need a label for it. The hash strings 
that git generates could work, but they are unwieldy. Branch pointers don't work because they stay 
at the tip of each branch.

Instead, git provides tags.

Tags are pointers that refer to a specific commit, and then never move. 

You can give a tag any label you'd like (short, meaningful, no spaces). A classic example of a tag 
may be "v1.0" to denote
a finalised "version 1" release of something.  

::::::::::::::::::::::::::::::::::::: challenge 

## Challenge

- In the [vizualise git environment](http://git-school.github.io/visualizing-git/) have a go at 
  creating tags.
- Use `git tag [tagname]`
- Create a tag, then add some commits. What happens to the different pointers?
- Make some more tags, then practice doing `git checkout [tag]`

::::::::::::::::::::::::::::::::::::::::::::::::

## Making tags static with GitHub and Zenodo

While tags are really useful to point to a particular commit, they don't give a single access point - for 
example they exist in all copies of the repository, and there doesn't have to be a publicly accessible copy. 
For a citation, that's not much good. 
If working in GitHub, there is an option to publish a Digital Object Identifier (DOI), permanently linking to a 
particular tag, via Zenodo - 
[https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content](https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content)
  
---
  
## Open Science

Free sharing of information might be the ideal in science, but the reality is often more complicated.
Often practice today looks something like this:

- A scientist collects some data and stores it on a machine that is occasionally backed up by their department.  
- They then write or modify a few small programs (which also reside on the machine) to analyze that data.  
- Once they have some results, they write them up and submit a paper. The scientist might include their 
  data -- a growing number of journals require this -- but they probably don't include the code.  
- Time passes.  
- The journal sends the scientist reviews written anonymously by a handful of other people in their field.  
  The scientist revises the paper to satisfy the reviewers, during which time they might also modify the 
  scripts they wrote earlier, and resubmits.  
- More time passes.  
- The paper is eventually published. It might include a link to an online copy of the data,
  but the paper itself will be behind a paywall: only people who have personal or institutional access
  will be able to read it.  

For a growing number of scientists, though, the process looks like this:

- The data that the scientist collects is stored in an open access repository
  like CSIRO's [Data Access Portal](https://data.csiro.au/), possibly as soon as it's collected,
  and given its own  
  [Digital Object Identifier](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). 
- The scientist creates a new repository on BitBucket to hold their work.  
- During analysis, they push changes to their scripts (and possibly some output files) to that repository.
  The scientist also uses the repository for their paper; that repository is then the hub for collaboration 
  with colleagues.  
- When they are happy with the state of the paper, the scientist posts a version to [arXiv](https://arxiv.org/)
  or some other preprint server to invite feedback from peers.  
- Based on that feedback, they may post several revisions before finally submitting the paper to a journal.  
- The published paper includes links to the preprint and to the code and data repositories, which 
  makes it much easier for other scientists to use their work as starting point for their own research.  

This open model accelerates discovery:
the more open work is,
[the more widely it is cited and re-used](https://doi.org/10.1371/journal.pone.0000308).
However, people who want to work this way need to make some decisions about what exactly 
"open" means and how to do it. You can find more on the different aspects of 
Open Science in [this book](https://link.springer.com/book/10.1007/978-3-319-00026-8).

This is one of the (many) reasons we teach version control.
When used diligently, it answers the "how" question by acting as a shareable electronic lab notebook 
for computational work:

- The conceptual stages of your work are documented, including who did
  what and when. Every step is stamped with an identifier (the commit ID)
  that is for most intents and purposes unique.  
- You can tie documentation of rationale, ideas, and other
  intellectual work directly to the changes that spring from them.  
- You can refer to what you used in your research to obtain your
  computational results in a way that is unique and recoverable.  
- With a version control system such as Git,
  the entire history of the repository is easy to archive for perpetuity.  

With tools like [R Markdown](https://rmarkdown.rstudio.com/) and 
[Jupyter Notebooks](https://jupyter.org/), documentation may be mixed directly with code 
to generate graphs and images for the same documentation, and all stored in version control!  
   
---
  
## Licenses and citations

A final note to keep in mind if sharing a Git repository publicly- it may be important to 
include some licensing information (often done in a LICENSE.md file) instructing under what
conditions others are welcome to use/modify your work. 
[Example](https://github.com/csiro-data-school/git-intro-23/blob/gh-pages/LICENSE.md)
IM&T may help with this if necessary. 
  
Similarly, a citation file may be useful to include, with a request for how you'd like your work 
to be cited. A special format is proposed specifically for this purpose, in the form of 
a CITATION.cff file, containing a standardised set of information that is both human and
machine readable. E.g.:  
  
```
cff-version: 1.2.0
message: "If you use this software, please cite it as below."
authors:
  - family-names: Druskat
    given-names: Stephan
    orcid: https://orcid.org/1234-5678-9101-1121
title: "My Research Software"
version: 2.0.4
doi: 10.5281/zenodo.1234
date-released: 2021-08-11
```

More information is available here:  [citation-file-format.github.io](https://citation-file-format.github.io/)

::::::::::::::::::::::::::::::::::::: keypoints 

- Git tags may be generated to note a particular version in history.
- Consider use of git early in scientific workflows, for robust documentation.
- Open scientific work is more useful and more highly cited than closed.

::::::::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
