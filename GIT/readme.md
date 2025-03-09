# Interactive Git Commands Guide

This guide covers various Git commands used for version control, branch management, staging, committing, pushing changes, and handling conflicts. The commands are organized based on their functionality with explanations and usage examples.

## 1. Git Version

**Command:**
```bash
git --version
```
> **Description:**
Displays the current version of Git installed on your system.

## 2. Initialize a Git Repository

**Command:**
```bash
git init
```
> **Description:**
Initializes a new Git repository in the current directory.


## 3. Staging Changes

**Command:**
```bash
git add .
```
> **Description:**
Stages all changes (new, modified, or deleted files) for commit.

## 4. Setting Up Remote Repository

**Command:**
```bash
git remote add origin https://github.com/heeranwalnitish/Python-Practice.git
```
> **Description:**
Displays the current version of Git installed on your system.

## 5. Pushing Changes to Remote
**Command**:
```
git push origin master
```
> **Description:**: Pushes the committed changes to the master branch of the remote repository.

## 6. Reverting Changes
#### 6.1 Discarding Changes in a File
 **Command**:
```bash
 git checkout -- <file_name>
 ```
> **Description**: Reverts the changes made to a specific file. For example, git checkout -- 1.txt will revert changes made to the file 1.txt.

**Example**:

```bash
git checkout -- 1.txt
```
#### 6.2 Discarding Changes in All Files
**Command**:

```bash
git checkout .
```
> **Description** : Reverts changes in all modified files in the working directory.

## 7. Unstaging Changes
#### 7.1 Unstage a Single File
**Command**:

```bash
git reset HEAD <file_name>
```
> **Description** : Unstages a file from the staging area. For example, git reset HEAD 1.txt will unstage 1.txt.

**Example**:

```bash
git reset HEAD 1.txt
```
#### 7.2 Unstage All Files
**Command**:
```bash
git reset HEAD *
```
>**Description**: Unstages all files in the staging area.

## 8. Basic Git Workflow
 - Create a directory and change into it:

    ```bash 
    mkdir devops && cd devops
- Create files 1.txt, 2.txt, and 3.txt.
- Initialize a Git repository:

    ```bash
    git init
- Check the status:

    ```bash
    git status
- Add a specific file to staging:

    ```bash
    git add 1.txt
- Set user email and name for Git:
    ```bash
    git config --global user.email "nitishkumar231998@gmail.com"
    git config --global user.name "nitishkumar231998@gmail.com"
- Check status again to verify staging:
    ```bash
    git status
 - Add all files to staging:
    ```bash
    git add .
- Commit the changes:

    ```bash
    git commit -m "Changes are to be saved"
- Create a GitHub account and repository.
- Connect the remote repository:
    ```bash
    git remote add origin <repository_url>
- Push all changes to the remote repository:
    ```bash
    git push origin master
- Verify the changes on GitHub.

## 9. Cloning and Working with Repositories
#### 9.1 Clone the Repository
**Command**:

```bash
git clone <repository_url>
```
> **Description** : Clones the remote repository into a local directory.

#### 9.2 Add and Push a New File to the Remote
- Create a directory test and change into it.
- Clone the project into the test directory:
    ```bash
    git clone <repository_url>
- Add a new file 4.txt and push it:

    ```bash
    git add 4.txt
    git commit -m "Added 4.txt"
    git push origin master
## 10. Working with Branches
#### 10.1 Create a New Branch
**Command**:

```bash
git branch feature1
``` 
> **Description** : Creates a new branch named feature1.

#### 10.2 Switch Between Branches
**Command**:
```bash
git checkout <branch_name>
```
> **Description** : Switches to the specified branch. For example, git checkout feature1 switches to the feature1 branch.

#### 10.3 List All Branches
**Command** :
```bash
git branch
```
> **Description** : Lists all the branches in the repository. The current branch will be marked with a *.

#### 10.4 Delete a Branch
**Command**:
```bash
git branch -D feature1
```
> **Description** : Deletes the specified branch (feature1 in this case).

## 11. Working with Commits
#### 11.1 View Commit History
**Command**:

```bash
git log
```
> **Description** : Displays the commit history for the current branch.

#### 11.2 View Commit History with a Graph
**Command**:
```bash
git log --graph
```
> **Description**: Displays the commit history with a visual graph showing branch merges.

#### 11.3 View Commit History in One Line
**Command**:
```bash
git log --graph --pretty=oneline
```
> **Description** : Displays the commit history in a concise, one-line format. 

## 12. Stashing Changes
#### 12.1 Stash Changes
**Command**:
```bash
git stash
```
> **Description** : Temporarily stores changes that are not yet committed, allowing you to switch branches or perform other actions.

#### 12.2 Apply Stashed Changes
** Command**:
```bash
git stash pop
```
> **Description** : Restores the most recently stashed changes back into the working directory.

## 13. Handling Uncommitted Changes
#### 13.1 Discard Changes in a File
**Command**:

```bash

git checkout -- <file_name>
```
> **Description**: Discards uncommitted changes made to a specific file.

#### 13.2 Discard Changes in All Files
**Command**:
```bash
git checkout -- .
```
> **Description** : Discards uncommitted changes in all files.

## 14. Reset and Revert Changes
#### 14.1 Reset to a Specific Commit
** Command **:
```bash
git reset --hard <commit_id>
```
> **Description** : Resets the repository to a specific commit, discarding all changes after that commit.

##### 14.2 Revert a Commit
**Command**:
```bash
git revert <commit_id>
```
> **Description** : Reverts the changes made by a specific commit.

#### 15. Merging and Rebasing
## 15.1 Merge Two Branches
**Command**:
```bash
git merge <branch_name>
```
> **Description** : Merges the specified branch into the current branch.

#### 15.2 Rebase a Branch onto Another
**Command**:
```bash
git rebase <branch_name>
```
> **Description ** : Rebases the current branch onto the specified branch, allowing for a cleaner history.


