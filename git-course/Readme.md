## Git
Git is a distributed version control system designed to handle everything from small to very large projects with speed and efficiency. 

## GitHub
GitHub is a web-based platform that uses Git for version control. It provides a collaborative environment for software development.GitHub allows you to create, store, change, merge, and collaborate on files or code.

## Git Vs GitHub

## Clone

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
In Git, a branch is a movable pointer to a specific commit. It allows you to develop features, fix bugs, or experiment independently of the main project line. Here are some key concepts and commands related to branches in Git:

## Remote

