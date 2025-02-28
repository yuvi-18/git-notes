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
cd .. :- to change to previous directory
clear:- to clear the view
touch example.txt :- make a new file inside a folder

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

for a short method of finding the changes: - 

``` 
git status -s

here green reoresent staging area, red stands for modified in working tree.
```

## initialise 

initialise a empty git repo in that folder.

```
git init
```

## clone a repo
clone the repo and all its code to your local device.

```
git clone https://github.com/username/repository.git
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

git offers:- Atomic commits
Atomic commits are a way to make sure that each commit is a self-contained unit of work. This means that if one commit fails, you can always go back to a previous commit and fix the issue. This is important for maintaining a clean and organized history in your repository.

example:- 

An unit of work for someone could be like making a footer.

commit messages are generally present tense and imperative like instead of added footer one should write add footer.


## commit add together 

```
git commit -am "Your commit message"
```

## Return to last commit 

This will only revert back the modified tracked files that aren't staged yet.
It will not touch staging area (the index) or reset anything in your commit history.

to return the data from your file to the previous commit:

``` 
git checkout <name of folder>
```


to restore the previous data for all the files according to the last commit

```
git checkout -f
```

## Return Everything to the last commit 

It will discard both staged and unstaged changes in your working directory and index, resetting everything to the state of the last commit (HEAD).
This is a destructive operation—your changes (both staged and unstaged) will be lost.

```
git reset --hard HEAD
```


## Remove the last added commit 

```
git rm --cached <fileName>
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

! these small options like "--oneline" are called flags in git.

! if lag occurs press q to exit.

to check certain numbers of commit logs

```
git log -p -1
```


## git diff

To check the difference between the staging area and the code 

```
git diff
```

To check the difference between the staging area and the last commit 

```
git diff --staged 
```


## Change existing code editor 

```
git config --global core.editor "code --wait"
```

Useful in a case like when u commit without giving any message git will open a folder in your code editor and then you can write the messaage there, after writing the message save and then close the folder, the commits would be saved now.

## git ignore

Gitignore is a file that tells git which files and folders to ignore. It is a way to prevent git from tracking certain files or folders. 

to use this :-

make a .gitignore folder and list all the files to be ignored there :-
```
.env
anyfile
```

make the gitignore file form the terminal to aboid any errors 

```
touch .gitignore
```

to ignore only the folder which is in the same directory as the git ignore file and not in any folder use /. otherwise gitignore will ignore all the files with the name given no mater where it is :-

```
/mylogs.log
```


to ignore all the files with the specific type use *

```
*.log
*.cpp
```

to ignore a folder write inside the gitignore file :- 

```
anyfolder/
```

## git keep

sometimes we want some empty folders to be there in the repo but git deosn't track the empty folders, ex:- 
if you add a empty folder like images and then use git status it won't show you the images folder as it is empty as of now, so to keep those folders we keep a .gitkeep file in the folder.

```
/images    // folder
  .gitkeep // file
```


# git behind the schenes
(only for info purpous this is not used or asked anywhere)


## Commit behidn the schenes

when an commit is made, a sha id(hash) is generated which keeps the info of the commit and the info of the parent commit, commits are dependent on the parent commit.

```
hash 
parent:-
info
```

every commit id is unique.

## git as a snapshot
A git snapshot is a point in time in the history of your code. It represents a specific version of your code, including all the files and folders that were present at that time. Each snapshot is identified by a unique hash code, which is a string of characters that represents the contents of the snapshot.
here snapshot is a loose term and not exactly means tkaing and storing a snapshot of the code.

## commit object

Each commit in the project is stored in .git folder in the form of a commit object. A commit object contains the following information:

Tree Object
Parent Commit Object
Author
Committer
Commit Message

## tree object

Tree Object is a container for all the files and folders in the project. It contains the following information:

File Mode
File Name
File Hash
Parent Tree Object

Everything is stored as key-value pairs in the tree object. The key is the file name and the value is the file hash.

## blob object

Blob Object is present in the tree object and contains the actual file content. This is the place where the file content is stored.

ex:-
```js
function clicked(){
    console.log("I was clicked")
}
```


# Branches in git 

Can be termed as alternate timeline.
Branches are a way to work on different versions of a project at the same time. They allow you to create a separate line of development that can be worked on independently of the main branch. This can be useful when you want to make changes to a project without affecting the main branch.

we make a seperate branch other than the main branch so that whatever we do does not affect the main branch even if it means deleting the entire code.

### to check the branch
```
git branch
```

### to create a new branch

```
git branch branch-name
```

now if we use git branch we will still be in the master branch because we have only created a new branch but we have not switched from the current branch.

### to switch

```
git switch branch-name

or 

git checkout branch-name

```

now if we see the branch then our branch would have been switched form master to the new branch that we created.

after we swtich back to the master branch the changes and added files that we made in our new branch will be not visible as it was not done in this timeline, branches can be understood as diffrent timelines.


! This all switching creating process can be directly viewed in the head folder of the .git folder.

