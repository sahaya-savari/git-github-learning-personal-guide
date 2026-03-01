# Git & GitHub — Complete Practical Guide

## Table of Contents
1. [Introduction](#introduction)
	- [Quick Start (5 Steps)](#quick-start-5-steps)
2. [What is Git](#what-is-git)
3. [What is GitHub](#what-is-github)
4. [Core Terminology](#core-terminology)
   - [Emoji Quick Table](#emoji-quick-table)
5. [Installing Git (Windows)](#installing-git-windows)
6. [Initial Git Configuration](#initial-git-configuration)
7. [Creating a Repository](#creating-a-repository)
8. [Git File Lifecycle](#git-file-lifecycle)
9. [Staging Files](#staging-files)
10. [Committing Changes](#committing-changes)
11. [Connecting to GitHub](#connecting-to-github)
12. [Pushing Code](#pushing-code)
13. [Cloning Repositories](#cloning-repositories)
14. [Pulling Updates](#pulling-updates)
15. [Branching](#branching)
16. [Merging](#merging)
17. [Forking & Open-Source Workflow](#forking--open-source-workflow)
18. [Pull Requests](#pull-requests)
19. [Undoing Mistakes](#undoing-mistakes)
20. [Viewing History](#viewing-history)
21. [.gitignore](#gitignore)
22. [Authentication (HTTPS vs SSH)](#authentication-https-vs-ssh)
23. [Common Errors & Fixes](#common-errors--fixes)
24. [Best Practices](#best-practices)
25. [Daily Git Workflow](#daily-git-workflow)
26. [Conclusion](#conclusion)

---

## Chapter Navigation
| # | Emoji | Chapter | Link |
| --- | --- | --- | --- |
| 1 | 👋 | Introduction | [Go](#introduction) |
| 1.1 | 🚀 | Quick Start (5 Steps) | [Go](#quick-start-5-steps) |
| 2 | 🧠 | What is Git | [Go](#what-is-git) |
| 3 | 🌐 | What is GitHub | [Go](#what-is-github) |
| 4 | 🧩 | Core Terminology | [Go](#core-terminology) |
| 4.1 | 😀 | Emoji Quick Table | [Go](#emoji-quick-table) |
| 5 | 🧰 | Installing Git (Windows) | [Go](#installing-git-windows) |
| 6 | ⚙️ | Initial Git Configuration | [Go](#initial-git-configuration) |
| 7 | 📁 | Creating a Repository | [Go](#creating-a-repository) |
| 8 | ♻️ | Git File Lifecycle | [Go](#git-file-lifecycle) |
| 9 | ✅ | Staging Files | [Go](#staging-files) |
| 10 | 📝 | Committing Changes | [Go](#committing-changes) |
| 11 | 🔗 | Connecting to GitHub | [Go](#connecting-to-github) |
| 12 | ⬆️ | Pushing Code | [Go](#pushing-code) |
| 13 | 📥 | Cloning Repositories | [Go](#cloning-repositories) |
| 14 | ⬇️ | Pulling Updates | [Go](#pulling-updates) |
| 15 | 🌿 | Branching | [Go](#branching) |
| 16 | 🤝 | Merging | [Go](#merging) |
| 17 | 🍴 | Forking & Open-Source Workflow | [Go](#forking--open-source-workflow) |
| 18 | 📬 | Pull Requests | [Go](#pull-requests) |
| 19 | 🧹 | Undoing Mistakes | [Go](#undoing-mistakes) |
| 20 | 🧭 | Viewing History | [Go](#viewing-history) |
| 21 | 🚫 | .gitignore | [Go](#gitignore) |
| 22 | 🔐 | Authentication (HTTPS vs SSH) | [Go](#authentication-https-vs-ssh) |
| 23 | 🧯 | Common Errors & Fixes | [Go](#common-errors--fixes) |
| 24 | ⭐ | Best Practices | [Go](#best-practices) |
| 25 | 🗓️ | Daily Git Workflow | [Go](#daily-git-workflow) |
| 26 | ✅ | Conclusion | [Go](#conclusion) |

---

## Introduction
This guide teaches Git and GitHub from zero. It explains concepts first, then shows commands with simple, direct explanations. You do not need prior knowledge of version control, command-line tools, or GitHub.

## Quick Start (5 Steps)
| Step | Emoji | Command | Why |
| --- | --- | --- | --- |
| 1 | 📁 | `git init` | Start tracking a folder. |
| 2 | 🧪 | `git status` | Check what changed. |
| 3 | ✅ | `git add .` | Stage all changes. |
| 4 | 📝 | `git commit -m "Message"` | Save a snapshot. |
| 5 | ⬆️ | `git push origin main` | Back up to GitHub. |

## What is Git
Git is a tool that tracks changes to files over time. It lets you:
- Save snapshots of your work (called commits).
- See what changed and when.
- Go back to earlier versions if something breaks.
- Work with others without overwriting each other’s files.

Git works locally on your computer. You can use it without the internet.

## What is GitHub
GitHub is a website that stores Git repositories online. It lets you:
- Back up your code to the cloud.
- Share code with others.
- Collaborate by reviewing and merging changes.

GitHub is optional but very common for teamwork and open-source projects.

## Core Terminology
| Term | Emoji | Simple Meaning |
| --- | --- | --- |
| Repository (repo) | 📦 | A folder tracked by Git. |
| Commit | 📝 | A saved snapshot of your project. |
| Working directory | 🗂️ | The files on your computer you edit. |
| Staging area | ✅ | A holding area for changes you plan to commit. |
| Branch | 🌿 | A separate line of work inside a repo. |
| Merge | 🤝 | Combine changes from one branch into another. |
| Remote | 🌐 | A repo stored somewhere else (like GitHub). |
| Clone | 📥 | A full copy of a remote repo on your computer. |
| Push | ⬆️ | Send your local commits to a remote repo. |
| Pull | ⬇️ | Bring remote commits to your local repo. |
| Fork | 🍴 | Your own copy of someone else’s GitHub repo. |

## Emoji Quick Table
Use this emoji cheat sheet to remember common Git actions at a glance.

| Emoji | Meaning | Command Example |
| --- | --- | --- |
| 🌱 | Start a repo | `git init` |
| 🧪 | Check status | `git status` |
| ✅ | Stage changes | `git add .` |
| 📝 | Save a snapshot | `git commit -m "Message"` |
| 🌿 | Create a branch | `git branch feature-x` |
| 🔀 | Switch branch | `git switch feature-x` |
| 🤝 | Merge work | `git merge feature-x` |
| ⬆️ | Push to remote | `git push origin main` |
| ⬇️ | Pull updates | `git pull origin main` |
| 🧭 | View history | `git log --oneline` |
| 🧹 | Undo local changes | `git restore file.txt` |
| 🔒 | Ignore files | `.gitignore` |
| 🔑 | Authenticate | HTTPS or SSH |
| 📦 | Stash work | `git stash` |
| 🏷️ | Tag a release | `git tag v1.0.0` |
| 🔁 | Rebase branch | `git rebase main` |
| 🧯 | Reset changes | `git reset --soft HEAD~1` |
| 🔍 | Compare changes | `git diff` |
| 🛰️ | Fetch remotes | `git fetch` |

## Installing Git (Windows)
1. Go to https://git-scm.com/download/win
2. Download the installer and run it.
3. Accept the default options unless you have a specific reason to change them.
4. After installation, open “Command Prompt” or “PowerShell”.
5. Check that Git works:

```bash
git --version
```
Explanation:
- `git` is the program you installed.
- `--version` asks Git to show its version so you know it is installed.
Why this is used:
- It confirms Git is installed and available in the command line.

## Initial Git Configuration
Git attaches your name and email to every commit. This identifies who made the change.

```bash
git config --global user.name "Your Name"
```
Explanation (word by word):
- `git` runs the Git program.
- `config` changes Git settings.
- `--global` means “apply this setting for all your repositories on this computer.”
- `user.name` is the setting for your display name.
- `"Your Name"` is the value you want Git to store.
Why this is used:
- Commits need an author name so you and others know who made each change.

```bash
git config --global user.email "you@example.com"
```
Explanation (word by word):
- `git` runs the Git program.
- `config` changes Git settings.
- `--global` means “apply this setting for all your repositories on this computer.”
- `user.email` is the setting for your email address.
- `"you@example.com"` is the value you want Git to store.
Why this is used:
- Commits need an email to uniquely identify the author.

## Creating a Repository
You must create a repository before Git can track files in a folder.

```bash
git init
```
Explanation:
- `git` runs the Git program.
- `init` creates a new Git repository in the current folder.
Why this is used:
- It starts tracking changes in the folder.

## Git File Lifecycle
Git tracks files in three main states:
- **Untracked**: Git sees the file but is not tracking it.
- **Staged**: The file is marked to be included in the next commit.
- **Committed**: The file’s changes are saved in Git history.

Commands below will move files between these states.

## Staging Files
Staging tells Git exactly which changes you want to save in the next commit.

```bash
git add file.txt
```
Explanation:
- `git` runs the Git program.
- `add` places changes into the staging area.
- `file.txt` is the file you want to stage.
Why this is used:
- It lets you choose specific files or changes to commit.

```bash
git add .
```
Explanation:
- `git` runs the Git program.
- `add` stages changes.
- `.` means “all files and folders in the current directory.”
Why this is used:
- It stages everything at once when you want to commit all changes.

## Committing Changes
A commit saves staged changes as a snapshot in history.

```bash
git commit -m "Describe your change"
```
Explanation:
- `git` runs the Git program.
- `commit` creates a new snapshot.
- `-m` means “use this message.”
- `"Describe your change"` is the commit message.
Why this is used:
- The message explains why the change was made.

## Connecting to GitHub
To send your local commits to GitHub, you must link your local repo to a remote repo.

```bash
git remote add origin https://github.com/USERNAME/REPO.git
```
Explanation:
- `git` runs the Git program.
- `remote` manages remote repositories.
- `add` adds a new remote.
- `origin` is the common name for the main remote.
- `https://github.com/USERNAME/REPO.git` is the GitHub repo URL.
Why this is used:
- It tells Git where to send and receive code online.

## Pushing Code
Pushing sends your commits from your computer to GitHub.

```bash
git push -u origin main
```
Explanation:
- `git` runs the Git program.
- `push` sends commits to a remote.
- `-u` sets the default remote and branch for future pushes.
- `origin` is the remote name.
- `main` is the branch to push.
Why this is used:
- It uploads your work so others can see it and so it is backed up online.

## Cloning Repositories
Cloning copies a remote repository to your computer.

```bash
git clone https://github.com/USERNAME/REPO.git
```
Explanation:
- `git` runs the Git program.
- `clone` downloads a full copy of a remote repo.
- `https://github.com/USERNAME/REPO.git` is the repo URL.
Why this is used:
- It gives you a local copy to work on.

## Pulling Updates
Pulling gets the latest changes from the remote repo.

```bash
git pull origin main
```
Explanation:
- `git` runs the Git program.
- `pull` fetches changes and merges them into your branch.
- `origin` is the remote name.
- `main` is the branch to pull from.
Why this is used:
- It keeps your local work up to date with the remote.

## Branching
Branches let you work on changes without affecting the main line of work.

```bash
git branch feature-login
```
Explanation:
- `git` runs the Git program.
- `branch` creates a new branch.
- `feature-login` is the new branch name.
Why this is used:
- It keeps new work separate until it is ready.

```bash
git switch feature-login
```
Explanation:
- `git` runs the Git program.
- `switch` moves you to another branch.
- `feature-login` is the branch name.
Why this is used:
- It lets you start working on that branch.

## Merging
Merging combines changes from one branch into another.

```bash
git switch main
```
Explanation:
- `git` runs the Git program.
- `switch` moves you to another branch.
- `main` is the branch you want to merge into.
Why this is used:
- You must be on the branch that will receive the changes.

```bash
git merge feature-login
```
Explanation:
- `git` runs the Git program.
- `merge` combines changes.
- `feature-login` is the branch being merged into `main`.
Why this is used:
- It brings completed work into the main branch.

## Forking & Open-Source Workflow
Forking is a GitHub feature. It creates your own copy of someone else’s repository under your account. You usually:
1. Fork the repo on GitHub.
2. Clone your fork to your computer.
3. Create a branch, make changes, commit, and push to your fork.
4. Open a pull request to the original repo.

```bash
git clone https://github.com/YOUR-USERNAME/REPO.git
```
Explanation:
- `git` runs the Git program.
- `clone` downloads your fork.
- `https://github.com/YOUR-USERNAME/REPO.git` is your fork URL.
Why this is used:
- You need a local copy to make changes.

## Pull Requests
A pull request (PR) asks the original repository to review and merge your changes.

```bash
git push -u origin feature-branch
```
Explanation:
- `git` runs the Git program.
- `push` sends your branch to GitHub.
- `-u` sets the default upstream for this branch.
- `origin` is your fork on GitHub.
- `feature-branch` is the branch name.
Why this is used:
- GitHub needs your branch online before you can open a PR.

## Undoing Mistakes
Mistakes happen. Git provides safe ways to undo changes.

```bash
git restore file.txt
```
Explanation:
- `git` runs the Git program.
- `restore` discards changes in your working directory.
- `file.txt` is the file to revert.
Why this is used:
- It undoes uncommitted changes when you want to start over.

```bash
git restore --staged file.txt
```
Explanation:
- `git` runs the Git program.
- `restore` changes where the file is tracked.
- `--staged` removes the file from the staging area.
- `file.txt` is the file to unstage.
Why this is used:
- It keeps your edits but removes them from the next commit.

```bash
git revert HEAD
```
Explanation:
- `git` runs the Git program.
- `revert` creates a new commit that undoes a previous commit.
- `HEAD` means “the latest commit.”
Why this is used:
- It is a safe way to undo a commit while keeping history intact.

## Viewing History
History shows what changed and who changed it.

```bash
git log
```
Explanation:
- `git` runs the Git program.
- `log` shows commit history.
Why this is used:
- It helps you review past changes and messages.

```bash
git log --oneline
```
Explanation:
- `git` runs the Git program.
- `log` shows commit history.
- `--oneline` compresses each commit into one line.
Why this is used:
- It gives a quick summary of history.

## .gitignore
`.gitignore` is a file that tells Git which files to ignore.

```bash
echo node_modules/ >> .gitignore
```
Explanation:
- `echo` outputs text.
- `node_modules/` is a folder you want Git to ignore.
- `>>` appends text to a file.
- `.gitignore` is the file Git reads for ignore rules.
Why this is used:
- It prevents large or private files from being tracked.

## Authentication (HTTPS vs SSH)
You must authenticate to push to GitHub.

HTTPS:
- Uses your GitHub username and a personal access token (not your password).
- Easier to set up for beginners.

SSH:
- Uses a key pair (public and private keys).
- More secure and avoids typing credentials often.

```bash
git remote -v
```
Explanation:
- `git` runs the Git program.
- `remote` manages remotes.
- `-v` shows the remote URLs.
Why this is used:
- It tells you whether your repo is using HTTPS or SSH.

## Common Errors & Fixes
Common problems and simple fixes:

```bash
git status
```
Explanation:
- `git` runs the Git program.
- `status` shows the current state of your files.
Why this is used:
- It helps you understand what Git thinks is happening.

- **Error: “fatal: not a git repository”**
	- Meaning: You ran a Git command outside a repo.
	- Fix: Run `git init` in the correct folder or move into a repo.

- **Error: “failed to push some refs”**
	- Meaning: Your local branch is behind the remote.
	- Fix: Run `git pull origin main`, resolve any conflicts, then push again.

- **Error: “authentication failed”**
	- Meaning: GitHub rejected your credentials.
	- Fix: Use a personal access token for HTTPS or set up SSH keys.

## Best Practices
- Commit small, focused changes.
- Write clear commit messages.
- Pull before you start working.
- Use branches for new features or fixes.
- Do not commit secrets (passwords, keys).

## Daily Git Workflow
This is a common, safe workflow for everyday work.

```bash
git status
```
Explanation:
- `git` runs the Git program.
- `status` shows what has changed.
Why this is used:
- It helps you decide what to stage and commit.

```bash
git pull origin main
```
Explanation:
- `git` runs the Git program.
- `pull` gets the latest changes.
- `origin` is the remote name.
- `main` is the branch you are updating.
Why this is used:
- It avoids conflicts by starting with the latest code.

```bash
git add .
```
Explanation:
- `git` runs the Git program.
- `add` stages changes.
- `.` means “all changes in this folder.”
Why this is used:
- It prepares your work to be saved in a commit.

```bash
git commit -m "Short, clear message"
```
Explanation:
- `git` runs the Git program.
- `commit` saves your changes.
- `-m` adds a message.
- `"Short, clear message"` describes the change.
Why this is used:
- It creates a clear record of what you did and why.

```bash
git push
```
Explanation:
- `git` runs the Git program.
- `push` sends your commits to GitHub.
Why this is used:
- It backs up your work and shares it with others.

## Conclusion
You now have the basics to create, track, and share projects with Git and GitHub. Keep practicing with small projects to build confidence and avoid mistakes.

---

# Git & GitHub — Complete Practical Guide

Beginner-friendly, step-by-step notes for learning Git (a version control tool) and GitHub (a website for hosting Git repositories).

## Table of Contents

1. [Introduction](#1-introduction)
	- [Quick Start (5 Steps)](#11-quick-start-5-steps)
2. [What is Git](#2-what-is-git)
3. [What is GitHub](#3-what-is-github)
4. [Core Terminology](#4-core-terminology)
   - [Emoji Quick Table](#41-emoji-quick-table)
5. [Installing Git (Windows)](#5-installing-git-windows)
6. [Initial Git Configuration](#6-initial-git-configuration)
7. [Creating a Repository](#7-creating-a-repository)
8. [Git File Lifecycle](#8-git-file-lifecycle)
9. [Staging Files](#9-staging-files)
10. [Committing Changes](#10-committing-changes)
11. [Connecting to GitHub](#11-connecting-to-github)
12. [Pushing Code](#12-pushing-code)
13. [Cloning Repositories](#13-cloning-repositories)
14. [Pulling Updates](#14-pulling-updates)
15. [Branching](#15-branching)
16. [Merging](#16-merging)
17. [Forking & Open-Source Workflow](#17-forking--open-source-workflow)
18. [Pull Requests](#18-pull-requests)
19. [Undoing Mistakes](#19-undoing-mistakes)
20. [Viewing History](#20-viewing-history)
21. [.gitignore](#21-gitignore)
22. [Authentication (HTTPS vs SSH)](#22-authentication-https-vs-ssh)
23. [Common Errors & Fixes](#23-common-errors--fixes)
24. [Best Practices](#24-best-practices)
25. [Daily Git Workflow](#25-daily-git-workflow)
26. [Conclusion](#26-conclusion)

---

## Chapter Navigation
| # | Emoji | Chapter | Link |
| --- | --- | --- | --- |
| 1 | 👋 | Introduction | [Go](#1-introduction) |
| 1.1 | 🚀 | Quick Start (5 Steps) | [Go](#11-quick-start-5-steps) |
| 2 | 🧠 | What is Git | [Go](#2-what-is-git) |
| 3 | 🌐 | What is GitHub | [Go](#3-what-is-github) |
| 4 | 🧩 | Core Terminology | [Go](#4-core-terminology) |
| 4.1 | 😀 | Emoji Quick Table | [Go](#41-emoji-quick-table) |
| 5 | 🧰 | Installing Git (Windows) | [Go](#5-installing-git-windows) |
| 6 | ⚙️ | Initial Git Configuration | [Go](#6-initial-git-configuration) |
| 7 | 📁 | Creating a Repository | [Go](#7-creating-a-repository) |
| 8 | ♻️ | Git File Lifecycle | [Go](#8-git-file-lifecycle) |
| 9 | ✅ | Staging Files | [Go](#9-staging-files) |
| 10 | 📝 | Committing Changes | [Go](#10-committing-changes) |
| 11 | 🔗 | Connecting to GitHub | [Go](#11-connecting-to-github) |
| 12 | ⬆️ | Pushing Code | [Go](#12-pushing-code) |
| 13 | 📥 | Cloning Repositories | [Go](#13-cloning-repositories) |
| 14 | ⬇️ | Pulling Updates | [Go](#14-pulling-updates) |
| 15 | 🌿 | Branching | [Go](#15-branching) |
| 16 | 🤝 | Merging | [Go](#16-merging) |
| 17 | 🍴 | Forking & Open-Source Workflow | [Go](#17-forking--open-source-workflow) |
| 18 | 📬 | Pull Requests | [Go](#18-pull-requests) |
| 19 | 🧹 | Undoing Mistakes | [Go](#19-undoing-mistakes) |
| 20 | 🧭 | Viewing History | [Go](#20-viewing-history) |
| 21 | 🚫 | .gitignore | [Go](#21-gitignore) |
| 22 | 🔐 | Authentication (HTTPS vs SSH) | [Go](#22-authentication-https-vs-ssh) |
| 23 | 🧯 | Common Errors & Fixes | [Go](#23-common-errors--fixes) |
| 24 | ⭐ | Best Practices | [Go](#24-best-practices) |
| 25 | 🗓️ | Daily Git Workflow | [Go](#25-daily-git-workflow) |
| 26 | ✅ | Conclusion | [Go](#26-conclusion) |

---

## 1. Introduction

This guide teaches:

- What Git and GitHub are (from zero knowledge)
- The most common Git commands
- Why you use each command (not only how)

### What you need

- A Windows PC
- Internet access (for GitHub parts)
- Basic ability to open an app and copy/paste commands

## 1.1 Quick Start (5 Steps)
| Step | Emoji | Command | Why |
| --- | --- | --- | --- |
| 1 | 📁 | `git init` | Start tracking a folder. |
| 2 | 🧪 | `git status` | Check what changed. |
| 3 | ✅ | `git add .` | Stage all changes. |
| 4 | 📝 | `git commit -m "Message"` | Save a snapshot. |
| 5 | ⬆️ | `git push origin main` | Back up to GitHub. |

### Important idea (before commands)

Git works in a folder on your computer.

- You edit files normally.
- Git can **save snapshots** of your work called **commits**.
- Those commits form a **history** you can review and return to.

GitHub is optional for local work, but it is very useful for:

- Backup online
- Sharing code
- Collaborating with others

---

## 2. What is Git

**Git** is a **version control system**.

Version control means:

- Git tracks changes to files over time.
- You can save work in small steps.
- You can compare versions and undo mistakes.
- You can work on different features in parallel using branches.

Git runs on your computer. You can use it without the internet.

---

## 3. What is GitHub

**GitHub** is a website that stores Git repositories online.

GitHub is used for:

- Hosting repositories (a repo is a project folder tracked by Git)
- Collaboration (issues, pull requests, reviews)
- Sharing and discovering open-source projects

GitHub is not Git.

- Git = the tool
- GitHub = a service that hosts Git repositories

---

## 4. Core Terminology

| Term | Emoji | Simple meaning | Why it matters |
| --- | --- | --- | --- |
| Version control | 🕒 | A system that tracks changes over time | Lets you save history and undo mistakes |
| Repository (repo) | 📦 | A project folder tracked by Git | The basic unit Git works with |
| Commit | 📝 | A saved snapshot of changes | Creates a reliable history |
| Working directory | 🗂️ | Your normal files on disk | Where you edit files |
| Staging area (index) | ✅ | A “prep” area for the next commit | Lets you choose what goes into a commit |
| Branch | 🌿 | A separate line of work | Develop features without breaking main work |
| Merge | 🤝 | Combine changes from branches | Brings feature work back together |
| Remote | 🌐 | A repository stored elsewhere (often GitHub) | Enables sharing and backup |
| Origin | 🏷️ | The common default name of a remote | A convenient label for the remote URL |
| Clone | 📥 | A full copy of a remote repo | Gets a project onto your computer |
| Pull | ⬇️ | Download + merge remote changes | Keeps your local work up to date |
| Push | ⬆️ | Upload your commits to a remote | Shares your work |
| Fork | 🍴 | Your own copy of someone else’s repo on GitHub | Used in open-source workflows |
| Pull Request (PR) | 📬 | A request to merge changes on GitHub | Enables review and collaboration |

## 4.1 Emoji Quick Table
Use this emoji cheat sheet to remember common Git actions at a glance.

| Emoji | Meaning | Command Example |
| --- | --- | --- |
| 🌱 | Start a repo | `git init` |
| 🧪 | Check status | `git status` |
| ✅ | Stage changes | `git add .` |
| 📝 | Save a snapshot | `git commit -m "Message"` |
| 🌿 | Create a branch | `git branch feature-x` |
| 🔀 | Switch branch | `git switch feature-x` |
| 🤝 | Merge work | `git merge feature-x` |
| ⬆️ | Push to remote | `git push origin main` |
| ⬇️ | Pull updates | `git pull origin main` |
| 🧭 | View history | `git log --oneline` |
| 🧹 | Undo local changes | `git restore file.txt` |
| 🔒 | Ignore files | `.gitignore` |
| 🔑 | Authenticate | HTTPS or SSH |
| 📦 | Stash work | `git stash` |
| 🏷️ | Tag a release | `git tag v1.0.0` |
| 🔁 | Rebase branch | `git rebase main` |
| 🧯 | Reset changes | `git reset --soft HEAD~1` |
| 🔍 | Compare changes | `git diff` |
| 🛰️ | Fetch remotes | `git fetch` |

---

## 5. Installing Git (Windows)

### Step-by-step

1. Download Git for Windows from: https://git-scm.com/download/win
2. Run the installer.
3. Accept defaults if unsure.

### Verify the installation

```bash
git --version
```

Explanation (line-by-line meaning):

- `git` = runs the Git program.
- `--version` = asks Git to print its installed version.

Why you use it:

- Confirms Git is installed and available in your terminal.

---

## 6. Initial Git Configuration

Git adds your name and email to commits. This helps identify who made a change.

### Set your name

```bash
git config --global user.name "Your Name"
```

Explanation (word-by-word):

- `git` = run Git.
- `config` = change Git settings.
- `--global` = apply this setting to **all** repositories for your user account on this computer.
- `user.name` = the setting key for your display name.
- `"Your Name"` = the value you are setting (use your real name or a consistent name).

Why you use it:

- Your commits will show who created them. Teams need this.

### Set your email

```bash
git config --global user.email "you@example.com"
```

Explanation (word-by-word):

- `git` = run Git.
- `config` = change Git settings.
- `--global` = apply this setting to all repositories for your user account.
- `user.email` = the setting key for your email address.
- `"you@example.com"` = the value you are setting.

Why you use it:

- Git records an email in each commit. GitHub uses it to link commits to your account (if it matches).

### Check your settings

```bash
git config --global --list
```

Explanation:

- `--list` = shows current configuration values.

Why you use it:

- Confirms your name and email are set correctly.

---

## 7. Creating a Repository

You usually start a repo in an existing project folder.

### Create a new folder (optional)

```bash
mkdir my-project
cd my-project
```

Explanation:

- `mkdir my-project` = creates a folder named `my-project`.
- `cd my-project` = moves into that folder.

Why you use it:

- Git repositories live inside a folder.

### Initialize Git in the folder

```bash
git init
```

Explanation:

- `init` = initialize a new, empty Git repository in the current folder.

Why you use it:

- Tells Git: “Start tracking changes in this folder.”

### Check repository status

```bash
git status
```

Explanation:

- `status` = shows what Git currently sees (changed files, staged files, and branch info).

Why you use it:

- It is the safest command for beginners. Use it often to understand what’s happening.

---

## 8. Git File Lifecycle

A file usually moves through these states:

1. **Untracked**: Git sees the file, but is not tracking it yet.
2. **Modified**: The file is tracked, and you changed it.
3. **Staged**: You selected the change to be included in the next commit.
4. **Committed**: The change is saved in Git history.

Why this matters:

- Git does not automatically commit everything you change.
- The staging area gives you control over what is saved.

---

## 9. Staging Files

Staging means: “Choose what will go into the next commit.”

### Stage one file

```bash
git add README.md
```

Explanation:

- `add` = put changes into the staging area.
- `README.md` = the file you want to stage.

Why you use it:

- Lets you commit only the changes you intend to commit.

### Stage everything in the current folder

```bash
git add .
```

Explanation:

- `.` = “the current directory.”
- This stages all new/changed files under the current folder (except ignored files).

Why you use it:

- Quick way to stage multiple changes at once.

### Unstage a file (keep the file changes)

```bash
git restore --staged README.md
```

Explanation:

- `restore` = restore files to a previous state.
- `--staged` = operate on the staging area (not your working files).
- `README.md` = the file to remove from staging.

Why you use it:

- Fixes accidental staging without losing your edits.

---

## 10. Committing Changes

A commit is a saved snapshot of staged changes.

### Commit staged changes

```bash
git commit -m "Add initial README"
```

Explanation:

- `commit` = create a new snapshot in history.
- `-m` = provide a message right in the command.
- `"Add initial README"` = the commit message (describe what changed and why).

Why you use it:

- Creates a clear, recoverable history of your work.

### Stage and commit tracked files in one step (use carefully)

```bash
git commit -am "Fix typo"
```

Explanation:

- `-a` = automatically stage changes to **tracked** files (it will not add new untracked files).
- `-m` = set the message.

Why you use it:

- Faster for small edits when you are sure what you changed.

---

## 11. Connecting to GitHub

To connect your local repository to GitHub, you create a repository on GitHub, then add it as a remote.

### Create an empty repository on GitHub

On GitHub:

- Click **New repository**
- Choose a name
- Create it (do not add files if your local repo already has commits)

### Add the GitHub repo as a remote

```bash
git remote add origin https://github.com/USERNAME/REPO.git
```

Explanation:

- `remote` = manage remote connections.
- `add` = create a new remote entry.
- `origin` = the remote name (a common default).
- `https://...` = the remote repository URL.

Why you use it:

- It gives your local repo a “destination” for pushing and a “source” for pulling.

### Confirm remotes

```bash
git remote -v
```

Explanation:

- `-v` = “verbose” output; shows URLs for fetch and push.

Why you use it:

- Confirms you connected to the correct GitHub repository.

---

## 12. Pushing Code

Pushing uploads your commits from your computer to GitHub.

### Push your current branch to GitHub (first push)

```bash
git push -u origin main
```

Explanation:

- `push` = send local commits to a remote.
- `-u` = set an “upstream” so future `git push` and `git pull` know where to go.
- `origin` = the remote name.
- `main` = the branch name.

Why you use it:

- Publishes your work to GitHub and sets up a default connection for that branch.

### Push after the first time

```bash
git push
```

Explanation:

- With an upstream set, Git already knows the remote and branch.

Why you use it:

- Fast upload of new commits.

---

## 13. Cloning Repositories

Cloning creates a full local copy of a repository.

### Clone from GitHub

```bash
git clone https://github.com/USERNAME/REPO.git
```

Explanation:

- `clone` = download the repository, including its full commit history.
- The URL = where to download from.

Why you use it:

- Gets an existing project onto your computer so you can work on it.

### Clone into a specific folder name

```bash
git clone https://github.com/USERNAME/REPO.git my-folder
```

Explanation:

- `my-folder` = the directory name to create.

Why you use it:

- Useful when you want a different local folder name.

---

## 14. Pulling Updates

Pulling brings changes from GitHub (remote) into your local branch.

### Pull latest changes

```bash
git pull
```

Explanation:

- `pull` = fetches remote commits and then merges them into your current branch.

Why you use it:

- Keeps your local work up to date with the remote.

### Fetch without merging (safer for learning)

```bash
git fetch
```

Explanation:

- `fetch` = downloads remote updates but does not change your working files.

Why you use it:

- Lets you review remote changes before you merge them.

---

## 15. Branching

A branch is a separate line of work.

Why branches are used:

- Work on a feature without breaking the main branch.
- Try ideas safely.
- Develop multiple features in parallel.

### List branches

```bash
git branch
```

Explanation:

- `branch` (no extra args) = lists local branches.

Why you use it:

- Helps you see what branches exist and which one you are on.

### Create a new branch

```bash
git branch feature-login
```

Explanation:

- `feature-login` = the new branch name.

Why you use it:

- Creates a separate workspace in history.

### Switch to a branch

```bash
git switch feature-login
```

Explanation:

- `switch` = move to another branch.

Why you use it:

- Starts working on that branch’s version of the files.

### Create and switch in one step

```bash
git switch -c feature-login
```

Explanation:

- `-c` = create the branch if it does not exist.

Why you use it:

- Faster when starting a new feature.

---

## 16. Merging

Merging combines changes from one branch into another.

### Merge a feature branch into your current branch

First, switch to the branch that will receive the changes (often `main`):

```bash
git switch main
```

Explanation:

- This makes `main` the current branch, so it will receive the merge.

Why you use it:

- You must be “standing on” the destination branch before merging.

Now merge:

```bash
git merge feature-login
```

Explanation:

- `merge` = combine histories.
- `feature-login` = the branch whose commits you want to bring in.

Why you use it:

- Integrates completed feature work back into the main line.

### If there is a merge conflict

Git may stop and say there is a conflict (two changes to the same lines).

What to do:

- Open the conflicted files.
- Choose the correct content.
- Remove conflict markers.
- Stage and commit the merge resolution.

Commands used during conflict resolution:

```bash
git status
git add .
git commit -m "Resolve merge conflict"
```

Explanation:

- `git status` = tells you which files are conflicted.
- `git add .` = stages the resolved files.
- `git commit ...` = records the resolution.

Why you use them:

- Git needs a commit to finish the merge once conflicts are resolved.

---

## 17. Forking & Open-Source Workflow

Forking is a GitHub feature.

What it means:

- A **fork** is your own copy of someone else’s repository on GitHub.
- You can make changes in your fork without affecting the original project.

Why it’s used:

- In open-source, you usually do not have permission to push directly to the original repo.

Typical workflow:

1. Fork the original repo on GitHub.
2. Clone your fork to your computer.
3. Create a branch for your change.
4. Push the branch to your fork.
5. Open a Pull Request to the original repo.

---

## 18. Pull Requests

A Pull Request (PR) is a GitHub feature that proposes changes.

What a PR does:

- Shows your changes (diff)
- Allows discussion and review
- Lets maintainers merge your work

How you usually create a PR:

1. Push a branch to GitHub.
2. On GitHub, click **Compare & pull request**.
3. Write a clear title and description.
4. Submit.

Why you use PRs:

- They provide a safe review process before changes are merged.

---

## 19. Undoing Mistakes

Undoing depends on what you want to undo (and whether it is committed).

### Discard changes in a file (not staged)

```bash
git restore README.md
```

Explanation:

- `restore` = replace your working file with the last committed version.
- `README.md` = file to discard changes in.

Why you use it:

- Removes local edits you do not want.

### Unstage a staged file (keep your edits)

```bash
git restore --staged README.md
```

Explanation:

- Removes the file from the staging area but keeps your changes in the working directory.

Why you use it:

- Fixes accidental staging.

### Change the last commit message (only if not pushed)

```bash
git commit --amend -m "New message"
```

Explanation:

- `--amend` = modify the most recent commit.
- `-m` = set the new message.

Why you use it:

- Corrects mistakes in the latest commit without creating a new commit.

### Revert a commit (safe for shared history)

```bash
git revert COMMIT_HASH
```

Explanation:

- `revert` = creates a new commit that undoes the changes from an older commit.
- `COMMIT_HASH` = the identifier of the commit you want to undo.

Why you use it:

- Safe when others may already have pulled the history (it does not rewrite history).

### Reset (rewrites history; use carefully)

```bash
git reset --hard COMMIT_HASH
```

Explanation:

- `reset` = move the current branch pointer.
- `--hard` = also changes your working files to match.
- `COMMIT_HASH` = where you want to go back to.

Why you use it:

- Removes commits locally. Avoid on branches that are already pushed/shared.

---

## 20. Viewing History

History helps you understand what changed, when, and why.

### View commit history

```bash
git log
```

Explanation:

- `log` = shows commits, newest first.

Why you use it:

- Find commit hashes and read commit messages.

### Compact history view

```bash
git log --oneline
```

Explanation:

- `--oneline` = shows each commit in one line.

Why you use it:

- Faster scanning.

### Show what changed in the working directory

```bash
git diff
```

Explanation:

- `diff` = shows differences not yet staged.

Why you use it:

- Review your edits before staging.

### Show what is staged

```bash
git diff --staged
```

Explanation:

- `--staged` = compare staged changes against the last commit.

Why you use it:

- Review exactly what will be committed.

---

## 21. .gitignore

`.gitignore` tells Git which files to ignore.

Why you need it:

- Prevent committing secrets (passwords, API keys)
- Avoid committing generated files (build output)
- Keep the repo clean

### Create a `.gitignore`

Create a file named `.gitignore` in the repository root.

Example:

```bash
# Node
node_modules/

# Logs
*.log

# Environment variables (often contains secrets)
.env

# OS files
Thumbs.db
Desktop.ini
```

Explanation:

- Each line is a pattern Git should ignore.
- `folder/` ignores a folder.
- `*.log` ignores all `.log` files.

Why you use it:

- Stops accidental commits of unwanted files.

---

## 22. Authentication (HTTPS vs SSH)

Authentication is how Git proves you are allowed to push/pull.

### HTTPS

What it is:

- Remote URL starts with `https://...`
- Usually uses a browser login or a GitHub token

Why beginners use it:

- Easy to start

### SSH

What it is:

- Remote URL looks like `git@github.com:USERNAME/REPO.git`
- Uses SSH keys (a public/private key pair)

Why people use it:

- Convenient after setup
- No repeated login prompts

### Check what URL you are using

```bash
git remote -v
```

Explanation:

- Shows whether your remote uses HTTPS or SSH.

Why you use it:

- Helps troubleshoot authentication problems.

---

## 23. Common Errors & Fixes

### Error: “not a git repository”

Meaning:

- You ran a Git command in a folder that is not initialized as a repo.

Fix:

```bash
git init
```

Explanation:

- Initializes Git in the current folder.

Why you use it:

- Git needs a `.git` directory to track history.

### Error: “nothing to commit, working tree clean”

Meaning:

- There are no new changes to commit.

Fix:

```bash
git status
```

Explanation:

- Shows whether you changed files, staged files, or have untracked files.

Why you use it:

- Helps you understand what Git is waiting for.

### Error: “failed to push some refs”

Common meaning:

- The remote has commits you do not have locally.

Fix (safe approach):

```bash
git pull --rebase
git push
```

Explanation:

- `pull --rebase` = download remote commits and replay your local commits on top.
- `push` = try again.

Why you use it:

- Keeps history cleaner and resolves “behind” situations.

### Error: merge conflict

Meaning:

- Git cannot automatically combine changes.

Fix:

```bash
git status
```

Explanation:

- Identifies conflicted files.

Why you use it:

- You need to resolve conflicts manually before completing the merge.

---

## 24. Best Practices

- Commit small, logical changes.
- Write clear commit messages that explain **why**.
- Use branches for features and fixes.
- Pull before you start work if collaborating.
- Do not commit secrets (use `.gitignore`).
- Run `git status` often.

---

## 25. Daily Git Workflow

This is a simple, repeatable routine.

### 1) Get the latest changes (if working with a remote)

```bash
git pull
```

Explanation:

- Updates your current branch from the remote.

Why you use it:

- Reduces conflicts by starting from the latest version.

### 2) Create a new branch for your work

```bash
git switch -c my-change
```

Explanation:

- Creates and switches to a branch named `my-change`.

Why you use it:

- Keeps your work isolated and easier to review.

### 3) Make changes, then review

```bash
git status
git diff
```

Explanation:

- `git status` = shows what changed.
- `git diff` = shows the exact edits.

Why you use it:

- Helps you confirm what you are about to save.

### 4) Stage changes

```bash
git add .
```

Explanation:

- Stages all intended changes.

Why you use it:

- Selects what goes into the commit.

### 5) Commit

```bash
git commit -m "Describe what and why"
```

Explanation:

- Records a snapshot with a message.

Why you use it:

- Creates a checkpoint you can return to.

### 6) Push your branch

```bash
git push -u origin my-change
```

Explanation:

- Uploads your branch and sets upstream.

Why you use it:

- Backs up work and prepares for a Pull Request.

---

## 26. Conclusion

You now have the basics:

- What Git is (local version control)
- What GitHub is (remote hosting and collaboration)
- How to stage, commit, push, pull, branch, and merge

Next step:

- Practice in a small test repository until each command feels predictable.
