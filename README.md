# Codes that were performed according to questions of Git Assignment 3
# Git Assignment 3

## Windows PowerShell
```
Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

Install the latest PowerShell for new features and improvements! https://aka.ms/PSWindows
```

## Step 1: Initializing the Git Repository and Creating Branches
```powershell
PS C:\Users\HP> mkdir Git_Assignment_3
PS C:\Users\HP> cd Git_Assignment_3
PS C:\Users\HP\Git_Assignment_3> git init
Initialized empty Git repository in C:/Users/HP/Git_Assignment_3/.git/

PS C:\Users\HP\Git_Assignment_3> git branch develop
fatal: not a valid object name: 'master'

PS C:\Users\HP\Git_Assignment_3> New-Item Start.txt -ItemType File
PS C:\Users\HP\Git_Assignment_3> git add Start.txt
PS C:\Users\HP\Git_Assignment_3> git commit -m 'Initial commit with start.txt'
[master (root-commit) 2c2e747] Initial commit with start.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Start.txt

PS C:\Users\HP\Git_Assignment_3> git branch develop
PS C:\Users\HP\Git_Assignment_3> git branch f1
PS C:\Users\HP\Git_Assignment_3> git branch f2
```

## Step 2: Committing `main.txt` to the Master Branch
```powershell
PS C:\Users\HP\Git_Assignment_3> New-Item main.txt -ItemType File
PS C:\Users\HP\Git_Assignment_3> git add main.txt
PS C:\Users\HP\Git_Assignment_3> git commit -m 'Added main.txt in master branch'
[master 5357887] Added main.txt in master branch
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 main.txt
```

## Step 3: Committing `develop.txt` in the Develop Branch
```powershell
PS C:\Users\HP\Git_Assignment_3> git checkout develop
Switched to branch 'develop'
PS C:\Users\HP\Git_Assignment_3> New-Item develop.txt -ItemType File
PS C:\Users\HP\Git_Assignment_3> git add develop.txt
PS C:\Users\HP\Git_Assignment_3> git commit -m "Added develop.txt in develop branch"
[develop 73d44ca] Added develop.txt in develop branch
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 develop.txt
```

## Step 4: Committing `f1.txt` in the f1 Branch
```powershell
PS C:\Users\HP\Git_Assignment_3> git checkout f1
Switched to branch 'f1'
PS C:\Users\HP\Git_Assignment_3> New-Item f1.txt -ItemType File
PS C:\Users\HP\Git_Assignment_3> git add f1.txt
PS C:\Users\HP\Git_Assignment_3> git commit -m "Added f1.txt in f1 branch"
[f1 18c6b60] Added f1.txt in f1 branch
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 f1.txt
```

## Step 5: Committing `f2.txt` in the f2 Branch
```powershell
PS C:\Users\HP\Git_Assignment_3> git checkout f2
Switched to branch 'f2'
PS C:\Users\HP\Git_Assignment_3> New-Item f2.txt -ItemType File
PS C:\Users\HP\Git_Assignment_3> git add f2.txt
PS C:\Users\HP\Git_Assignment_3> git commit -m "Added f2.txt in f2 branch"
[f2 4a2445b] Added f2.txt in f2 branch
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 f2.txt
```

## Step 6: Pushing All Branches to GitHub
```powershell
PS C:\Users\HP\Git_Assignment_3> git remote add origin https://github.com/Mamatayadav1/Git_Assignment_1.3.git

PS C:\Users\HP\Git_Assignment_3> git push -u origin master
PS C:\Users\HP\Git_Assignment_3> git push -u origin develop
PS C:\Users\HP\Git_Assignment_3> git push -u origin f1
PS C:\Users\HP\Git_Assignment_3> git push -u origin f2
```

## Step 7: Deleting the `f2` Branch Locally and Remotely
```powershell
PS C:\Users\HP\Git_Assignment_3> git branch -d f2
error: cannot delete branch 'f2' used by worktree at 'C:/Users/HP/Git_Assignment_3'

PS C:\Users\HP\Git_Assignment_3> git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

PS C:\Users\HP\Git_Assignment_3> git branch -d f2
warning: deleting branch 'f2' that has been merged to
         'refs/remotes/origin/f2', but not yet merged to HEAD
Deleted branch f2 (was 4a2445b).

PS C:\Users\HP\Git_Assignment_3> git push origin --delete f2
To https://github.com/Mamatayadav1/Git_Assignment_1.3.git
 - [deleted]         f2
```

## Checking Remote Branches
```powershell
PS C:\Users\HP\Git_Assignment_3> git branch -r
  origin/develop
  origin/f1
  origin/master
```

This README provides a structured approach for setting up a Git repository, creating branches, committing files, pushing branches to GitHub, and deleting branches.
