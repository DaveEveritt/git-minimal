# GIT commands

  - [Setup](#first-time-setup)
  - [Work on another machine](#work-on-another-machine)
  - [Use a branch to test new code](#use-a-branch-to-test-new-code)
  - [Check history and rewind](#check-history-and-rewind)
  - [Change remote](#change-remote)
  - [Resources](#resources)

---

A deliberately minimal set of commands for using GIT as simply as possible. Note:

- GIT will ask for some details the first time you use it on a machine
- this presumes you've created a simple repo on GitHub
- don't create a readme.md file on GitHub, make it locally and push


## First-time setup

1. git init
1. git status
1. git add .
1. git commit -m “describe change”
1. git status
1. git remote add origin (URL of remote repo)
1. git remote -v
1. git push -u origin master

## Work on another machine

1. git clone (URL of remote repo)
1. (do some work)
1. git add .
1. git commit -m “describe change”
1. git push

## Use a branch to test new code

1. git checkout -b branchname
1. (do some work)
1. git add .
1. git commit -m “describe change”
1. git push -u origin branchname
1. git checkout master
1. git diff master branchname
1. (repeat 2-4 if necessary)
1. git merge branchname
1. (repeat 2-4 if necessary)
1. git branch -a (lists all branches)
1. git branch -d (use -D to force delete)

## Check history and rewind

1. git log --pretty=oneline
1. git fetch origin (override local changes)
1. git reset --hard origin/master
1. git checkout -- filename (restore previous version of file)
1. git reset —hard HEAD~ (revert to previous commit)

## Change remote

1. git clone (URL of remote repo)
1. git remote set-url origin (URL of new repo)
1. git remote -v


## Resources

- [Video tutorial for Git use in CTEC3905](https://dmureplay.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=5ae4fefe-c3b9-4171-a381-f227e3e47c29)  
- [git - the simple guide](https://rogerdudler.github.io/git-guide/)
