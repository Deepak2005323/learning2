# Git

## What is Git?

Git is a Distributed Version Control System (DVCS) used to track changes in source code and collaborate with multiple developers.

### Key Benefits

- Tracks code changes over time
- Supports team collaboration
- Maintains version history
- Enables branching and merging
- Allows rollback to previous versions

---

## Core Concepts

### Repository

A repository (repo) is a storage location for your project and its history.

There are two types:

- Local Repository
- Remote Repository

### Working Area

Where files are created and modified.

### Staging Area

Temporary area where changes are prepared before committing.

### Commit

A snapshot of the project at a specific point in time.

---

## Git Workflow

```text
Working Directory
       │
       ▼
Staging Area
       │
       ▼
    Commit
       │
       ▼
Remote Repository
```

---

## Initialize Repository

Create a new Git repository:

```bash
git init
```

Check hidden files:

```bash
ls -la
```

---

## Check Repository Status

```bash
git status
```

Shows:

- Modified files
- Untracked files
- Staged files

---

## Add Files to Staging Area

Add specific file:

```bash
git add file.txt
```

Add all files:

```bash
git add .
```

---

## Create a Commit

```bash
git commit -m "Initial commit"
```

Example:

```bash
git commit -m "Added user management notes"
```

---

## View Commit History

Detailed log:

```bash
git log
```

Compact log:

```bash
git log --oneline
```

---

## Connect to Remote Repository

Add GitHub repository:

```bash
git remote add origin <repository-url>
```

Example:

```bash
git remote add origin https://github.com/Deepak2005323/linux-notes.git
```

Verify:

```bash
git remote -v
```

---

## Push Changes

Push to remote repository:

```bash
git push origin main
```

First push:

```bash
git push -u origin main
```

---

## Clone Repository

HTTPS:

```bash
git clone <repository-url>
```

SSH:

```bash
git clone git@github.com:user/repository.git
```

---

# Branching

## Create Branch

```bash
git branch feature-login
```

## Switch Branch

```bash
git checkout feature-login
```

## Create and Switch

```bash
git checkout -b feature-login
```

## List Branches

```bash
git branch
```

---

# Merging

Switch to target branch:

```bash
git checkout main
```

Merge feature branch:

```bash
git merge feature-login
```

---

# Pull Requests

Common GitHub workflow:

1. Create branch
2. Make changes
3. Push branch
4. Create Pull Request
5. Review changes
6. Merge into main

---

# Merge Conflicts

When two developers modify the same lines in a file, Git cannot decide which change to keep automatically.

Conflict markers:

```text
<<<<<<< HEAD
Current branch changes
=======
Incoming branch changes
>>>>>>> feature-branch
```

Steps:

```bash
# Fix file manually

git add .
git commit
```

---

# Fetch vs Pull

## Fetch

Downloads changes without merging.

```bash
git fetch origin main
```

## Pull

Downloads and merges.

```bash
git pull origin main
```

---

# Rebase

Reapplies commits on top of another branch.

```bash
git rebase main
```

Benefits:

- Cleaner history
- Fewer merge commits

---

# Interactive Rebase

Used to clean commit history.

```bash
git rebase -i HEAD~4
```

Common options:

```text
pick
reword
edit
squash
fixup
drop
```

---

# Cherry Pick

Apply a specific commit from another branch.

```bash
git cherry-pick <commit-id>
```

Example:

```bash
git cherry-pick a1b2c3d
```

---

# Git Reset

## Soft Reset

Moves HEAD but keeps staged changes.

```bash
git reset --soft HEAD~1
```

## Hard Reset

Removes commit and changes.

```bash
git reset --hard HEAD~1
```

⚠️ Use with caution.

---

# Git Revert

Undo a commit by creating a new commit.

```bash
git revert <commit-id>
```

Example:

```bash
git revert a1b2c3d
```

---

# Git Stash

Temporarily save uncommitted work.

Store changes:

```bash
git stash
```

View stashes:

```bash
git stash list
```

Restore latest stash:

```bash
git stash pop
```

Restore specific stash:

```bash
git stash pop stash@{1}
```

---

# Useful Commands

```bash
git status
git add .
git commit -m "message"
git log --oneline
git push
git pull
git fetch
git branch
git checkout
git merge
git rebase
git stash
git revert
git reset
```

---