git graph extnesion can be used for a easy and visual representation of branches.



### To switch and create a new branch at same time

```
git switch -c branch-name
```

## head in git

The HEAD is a pointer to the current branch that you are working on. It points to the latest commit in the current branch. When you create a new branch, it is automatically set as the HEAD of that branch.

before swtiching to our new branch the head was pointing to the master branch but now it would have been pointing on the new branch.

## merging branches in git

### Fast-forward merge

Get to the branch on which you want to merge the new branch to, ex:- 
on master branch I want to merge bug-fix branch
```
git merge bug-fix
```

to merge master branch into another branch run 

```
git merge master
```

### Not-fast forward merge

In this type of merge, the master branch also worked and have some commits that are not in the bug-fix branch. This is a not fast-forward merge.

in this type of merge you also have to give a message along with merging both the branches.

```
git merge bug-fix
```

~The message given here is mentioned as an extra commit in the repo.

If the command are same, what is the difference between fast-forward and not fast-forward merge?

The difference is resolving the conflicts. In a fast-forward merge, there are no conflicts. But in a not fast-forward merge, there are conflicts, and there are no shortcuts to resolve them. You have to manually resolve the conflicts. Decide, what to keep and what to discard.


## managing conflicts

There is no magic button to resolve conflicts. You have to manually resolve the conflicts. Decide, what to keep and what to discard.

in vs it is easy to solve conficts as it highlights the changes from the branch you are merging content from and gives you options like accept changes, decline etc.

```
<<<<<<< HEAD
added marketing section in the master branch
footer note :-
2025 is coming
======
footer note 
gta 6 is coming
>>>>>>> bug-fix
```

if i click on accept current change which was the change i made in the branch that i am currently on then to proceed further first i will abort the merge req.

```
git merge --abort

On branch master
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   file2.txt

```

so when manual fixing the file we jsut have to delete the portion of the code that we don't want and then all the arrows, then we'll just git add the modified file and commit it.

just like this we have manually merged conflicts.


## rename a branch

```
git branch -m master main
```

## delete a branch

```
git branch -d <branch-name>
```

## pull the latest branch

to pull the latest branch into the master branch 

```
git pull origin
```

# diff, stash amd tags

## git diff

The git diff is an informative command that shows the differences between two commits. It is used to compare the changes made in one commit with the changes made in another commit.
Git consider the changed versions of same file as two different files. Then it gives names to these two files and shows the differences between them.

### How to read the diff
a -> file A and b -> file B
---- indicates the file A
+++ indicates the file B
@@ indicates the line number
Here the file A and file B are the same file but different versions.

--- and +++ doesn't indicate subtraction or addition, it just denotes file a and file b.


```
git diff
```
This command alone will not show you the changes made in the file A and file B, you need to provide options to show the changes.

### Comparing Staging Area with Repository
git diff --staged

This command shows the changes between your last commit and the staging area (i.e., changes that are staged and ready to be committed).

### Comparing between branches
```
git diff <branch-name-one> <branch-name-two>
```

This command compares the difference between two branches.
Another way to compare the difference between two branches is to use the following command:

```
git diff branch-name-one..branch-name-two
```

### Comparing Specific Commits:
```
git diff <commit-hash-one> <commit-hash-two>
```

This command compares the difference between two commits.

## git stash

Stash is a way to save your changes in a temporary location. It is useful when you want to make changes to a file but don’t want to commit them yet. You can then come back to the file later and apply the changes.

Conflicting changes will not allow you to switch branches without committing the changes. Another alternative is to use the git stash command to save your changes in a temporary location.

```
git stash
```

This command saves your changes in a temporary location. It is like a stack of changes that you can access later.

### Naming the stash
You can also name the stash by using the following command:

```
git stash save "work in progress on X feature"
```

### View the stash list
You can view the list of stashes by using the following command:

```
git stash list
```

### Apply the stash
You can apply the stash by using the following command:

```
git stash apply
```

When you run git stash apply without specifying a particular stash, only the most recent stash (the first one) is applied. It does not apply all stashes.


### Apply the specific stash
You can apply the specific stash by using the following command:

```
git stash apply stash@{0}
```

Here stash@{0} is the name of the stash. You can use the git stash list command to get the name of the stash.

the recent stash is always on top of the previous stashes.

```
stash@{0}: WIP on main: 1234567 Commit message
stash@{1}: WIP on main: 89abcdef Commit message
```
Here, stash@{0} is the most recent stash, and stash@{1} is the one created earlier.


### Applying and dropping the stash
You can apply and drop the stash by using the following command:

```
git stash pop
```

The git stash pop command is used to apply the most recent stash from the stash list and remove it from the list of stashes.


### Drop the stash
You can drop the stash by using the following command:

```
git stash drop
```

drops the most recent stash form the stash list.

### Applying stash to a specific branch
You can apply the stash to a specific branch by using the following command:

```
git stash apply stash@{0} <branch-name>
```

### Clearing the stash
You can clear the stash by using the following command:

