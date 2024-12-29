# git 

git is a version control system software which tracks changes in your code. it is free and open source software that is available on windows, macOS and linux.(works as checkpoints to for our code).
! git is a software that can be installed on our computer.

# github

github whereas is a web based hosting service for git repositories.it is used as an online platform to store and share code with others. it is popular service among developer to collaborate and share code.

# Version Control System(VCS)

A Version Control System (VCS) is a tool that helps track changes to files over time, enabling multiple users to collaborate on the same project without overwriting each other's work. It keeps a history of all changes made to files, allowing users to revert to previous versions, compare changes, and manage different versions of a project efficiently.

!Git is the most popular distributed Version Control System (DVCS) used today, and platforms like GitHub, GitLab, and Bitbucket provide cloud-based hosting services for Git repositories, making collaboration easier.

!In simple words, vcs tool is utilised by git software.
!Yes, exactly! Git is a software tool that implements a Version Control System (VCS), specifically a Distributed Version Control System (DVCS).distributed here refers everyone has the copy of the repo.

# Installation

[Download git from:- https://git-scm.com/downloads](https://git-scm.com/downloads)

Reccommended git settings are good enogh so don't change them and let it install;

# git Terminologies

Open git bash by right clicking in the folder that you want to work in.
set the name and email after first time opening the git bash so that if you make a change in something your name will be there:-


### to check
```
yuvraj singh@pomogranate MINGW64 ~/Documents/git
$ git config --global user.name
Yuvraj

yuvraj singh@pomogranate MINGW64 ~/Documents/git
$ git config --global user.email
fcyuvraj18@gmail.com
```

### to set
```
yuvraj singh@pomogranate MINGW64 ~/Documents/git
$ git config --global user.name "yuvraj"

yuvraj singh@pomogranate MINGW64 ~/Documents/git
$ git config --global user.email "fcyuvraj18@gmail.com"
```

Prefer using double quotes for values so that it doesn't interfere when using special symbols


### to check all the changes that you made 
```
git config --list
```

### To open Vs

```
code .
```


### to check where are you in the terminal 

pwd :- present working directory
ls:- list the files and directories in the current working directory
cd foldername/ :- to change current directory
clear:- to clear the view

### To check for the version 

```
git --version
```

## Repositories

repo is nothing but another name for a folder where all the code has been stored.

to know if the pwd is a repo or not
```
git status
```

## initialise 

initialise a empty git repo in that folder.

```
git init
```

## clone a repo
clone the repo and all its code to your local device.

```
git clone
```

## to see hidden folders 

```
ls -lart
```

## Commit
Commit is a way to save your changes to your repository. It is a way to record your changes and make them permanent. You can think of a commit as a snapshot of your code at a particular point in time. When you commit your changes, you are telling git to save them in a permanent way. This way, you can always go back to that point in time and see what you changed.

## git flow

git flow:-

git init:- initialise the new repo.  // Working Directory
git add:- stage the changes  // Staging area
git commit:- add/save the changes in the repo.  // Repo
git push:- push/add the changes to github or gitlab.  // github


## Stage 
Stage is a way to tell git to track a particular file or folder.

```
git init
git add file file2
git status
``` 

To stage all the files together
```
git add .



output:- 
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   file.txt
        new file:   file2.txt
```

Currently our files are in staging area, this means that we have not yet committed the changes but are ready to be committed.



## Commit

Here we are committing the changes to the repository. We can see that the changes are now committed to the repository.


```
git commit -m "commit message"
git status



$ git commit -m "first commit"
[master (root-commit) 24592ad] first commit
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 file.txt
 create mode 100644 file2.txt
```


## git log

This command will show you the history of your repository. It will show you all the commits that were made to the repository.

```
git log



commit 49b9c31dda6bd7d1dff98de36cf4498927bf202b (HEAD -> master)
Author: Yuvraj <fcyuvraj18@gmail.com>
Date:   Sun Dec 29 10:12:29 2024 +0530

    modified

commit 24592ad97c313c9f7948de64237bb6a354f7807f
Author: Yuvraj <fcyuvraj18@gmail.com>
Date:   Sun Dec 29 10:08:20 2024 +0530

    first commit
```



to only see the commit message 
```
git log --online


49b9c31 (HEAD -> master) modified
24592ad first commit
```


