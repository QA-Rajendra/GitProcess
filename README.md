# GitProcess
Git all Process
# Complete Git Guide with Commands, Flowcharts, and Examples

---

## 1. What is Git?

Git is a distributed version control system that helps track changes in source code during software development.

**Key Features:**

* Distributed (local + remote repo)
* Branching & Merging
* Collaboration via platforms like GitHub
* Track History

---

## 2. Git Installation & Configuration

### Installation:

* Download Git: [https://git-scm.com](https://git-scm.com)
* Install with default options

### Global Config:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global core.editor "code --wait"
```

---

## 3. Git Architecture

### Flow:

```
Working Directory (Workspace)
    ↓ git add
Staging Area (Index)
    ↓ git commit
Local Repository
    ↓ git push
Remote Repository (GitHub)
```

---

## 4. First Git Commit Setup

### Steps:

1. Create GitHub Account and Repo
2. Initialize Git

```bash
git init
git remote add origin https://github.com/user/repo.git
git add .
git commit -m "Initial commit"
git push -u origin master
```

3. Setup Authentication (PAT or Credential helper)

---

## 5. Second Commit

### Operations:

* Create: `touch file.txt`
* Update: Edit using any editor
* Delete: `rm file.txt`

### Workflow:

```bash
git add .
git commit -m "Added new feature"
git push origin master
```

---

## 6. Git Logs / History

```bash
git log
git log --oneline
git log --author="name"
git log --since="2 days ago"
git show <commit>
```

---

## 7. Git Diff

```bash
git diff                # Working dir vs stage
git diff --staged       # Stage vs repo
git diff commit1 commit2
```

---

## 8. Git Blame / Shortlog

```bash
git blame file.java
git shortlog -s -n
```

---

## 9. Git Local Branching

```bash
git branch feature-x
git checkout feature-x
# or
git switch -c feature-x
git add .
git commit -m "Feature done"
git push origin feature-x
```

---

## 10. Pull Request (PR)

### Flow:

```
Feature Branch → Push to GitHub → PR → Review → Merge
```

### PR Actions:

* Approve
* Comment
* Request changes
* Merge

---

## 11. Branch Commands

```bash
git branch              # List local
git branch -r           # List remote
git branch -d feature-x
git checkout branch-name
git switch branch-name
```

---

## 12. Clone vs Fork

### Clone:

```bash
git clone https://github.com/user/repo.git
```

### Fork:

* Create copy on GitHub
* Clone fork locally

---

## 13. Local Merge

```bash
git checkout master
git merge feature-x
```

---

## 14. Tag and Releases

```bash
git tag v1.0
git tag
git push origin v1.0
```

* Create Release from Tag on GitHub

---

## 15. Fetch vs Pull

```bash
git fetch       # Download only
git pull        # Fetch + Merge
```

---

## 16. Merge vs Rebase

### Merge:

```bash
git merge branch
```

* Maintains history

### Rebase:

```bash
git rebase branch
```

* Cleaner linear history

---

## 17. Cherry Pick

```bash
git cherry-pick <commit>
```

---

## 18. Git Stash

```bash
git stash
git stash list
git stash pop
```

---

## 19. Merge Conflict

* Happens when the same lines are edited in both branches.
* Git shows `<<<< HEAD` conflict markers.
* Resolve manually, then:

```bash
git add .
git commit
```

---

## 20. Git Aliases

```bash
git config --global alias.s "status"
git config --global alias.co "checkout"
git config --global alias.lg "log --oneline --graph"
```

---

## 21. Compare Two Commits

```bash
git diff commit1 commit2
```

---

## 22. Git Reset

```bash
git reset --soft HEAD~1
# unstage but keep code
git reset --mixed HEAD~1
# remove code too
git reset --hard HEAD~1
```

---

## 23. Git Revert

```bash
git revert <commit>
```

* Safely undo changes
* Adds a new commit

---

## ✅ Summary:

This Git guide provides real-world workflows, syntax, and best practices across the lifecycle of version control, suitable for developers, testers, and
