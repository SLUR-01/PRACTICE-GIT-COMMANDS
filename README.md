# 📘 Git & GitHub Command Guide

This guide serves as a handy reference for using Git and GitHub during development. Each command includes an explanation to help you understand its purpose.

---

## 🛠️ Initial Setup

```bash
git init
git remote add origin https://github.com/your-username/your-repo.git
git branch -M main

📥 Cloning a Repository
git clone https://github.com/username/repo.git
Clone an existing GitHub repository to your local machine.


💾 Working with Changes
git status
git add .
git add filename.js
git commit -m "Your commit message"

🚀 Pushing Changes
git push origin main
git push origin branch-name

🔄 Pulling Changes
git pull origin main
(Pull the latest changes from the remote main branch and merge them with your local branch.)

🌿 Branching
git branch
(List all local branches.)
git checkout -b feature-name
git checkout branch-name
git push origin branch-name

🔀 Merging Branches
git checkout main
git pull origin main
(Make sure your main is up to date before merging.)
git merge feature-name
git push origin main

⚔️ Resolving Merge Conflicts
Git marks conflicts in files like this:
<<<<<<< HEAD
Your teammate's changes
=======
Your changes
>>>>>>> feature-branch

Manually edit the file to resolve the conflict.

Then run:

git add conflicted-file.js
git commit -m "Resolved conflict in conflicted-file.js"
git push origin main


🧪 Undoing Changes
git restore filename

git reset --soft HEAD~1

git reset --hard HEAD~1