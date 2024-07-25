---
title: "Motivation"
teaching: 20
exercises: 0
---

:::::::::::::::::::::::::::::::::::::: questions 

- Why version control?
- Why Git?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Understand the benefits of an automated version control system.
- Understand the basics of how automated version control systems work.

::::::::::::::::::::::::::::::::::::::::::::::::

## Why do we need version control?

We’ll start by exploring how version control can be used to keep track of what one person did and when. 
Even if you aren’t collaborating with other people, automated version control is much better than this situation:

[![Piled Higher and Deeper by Jorge Cham, http://www.phdcomics.com/comics/archive_print.php?comicid=1531](fig/intro/phd101212s.png)](http://www.phdcomics.com)
  
  
We've all been in this situation before: it seems unnecessary to have
multiple nearly-identical versions of the same document. Some word
processors let us deal with this a little better, such as Microsoft
Word's
[Track Changes](https://support.office.com/en-us/article/Track-changes-in-Word-197ba630-0f5f-4a8e-9a77-3712475e806a),
Google Docs' [version history](https://support.google.com/docs/answer/190843?hl=en), or
LibreOffice's [Recording and Displaying Changes](https://help.libreoffice.org/Common/Recording_and_Displaying_Changes).

Version control systems start with a base version of the document and
then record changes you make each step of the way. You can
think of it as a recording of your progress: you can rewind to start at the base
document and play back each change you made, eventually arriving at your
more recent version.

![](fig/intro/play-changes.svg){alt='Changes Are Saved Sequentially' width="700"}

Once you think of changes as separate from the document itself, you
can then think about "playing back" different sets of changes on the base document, ultimately
resulting in different versions of that document. For example, two users can make independent
sets of changes on the same document.

![](fig/intro/versions.svg){alt='Different Versions Can be Saved' width="700"}

Unless multiple users make changes to the same section of the document - a conflict - you can
incorporate two sets of changes into the same base document.

![](fig/intro/merge.svg){alt='Multiple Versions Can be Merged' width="700"}

A version control system is a tool that keeps track of these changes for us,
effectively creating different versions of our files. It allows us to decide
which changes will be made to the next version (each record of these changes is
called a [commit](../learners/reference.md#commit)), and keeps useful metadata
about them. The complete history of commits for a particular project and their
metadata make up a [repository](../learners/reference.md#repository).
Repositories can be kept in sync across different computers, facilitating
collaboration among different people.

::::::::::::::::::::::::::::::::::::::::::::::::::

## Have you ever said or heard...

- *"I will just finish my work and then you can start with your changes."*.
- *"Can you please send me the latest version?"*.
- *"Where is the latest version?"*.
- *"Which version are you using?"*.
- *"Which version have the authors used in the paper I am trying to reproduce?"*.

**Then version control is for you**
 
:::::::::::::::::::::::::::::::::::::::::  callout

::::::::::::::::::::::::::::::::::::::::::::::::::

## Discussion : Paper Writing
 
- Imagine you drafted an excellent paragraph for a paper you are writing, but later ruin
it. How would you retrieve the *excellent* version of your conclusion? Is it even possible?
  
- Imagine you have 5 co-authors. How would you manage the changes and comments
they make to your paper?  If you use LibreOffice Writer or Microsoft Word, what happens if
you accept changes made using the `Track Changes` option? Do you have a
history of those changes?
 
:::::::::::::::::::::::::::::::::::::::::  discussion

  
## What is version control?

There are lots of different tools that implement version control (generally referred to as **V**ersion **C**ontrol **S**ystems, **VCS**). They all have common features, including:

- A system which **records snapshots** of a project
- Implementation of **branching**:
  - you can work on several feature branches and switch between them
  - different people can work on the same code/project in parallel without interfering
  - you can experiment with an idea and discard it if it turns out to be a bad idea
- Implementation of **merging**:
  - tool to merge different versions of a file 
  
  
## Code becomes a disaster without version control


### Roll-back functionality

- Mistakes happen - without recorded snapshots you cannot easily undo mistakes and go back to a working version.


### Branching

- Often you want to experiment with an idea, or work on different approaches in one file - without branching this can be messy and confusing.
- You could simulate branching by copying an entire project to multiple places but this would be messy and confusing.


### Reproducibility

- How do you indicate which version of your code you have used in your paper?
- When you find a bug, how do you know when precisely this bug was introduced
  (are published results affected? do you need to inform collaborators or users of your code?).


### Storing and sharing code

- Online repositories, for safely storing snapshots and version history, are a cornerstone of version control
- Can act as a file backup, a collaboration tool, a download source, a citable reference, etc..
  
  
## We will use [Git](https://git-scm.com) as our VCS to record snapshots of our work - why Git?

- Easy to set up - use even by yourself with no server needed.
- Very popular: if contributing to somebody else's code, chances are it's tracked with Git.
- Distributed: good backup, no single point of failure, you can track and clean-up changes offline, simplifies collaboration model for open-source projects.
- Important platforms such as [GitHub](https://github.com), [GitLab](https://gitlab.com), and [Bitbucket](https://bitbucket.org)
  build on top of Git.
- Sharing software and data is getting popular and required in research context
  and sites like [GitHub](https://github.com) are a popular platform for sharing software.
  
::::::::::::::::::::::::::::::::::::: keypoints 

- Version control is like an unlimited 'undo'.
- Version control also allows many people to work in parallel.

::::::::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
