# GIT commands

  - [Setup](#1.-setup)
  - [Work on another machine](#2.-work-on-another-machine)
  - [Use a branch to test new code](#3.-use-a-branch-to-test-new-code)
  - [Check history and rewind](#4.-check-history-and-rewind)
  - [Resources](#resources)

---

A deliberately minimal set of commands for using GIT as simply as possible. Note:

- GIT will ask for some details the first time you use it on a machine
- this presumes you've created a simple repo on GitHub
- don't create a readme.md file on GitHub, make it locally and push


## 1. Setup

1. `git init`
2. `git status`
3. `git add .`
4. `git commit -m "describe change"`
5. `git status`
6. `git remote add origin URL_of_remote_repo_here`
7. `git remote -v`
8. `git push -u origin master`

## 2. Work on another machine

1. `git clone URL_of_remote_repo_here`
2. (do some work)
3. (repeat 2, 5)
4. `git push`

## 3. Use a branch to test new code

1. `git checkout -b branchname_here`
2. `git checkout -b branchname_here`
3. (do some work)
4. (repeat 2-5)
5. `git push -u origin branchname_here`
6. `git checkout master`
7. `git diff master branchname_here`
8. (repeat 2-5 if necessary)
9. `git merge branchname_here`
10. (repeat 2-5 if necessary)
11. `git branch -a` (lists all branches)
12. `git branch -d` (use `-D` to force delete)

## 4. Check history and rewind

1. `git log --pretty=oneline`
2. `git fetch origin` (override local changes)
3. `git reset --hard origin/master`
4. `git checkout -- filename_here` (restore previous version of file)
5. `git reset —hard HEAD~` (revert to previous commit)

## Resources

[git - the simple guide (Roger Dudler)](https://rogerdudler.github.io/git-guide/)
