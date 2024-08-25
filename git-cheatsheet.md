# Git Cheat Sheet

## Basic Commands

### Initialize a Repository
**Syntax:**
```bash
git init
```
**Example:**
```bash
cd my-project
git init
```
*Creates a new Git repository in the `my-project` directory.*

---

### Clone a Repository  
**Syntax:**
```bash
git clone <repository-url>
```
**Example:**
```bash
git clone https://github.com/user/repo.git
```
*Copies the remote repository located at the specified URL to your local machine.*

---

### Check Status
**Syntax & Example:**
```bash
git status
```
*Displays the current state of the working directory and staging area.*

---

### Add Changes
**Syntax:**
```bash
git add <file>
```
**Example:**
```bash
git add file.txt
```
*Stages the file `file.txt` for the next commit. 
To stage all changes:*
```bash
git add .
```

---

### Commit Changes
**Syntax:**
```bash
git commit -m "<commit message>"
```
**Example:**
```bash
git commit -m "Initial commit"
```
*Records the staged changes in the repository with a descriptive message.*

---

## Branching and Merging

### Create a New Branch
**Syntax:**
```bash
git branch <branch-name>
```
**Example:**
```bash
git branch feature-branch
```
*Creates a new branch named `feature-branch`.*

---

### Switch Branches
**Syntax:**
```bash
git checkout <branch-name>
```
**Example:**
```bash
git checkout feature-branch
```
*Switches to the `feature-branch`.*

---

### Merge Branches
**Syntax:**
```bash
git merge <branch-name>
```
**Example:**
```bash
git checkout main
git merge feature-branch
```
*Switches to the `main` branch and merges changes from `feature-branch` into it.*

---

### Delete a Branch
**Syntax:**
```bash
git branch -d <branch-name>
```
**Example:**
```bash
git branch -d feature-branch
```
*Deletes the `feature-branch` if it has been merged.*

---

## Remote Repositories

### View Remote Repositories
**Syntax:**
```bash
git remote -v
```
**Example:**
```bash
git remote -v
```
*Lists all remote connections for your repository.*

---

### Push Changes
**Syntax:**
```bash
git push <remote> <branch>
```
**Example:**
```bash
git push origin main
```
*Uploads local changes from the `main` branch to the remote repository named `origin`.*

---

### Pull Changes
**Syntax:**
```bash
git pull <remote> <branch>
```
**Example:**
```bash
git pull origin main
```
*Fetches and merges changes from the remote `main` branch into your local branch.*

---

## Undoing Changes

### Revert a Commit
**Syntax:**
```bash
git revert <commit-id>
```
**Example:**
```bash
git revert 1a2b3c4
```
*Creates a new commit that undoes changes from the specified commit ID `1a2b3c4`.*

---

### Reset Changes
**Syntax:**
```bash
git reset --hard <commit-id>
```
**Example:**
```bash
git reset --hard 1a2b3c4
```
*Resets the current branch to the specified commit, discarding all changes after that commit.*

---

## Viewing History

### View Commit History
**Syntax & Example:**
```bash
git log
```
*Displays the commit history for the current branch.*

---

### Graphical History
**Syntax & Example:**
```bash
git log --oneline --graph
```
*Shows a simplified view of the commit history in a graphical format.*

---

## Stashing Changes

### Stash Changes
**Syntax & Example:**
```bash
git stash
```
*Temporarily saves changes that are not ready to be committed.*

---

### Apply Stashed Changes
**Syntax & Example:**
```bash
git stash pop
```
*Restores the most recently stashed changes and removes them from the stash list.*

---

This cheat sheet provides a quick reference to essential Git commands, complete with syntax and examples. By practicing these commands, you can efficiently manage your Git repositories and streamline your version control workflow!
