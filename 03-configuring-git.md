---
title: "Configuring Git"
teaching: 15
exercises: 15
---

:::::::::::::::::::::::::::::::::::::: questions 

- How do we configure git?
- What are our options for text editors?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Learn how to configure the most useful git options.

::::::::::::::::::::::::::::::::::::::::::::::::

## Configuring Git

**All the configuration we enter here will be stored in a file `~/.gitconfig`.**

When we use Git on a new computer for the first time,
we need to configure a few things. Below are a few examples
of configurations we will set as we get started with Git:

*   our name and email address,
*   what our preferred text editor is,
*   and that we want to use these settings globally (i.e. for every project).

Let's work through it together in Git Bash.

First, the following commands will set your user name and email address:

```bash
$ git config --global user.name "Your Name"
$ git config --global user.email yourname@example.com
```

The name and contact email will be recorded together with the code changes when we run `git commit`.

::::::::::::::::::::::::::::::::::::: callout

## Private email

If you're using GitHub, and if you'd like to keep your personal email address private, 
you can use a GitHub-provided no-reply email address as your commit email address. 
[See here for further details](https://help.github.com/articles/about-commit-email-addresses/).

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: callout

## Line Endings

As with other keys, when you hit <kbd>Return</kbd> on your keyboard,
your computer encodes this input as a character.
Different operating systems use different character(s) to represent the end of a line.
(You may also hear these referred to as newlines or line breaks.)
Because Git uses these characters to compare files,
it may cause unexpected issues when editing a file on different machines. 
Though it is beyond the scope of this lesson, you can read more about this issue 
[on this GitHub page](https://help.github.com/articles/dealing-with-line-endings/).

::::::::::::::::::::::::::::::::::::::::::::::::

> You can change the way Git recognizes and encodes line endings
> using the `core.autocrlf` command to `git config`.
> The following settings are recommended:
>
> On macOS and Linux:
>
> ~~~bash
> $ git config --global core.autocrlf input
> ~~~
>
> And on Windows:
>
> ~~~bash
> $ git config --global core.autocrlf true
> ~~~


## Setting a default text editor

When you work with Git, you often need to make small text files to describe a 'snapshot'. When this is necessary, Git will open whatever default text editor you have set. 
This means it's often useful to choose which text editor you prefer, and set it as the default. On your local machine, you can set it to be whatever you like, but if you're working on a remote system, you will only have access to editors that are available there.

Below is a list of commands to set the default editor to a list of common tools. If you don't have any of these available, you might want to install Sublime Text, which is a great option that you can download from [https://www.sublimetext.com/3](https://www.sublimetext.com/3), or
[VS Code](https://code.visualstudio.com/), which is also great and in addition is free.


| Editor             | Configuration command                            |
|:-------------------|:-------------------------------------------------|
| Atom | `$ git config --global core.editor "atom --wait"`|
| BBEdit (Mac, with command line tools) | `$ git config --global core.editor "bbedit -w"`    |
| Emacs              | `$ git config --global core.editor "emacs"`   |
| Gedit (Linux)      | `$ git config --global core.editor "gedit --wait --new-window"`   |
| Kate (Linux)       | `$ git config --global core.editor "kate"`       |
| nano               | `$ git config --global core.editor "nano -w"`    |
| Notepad++ (Win, 32-bit install)    | `$ git config --global core.editor "'c:/program files (x86)/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`|
| Notepad++ (Win, 64-bit install)    | `$ git config --global core.editor "'c:/program files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`|
| Scratch (Linux)       | `$ git config --global core.editor "scratch-text-editor"`  |
| Sublime Text (Mac) | `$ git config --global core.editor "/Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl -n -w"` |
| Sublime Text (Win, 32-bit install) | `$ git config --global core.editor "'c:/program files (x86)/sublime text 3/sublime_text.exe' -w"` |
| Sublime Text (Win, 64-bit install) | `$ git config --global core.editor "'c:/program files/sublime text 3/sublime_text.exe' -w"` |
| Vim                | `$ git config --global core.editor "vim"`   |
| VS Code | `$ git config --global core.editor "code --wait"` |
  
  
    
::::::::::::::::::::::::::::::::::::: callout

## Git Help and Manual

Always remember that if you forget a `git` command, you can access the list of commands by using `-h` and access the Git manual by using `--help` :

~~~bash
$ git config -h
$ git config --help
~~~

::::::::::::::::::::::::::::::::::::::::::::::::


## Optional: Git GUI

You might find it easier to know what is going on if you install a Graphical User Interface.

There are many options here. 
Depending on your installation of git you might have a built-in basic GUI called `gitk` or `[QGit](https://github.com/tibirna/qgit#readme)`.
This is free.
Alternatively you might try a commercial git GUI. Here are some popular ones:

* [Sourcetree](https://www.sourcetreeapp.com/) (macOS, Windows)  
* [Sublime merge](https://www.sublimemerge.com/) (macOS, Windows, Linux) 
* [Gitkraken](https://www.gitkraken.com/) (macOS, Windows, Linux) 
* [Fork](https://git-fork.com/) (macOS, Windows)

Sourcetree is available for CSIRO staff within the Software Center.  

None of these are needed for this introductory tutorial, but they can be helpful to build understanding.

::::::::::::::::::::::::::::::::::::: keypoints 

- git configuration is all stored in `~/.gitconfig`
- The config is specific to each computer you use.

::::::::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