```
git stash clear
```

The git stash clear command is used to remove all stashes from the stash list at once.


!In all the commands if you don't specify the stash then it would be applied on the most recent stash.


## Git Tags
!generally not used by developers
Tags are a way to mark a specific point in your repository. They are useful when you want to remember a specific version of your code or when you want to refer to a specific commit. Tags are like sticky notes that you can attach to your commits.

### Creating a tag
You can create a tag using the following command:

```
git tag <tag-name>
```

This command creates a new tag with the specified name. The tag will be attached to the current commit.

### Create an annotated tag
You can create an annotated tag using the following command:

```
git tag -a <tag-name> -m "Release 1.0"
```

This command creates an annotated tag with the specified name and message. The tag will be attached to the current commit.

### List all tags
You can list all tags using the following command:

```
git tag
```

This command lists all the tags in your repository.

### Tagging a specific commit
You can tag a specific commit using the following command:

```
git tag <tag-name> <commit-hash>
```

### Push tags to remote repository
You can push tags to a remote repository using the following command:

```
git push origin <tag-name>
```

### Delete a tag
You can delete a tag using the following command:

```
git tag -d <tag-name>
```

### Delete tag on remote repository
You can delete a tag on a remote repository using the following command:

```
git push origin :<tag-name>
```


# Git rebase and reflog

## Git rebase

Git rebase is a powerful Git feature used to change the base of a branch. It effectively allows you to move a branch to a new starting point, usually a different commit, by “replaying” the commits from the original base onto the new base. This can be useful for keeping a cleaner, linear project history.

faaltu je commits na show ho jese jab merge karte hain branch tab ek faaltu ka commit message aa jaata hai merge ka wese message na aaye isliye git rebase use kar sakte.

it is suggested that jo master ya main branch hai usko rebase na karo, kisi or branch ko rebase karo

Ensure you are on the branch you want to rebase:

```
git branch 

*purple mode 


git rebase master
```

koi additinal commit nhi aayega   


## Git reflog 

poori history

Git reflog is a command that shows you the history of your commits. It allows you to see the changes that you have made to your repository over time. This can be useful for debugging and understanding the history of your project.


specific commit kek liye 

```
git reflog <commit-hash>
```

### Git commit recover using reflogs

If you accidentally deleted a branch or made changes that are no longer visible in the commit history, you can often recover them using the reflog. First, find the reference to the commit where the branch or changes existed, and then reset your branch to that reference. 

iss commit id tak thik tha toh wo mention karo toh utne tak reset ho jayega.

```
git reflog <commit-hash>
git reset --hard <commit-hash>

```


# Github

Github is a web-based Git repository hosting service. It is a popular platform for developers to collaborate on projects and to share code. Github provides a user-friendly interface for managing and tracking changes to your code, as well as a platform for hosting and sharing your projects with others.

Some other alternative of Github are:

Gitlab
Bitbucket
Azure Repos
Gitea

But mainstream popular tool these days is Github.


### Check remote url setting
You can check the remote url setting by running the following command:

```
git remote -v
```

This will show you the remote url of your repository.


### ssh keys

to give the permission of your local device to modify the repository of your github account you need to generate the ssh keys and paste it into your local device. the guide to this is given on the official github webite just go to gihub > settings > generate ssh and gpg keys or ["[click here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)"]

### Add remote repository
You can add a remote repository by running the following command:

```
git remote add origin <remote-url>
```

Here <remote-url> is the url of the remote repository that you want to add and origin is the name of the remote repository. This origin is used to refer to the remote repository in the future.

```
git remote add origin https://github.com/hiteshchoudhary/chai-something.git
```

### Push code to remote repository

```
git push -u origin main
```

This will set up an upstream remote and push your code to the remote repository. by upstream now you can just write git push and it will already know orgin and main.

## Hard push

```
git push --force origin <branchName>
```

This command pushes changes to the remote main branch, but it forces the push, even if it would overwrite changes on the remote branch.

Effect:
The --force flag forces the push to the remote repository, even if it would result in overwriting commits on the remote main branch that are not present in your local branch.

This can be dangerous because it rewrites history on the remote branch, potentially causing loss of commits or work that others have pushed to the same branch.

## Get code from remote repository
There are two ways to get code from a remote repository:

fetch the code

pull the code


Fetch the code means that you are going to download the code from the remote repository to your local repository.
Pull the code means that you are going to download the code from the remote repository and merge it with your local repository.

git pull = git fetch + git merge 


### Fetch code
To fetch code from a remote repository, you can use the following command:

```
git fetch <remote-name>
```


Here <remote-name> is the name of the remote repository that you want to fetch from.


### Pull code
To pull code from a remote repository, you can use the following command:


git pull <remote-name> <branch-name>
```
git pull origin main
```

Here <remote-name> is the name of the remote repository that you want to pull from and <branch-name> is the name of the branch that you want to pull.

the best way to use this is by first switching to the master branch and updating it to the latest version of the origin and then switching back to your local branch on which you were working on and updating it.