# GIT commands

- [GIT commands](#git-commands)
  - [Setup a new repository](#setup-a-new-repository)
  - [Work on another machine](#work-on-another-machine)
  - [Use a branch to test new code](#use-a-branch-to-test-new-code)
  - [Check history and rewind](#check-history-and-rewind)
  - [Change remote](#change-remote)
  - [Resources](#resources)

---

A deliberately minimal set of commands for using GIT as simply as possible. Note:

1. GIT will *ask for some details* the first time you use it on a machine
2. these instructions will *need a repo on GitHub* for you to push to
3. *don't* create a readme.md file on GitHub, make it locally and push

## Setup a new repository

1. `git init`
2. `git status`
3. `git add .`
4. `git commit -m "describe change"`
5. `git status`
6. `git remote add origin URL_of_remote_repo_here`
7. `git remote -v`
8. `git push -u origin master`

## Work on another machine

1. `git clone URL_of_remote_repo_here`
2. (do some work)
3. `git add .`
4. `git commit -m "describe change"`
5. `git status`
6. `git push`

## Use a branch to test new code

1. `git checkout -b branchname_here`
2. (do some work)
3. `git add .`
4. `git commit -m “describe change”`
5. (repeat 2-4)
6. `git push -u origin branchname_here`
7. `git checkout master`
8. `git diff master branchname_here`
9. (repeat 2-4 if necessary)
10. `git merge branchname_here`
11. (repeat 2-4 if necessary)
12. `git branch -a` (lists all branches)
13. `git branch -d` (use `-D` to force delete)

## Check history and rewind

1. `git log --pretty=oneline`
2. `git fetch origin` (override local changes)
3. `git reset --hard origin/master`
4. `git checkout -- filename_here` (restore previous version of file)
5. `git reset —hard HEAD~` (revert to previous commit)

## Change remote

1. `git clone URL_of_remote_repo`
2. `git remote set-url origin URL_of_NEW_repo`
3. `git remote -v`

---

## Resources

- [git - the simple guide (Roger Dudler)](https://rogerdudler.github.io/git-guide/)
- Fania's [video walkthrough for Git use in the labs](https://dmureplay.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=5ae4fefe-c3b9-4171-a381-f227e3e47c29)  
