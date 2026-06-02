# SOA Internship Assignment Execution Steps

This document outlines the step-by-step process and commands used to complete the SOA Internship Assignment.

## PART 1 — Linux Navigation & File Management

### Task 1 & 2 — Create Workspace and Project Structure
First, we created the main folder and the required subdirectories.

```bash
mkdir PuspalAssignment
cd PuspalAssignment
mkdir docs scripts logs images notes
```

### Task 3 — Create Files
Next, we created the required files inside the directories.
```bash
touch docs/git.txt docs/linux.txt notes/commands.txt scripts/start.sh logs/app.log
```
*(Note: In PowerShell, `New-Item` or `echo` was used as the equivalent for `touch`)*

### Task 4 — Add Content
We added the required text to `git.txt` and `linux.txt`.

**For `git.txt`**:
```bash
echo "1. What is Git
2. Why Git is useful
3. Difference between Git and GitHub" > docs/git.txt
```

**For `linux.txt`**:
```bash
echo "1. What is Linux
2. Three commands learned" > docs/linux.txt
```

### Task 5 — Linux Search
We searched for the word "Git" inside all files.
```bash
grep -r "Git" .
```

---

## PART 2 — Git Fundamentals

### Task 6 & 7 — Initialize Repository and First Commit
We staged all the new files and folders, and committed them.
```bash
git add .
git commit -m "Initial Project Setup"
```

### Task 8 — Track Changes
We modified `docs/git.txt` to add a new line, checked the status, and committed the changes.
```bash
echo "Three git commands learned" >> docs/git.txt
git status
git diff
git add docs/git.txt
git commit -m "Updated git notes"
```

### Task 9 — Branching
We created a new branch named `feature/puspa` and verified it.
```bash
git checkout -b feature/puspa
git branch
```

### Task 10 — Feature Development
Inside the new branch, we created `notes/learning.md` and committed it.
```bash
echo "My top 5 learnings" > notes/learning.md
git add notes/learning.md
git commit -m "Added learning summary"
```

### Task 11 — Merge Branch
We switched to the `main` branch and merged our feature branch into it.
```bash
git checkout main
git merge feature/puspa
```

---

## PART 3 — GitHub & Final Adjustments

### Task 12 — Create GitHub Repository & Push
We pushed the feature branch to the remote GitHub repository so that a Pull Request could be created.
```bash
git push origin feature/puspa
```

### Additional Step: Renaming the Workspace Folder
We renamed the root folder to `PuspalAssignment` using Git to keep the history intact, committed the rename, and pushed the changes.
```bash
git mv internship-assignment PuspalAssignment
git commit -m "Rename internship-assignment to PuspalAssignment"
git push origin feature/puspa
```
