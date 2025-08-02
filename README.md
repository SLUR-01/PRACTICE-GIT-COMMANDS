# 📘 Git & GitHub Command Guide

This guide serves as a comprehensive reference for using **Git** (version control system) and **GitHub** (remote repository host). Each command is explained with practical context, making it ideal for beginners and useful as a refresher for experienced developers.

---

## 🛠️ Initial Project Setup

```bash
git init
```

Initializes a new Git repository in your current folder. This sets up all necessary files for Git tracking.

```bash
git remote add origin https://github.com/your-username/your-repo.git
```

Links your local repository to a remote GitHub repository. Replace the URL with your actual repo.

```bash
git branch -M main
```

Renames the current branch to `main` (standard practice as the default branch).

---

## 📅 Cloning an Existing Repository

```bash
git clone https://github.com/username/repo.git
```

Downloads an existing project from GitHub into your local machine. This also sets the remote to `origin`.

---

## 💾 Working with Changes

```bash
git status
```

Displays the status of your working directory: which files are modified, staged, or untracked.

```bash
git add .
```

Stages **all** changes (new, modified, or deleted files) for the next commit.

```bash
git add filename.js
```

Stages a **specific file** only.

```bash
git commit -m "Your commit message"
```

Saves the staged changes to the local repository with a descriptive message.

---

## 🚀 Pushing Changes to GitHub

```bash
git push origin main
```

Uploads your local `main` branch commits to the remote repository on GitHub.

```bash
git push origin branch-name
```

Pushes a different branch (like a feature branch) to GitHub.

---

## 🔄 Pulling Changes from GitHub

```bash
git pull origin main
```

Fetches and integrates changes from the remote `main` branch into your current local branch. Useful for syncing before working or merging.

---

## 🌿 Branching (Creating and Switching)

```bash
git branch
```

Lists all **local** branches in your repository.

```bash
git checkout -b feature-name
```

Creates a **new branch** called `feature-name` and switches to it.

```bash
git checkout branch-name
```

Switches to an existing branch.

```bash
git push origin branch-name
```

Pushes the newly created or updated branch to GitHub.

---

## 🔀 Merging Branches

```bash
git checkout main
```

Switch to the `main` branch (or any target branch where you want to merge changes).

```bash
git pull origin main
```

Ensure your local main branch is up to date.

```bash
git merge feature-name
```

Merge the changes from `feature-name` into `main`.

```bash
git push origin main
```

Push the merged result to GitHub.

---

## ⚔️ Resolving Merge Conflicts

Git will mark conflicts within files like this:

```text
<<<<<<< HEAD
Your teammate's changes
=======
Your changes
>>>>>>> feature-branch
```

Manually edit the file to resolve the conflict, then run:

```bash
git add conflicted-file.js
git commit -m "Resolved conflict in conflicted-file.js"
git push origin main
```

---

## 🧪 Undoing Changes

```bash
git restore filename
```

Restores the file to the last committed state. Useful for discarding local changes.

```bash
git reset --soft HEAD~1
```

Undo the last commit, but keep all changes staged (ready to recommit).

```bash
git reset --hard HEAD~1
```

Completely removes the last commit **and** all local changes. Use with caution — changes cannot be recovered.

---

### ✅ Best Practices

* Always `pull` before starting work to avoid conflicts.
* Use descriptive commit messages.
* Keep feature branches short-lived and merge frequently.
* Never use `--hard` reset unless you're absolutely sure.
* Always check `git status` before committing or pushing.
