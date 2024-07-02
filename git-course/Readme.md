# Basics of Git and GitHub
## Table of contents
+ [Git and GitHub](#git-and-github)
    + [Git](#git)
    + [GitHub](#github)
    + [Git Vs GitHub](#git-vs-github)
+ [Repository](#repository)
    + [Repository initialization](#repository-initialization)
+ [Clone](#clone)
    + [1. Cloning Using HTTPS](#1-cloning-using-https)
    + [2. Cloning Using SSH](#2-cloning-using-ssh)
    + [3. Cloning Using Git Protocol](#3-cloning-using-git-protocol)
+ [Commit](#commit)
    + [1. git commit -m "commit message"](#1-git-commit--m-commit-message)
    + [2. git add](#2-git-add-)
    + [3. git add.](#3-git-add--)
    + [4. git status](#4-git-status)
    + [5. git log](#5-git-log)
    + [6. git commit --amend](#6-git-commit---amend)
    + [7. git reset HEAD <file>](#7-git-reset-head-file)
    + [8. git revert <commit-hash>](#8-git-revert-)
    + [9. git cherry-pick <commit-hash>](#9-git-cherry-pick-)
    + [10. git show <commit-hash>](#10-git-show-)
    + [11. git diff](#11git-diff)
    + [12. git reset --soft <commit-hash>](#12-git-reset---soft-)
    + [13. git reset --hard <commit-hash>](#13-git-reset---hard-)
    + [14. git stash](#14-git-stash)
    + [15. git stash apply](#15git-stash-apply)
+ [Branch](#branch)
    + [Creating and Switching Branches](#creating-and-switching-branches)
        + [1. Create a new branch](#1-create-a-new-branch)
        + [2. Switch to a branch](#2-switch-to-a-branch)
        + [3. Create and switch to a new branch](#3-create-and-switch-to-a-new-branch)
    + [Managing branches](#managing-branches)
        + [4. List all branches](#4-list-all-branches)
        + [5. Delete a branch](#5-delete-a-branch)
        + [6. Force delete a branch (if not fully merged)](#6-force-delete-a-branch-if-not-fully-merged)
    + [Merging Branches](#merging-branches) 
        + [7. Merge a branch into the current branch](#7-merge-a-branch-into-the-current-branch)
        + [8. Abort a merge in progress](#8-abort-a-merge-in-progress)
    + [Branch Tracking and Remote Branches](#branch-tracking-and-remote-branches)
        + [9. List remote branches](#9-list-remote-branches)
        + [10. Create a local branch tracking a remote branch](#10-create-a-local-branch-tracking-a-remote-branch)
+ [Merge](#merge)
    + [1. Merge a branch into the current branch](#1-merge-a-branch-into-the-current-branch)
    + [2. Abort a merge in progress](#2-abort-a-merge-in-progress)


## Git and GitHub

### Git
Git is a distributed version control system designed to handle everything from small to very large projects with speed and efficiency. 

### GitHub
GitHub is a web-based platform that uses Git for version control. It provides a collaborative environment for software development.GitHub allows you to create, store, change, merge, and collaborate on files or code.

### Git Vs GitHub
|Git|GitHub|
|---|---|
|Git is a software.|GitHub is a service.|
|Git is a command-line tool|GitHub is a graphical user interface|
|Git was first released in 2005.|GitHub was launched in 2008.|
|Git is open-source licensed.|GitHub includes a free-tier and pay-for-use tier.|
|Git is installed locally on the system.|GitHub is hosted on the web|
|Git competes with CVS, Azure DevOps Server, Subversion, Mercurial, etc.|GitHub competes with GitLab, Bit Bucket, AWS Code Commit, etc.|

## Repository
A repository (or repo) is a data structure that stores metadata and an object database for a project. It contains all the files, history, and configuration settings necessary to manage and track changes to the project over time.
### Repository initialization
```sh
git init
```

## Clone
The clone command is used to create a copy of an existing repository. This command is often used to obtain a local copy of a remote repository.Here are three common ways to clone a repository:

### 1. Cloning Using HTTPS
The HTTPS method is commonly used because it requires minimal setup and works well behind proxies and firewalls. It's often used for public repositories or when you prefer not to set up SSH keys.
```sh
git clone https://github.com/user/repo.git
```
### 2. Cloning Using SSH
The SSH method is more secure and is preferred for private repositories. It requires setting up SSH keys on your local machine and configuring them on the remote server.
```sh
git clone git@github.com:user/repo.git
```
### 3. Cloning Using Git Protocol
The Git protocol is efficient and fast but generally requires that the remote server support the Git protocol. It's less commonly used because it doesn't provide built-in authentication and is typically used for public repositories.
```sh
git clone git://github.com/user/repo.git
```
## Commit
Coomit in Git is a snapshot of your repository at a specific point in time. It captures the current state of the files in the repository, including the changes made since the last commit. Commits are fundamental to version control in Git. 
```sh
git commit
```
Some key commands related to commit:
### 1. git commit -m "commit message": 
Creates a new commit with the changes in the staging area and includes a commit message.
```sh
git commit -m "Initial commit"
```
### 2. git add <file>:
Adds a specific file to the staging area.
```sh
git add file.txt
```
### 3. git add . :
Adds all changed files in the current directory and its subdirectories to the staging area.
```sh
git add.
```
### 4. git status: 
Shows the status of changes as untracked, modified, or staged.
```sh
git status
```
### 5. git log: 
Displays the commit history.
```sh
git log
```
### 6. git commit --amend:
Modifies the most recent commit with additional changes or a new commit message.
```sh
git commit --amend -m "Updated commit message"
```
### 7. git reset HEAD <file>: 
Removes a file from the staging area, keeping the changes in the working directory.
```sh
git reset HEAD file.txt
```
### 8. git revert <commit-hash>: 
Creates a new commit that undoes the changes of a specified commit.
```sh
git revert abc1234
```
### 9. git cherry-pick <commit-hash>: 
Applies the changes from a specific commit to the current branch.
```sh 
git cherry-pick abc1234
```
### 10. git show <commit-hash>: 
Displays the details and changes of a specific commit.
```sh
git show abc1234
```
### 11.git diff: 
Shows the differences between the working directory and the staging area, or between commits.
```sh
git diff
git diff HEAD
git diff abc1234 abc5678
```
### 12. git reset --soft <commit-hash>: 
Resets the current branch to the specified commit, keeping changes in the staging area.
```sh
git reset --soft abc1234
```
### 13. git reset --hard <commit-hash>: 
Resets the current branch to the specified commit, discarding all changes in the working directory and staging area.
```sh
git reset --hard abc1234
```
### 14. git stash: 
Temporarily saves changes in the working directory that are not ready to be committed.
```sh
git stash
```
### 15.git stash apply: 
Applies the most recent stash to the working directory
```sh
git stash apply
```

## Branch
Branch is a movable pointer to a specific commit. It allows you to develop features, fix bugs, or experiment independently of the main project line. 
Here are some key concepts and commands related to branches in Git:
### Creating and Switching Branches
#### 1. Create a new branch:
```sh
git branch <branch-name>
```
#### 2. Switch to a branch:
```sh
git checkout <branch-name>
```
#### 3. Create and switch to a new branch:
```sh
git checkout -b <branch-name>
```
### Managing Branches
#### 4. List all branches:
```sh
git branch
```
#### 5. Delete a branch:
```sh
git branch -d <branch-name>
```
#### 6. Force delete a branch (if not fully merged):
```sh
git branch -D <branch-name>
```
### Merging Branches
#### 7. Merge a branch into the current branch:
```sh
git merge <branch-name>
```
#### 8. Abort a merge in progress:
```sh
git merge --abort
```
### Branch Tracking and Remote Branches
#### 9. List remote branches:
```sh
git branch -r
``` 
#### 10. Create a local branch tracking a remote branch:
```sh 
git checkout -b <branch-name> origin/<branch-name>
```
## Merge
Merge refers to combining changes from one branch (often a feature branch) into another branch (typically the main branch, like `main` or `master`). This process integrates the changes and reconciles any differences between the branches. It's commonly used to incorporate completed features or fixes into the main codebase.
### 1. Merge a branch into the current branch:
```sh
git merge <branch-name>
```
### 2. Abort a merge in progress:
```sh
git merge --abort
```





