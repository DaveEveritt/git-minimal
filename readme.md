# GIT commands

A deliberately minimal set of commands for using GIT as simply as possible.

- GIT will ask for some details the first time you use it on a machine
- this presumes you've created a simple repo on GitHub
- don't create a readme.md file on GitHub, make it locally and push

## Setup

1. git init
2. git status
3. git add .
4. git commit -m “describe change”
5. git status
6. git remote add origin (URL of remote repo)
7. git remote -v
8. git push -u origin master

## Work on another machine

9. git clone (URL of remote repo)
10. (do some work)
11. (repeat 2, 5)
12. git push

## Use a branch to test new code

13. git checkout -b branchname
14. (do some work)
15. (repeat 2-5)
16. git push -u origin branchname
17. git checkout master
18. git diff master branchname
19. (repeat 2-5 if necessary)
20. git merge branchname
21. (repeat 2-5 if necessary)
22. git branch -a (lists all branches)
23. git branch -d (use -D to force delete)

## Check history and rewind

24. git log --pretty=oneline
25. git fetch origin (override local changes)
26. git reset --hard origin/master
27. git checkout -- filename (restore previous version of file)
28. git reset —hard HEAD~ (revert to previous commit)

## Resources

[git - the simple guide](https://rogerdudler.github.io/git-guide/)
