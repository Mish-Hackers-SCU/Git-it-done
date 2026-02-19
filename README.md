# Git-it-done 🚀

![msh_hackers_img](msh_icon.png)

---

## 📚 Table of Contents
1. [Setup & Configuration](#-setup--configuration)
2. [Creating Repositories](#-creating-repositories)
3. [Staging & Committing](#-staging--committing)
4. [Branching](#-branching)
5. [Merging & Rebasing](#-merging--rebasing)
6. [Remote Repositories](#-remote-repositories)
7. [Fetching, Pulling & Pushing](#-fetching-pulling--pushing)
8. [Undoing Changes](#-undoing-changes)
9. [Stashing](#-stashing)
10. [Tagging](#-tagging)
11. [Inspecting & Logging](#-inspecting--logging)
12. [GitHub Learning Resources](#-github-learning-resources)

---

## ⚙️ Setup & Configuration

```bash
# Set your name and email (used in commits)
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

# Set the default branch name to 'main'
git config --global init.defaultBranch main

# Set your preferred editor (e.g., VS Code)
git config --global core.editor "code --wait"

# View all configuration settings
git config --list

# View a specific setting
git config user.name
```

---

## 📁 Creating Repositories

```bash
# Initialize a new local repository
git init

# Clone an existing remote repository
git clone https://github.com/user/repo.git

# Clone into a specific folder name
git clone https://github.com/user/repo.git my-folder
```

---

## 📝 Staging & Committing

```bash
# Check the status of your working directory
git status

# Stage a specific file
git add filename.txt

# Stage all changes in the current directory
git add .

# Stage parts of a file interactively
git add -p filename.txt

# Commit staged changes with a message
git commit -m "Your commit message"

# Stage all tracked files and commit in one step
git commit -am "Your commit message"

# Amend the last commit (message or content)
git commit --amend -m "Updated commit message"
```

---

## 🌿 Branching

```bash
# List all local branches (* marks the active branch)
git branch

# List all branches including remote
git branch -a

# Create a new branch
git branch feature/my-feature

# Switch to an existing branch
git checkout feature/my-feature
# Or (modern syntax)
git switch feature/my-feature

# Create and switch to a new branch
git checkout -b feature/my-feature
# Or (modern syntax)
git switch -c feature/my-feature

# Rename a branch
git branch -m old-name new-name

# Delete a branch (safe — only if merged)
git branch -d feature/my-feature

# Force-delete a branch
git branch -D feature/my-feature
```

---

## 🔀 Merging & Rebasing

```bash
# Merge a branch into the current branch
git merge feature/my-feature

# Merge without fast-forward (preserves branch history)
git merge --no-ff feature/my-feature

# Abort a merge in progress
git merge --abort

# Rebase current branch onto another
git rebase main

# Abort a rebase in progress
git rebase --abort

# Continue after resolving conflicts during rebase
git rebase --continue
```

---

## 🌐 Remote Repositories

```bash
# View configured remote connections
git remote -v

# Add a new remote named 'origin'
git remote add origin https://github.com/user/repo.git

# Rename a remote
git remote rename origin upstream

# Remove a remote
git remote remove origin

# Change the URL of an existing remote
git remote set-url origin https://github.com/user/new-repo.git
```

---

## 📡 Fetching, Pulling & Pushing

```bash
# Fetch updates from remote (does NOT merge)
git fetch origin

# Pull changes from remote and merge into current branch
git pull origin main

# Pull with rebase instead of merge
git pull --rebase origin main

# Push current branch to remote
git push origin main

# Push and set upstream tracking
git push -u origin feature/my-feature

# Push all branches
git push --all origin

# Delete a remote branch
git push origin --delete feature/my-feature

# Force push (use with caution!)
git push --force-with-lease origin feature/my-feature
```

---

## ↩️ Undoing Changes

```bash
# Discard changes in a file (restore to last commit)
git restore filename.txt
# Or (older syntax)
git checkout -- filename.txt

# Unstage a file (keep changes in working directory)
git restore --staged filename.txt
# Or (older syntax)
git reset HEAD filename.txt

# Undo the last commit but keep changes staged
git reset --soft HEAD~1

# Undo the last commit and unstage changes
git reset --mixed HEAD~1

# Undo the last commit and discard all changes (destructive!)
git reset --hard HEAD~1

# Create a new commit that reverses a previous commit (safe for shared history)
git revert <commit-hash>
```

---

## 🗄️ Stashing

```bash
# Stash uncommitted changes
git stash

# Stash with a descriptive message
git stash push -m "work in progress on feature X"

# List all stashes
git stash list

# Apply the most recent stash (keeps it in stash list)
git stash apply

# Apply a specific stash
git stash apply stash@{2}

# Apply and remove the most recent stash
git stash pop

# Delete a specific stash
git stash drop stash@{1}

# Delete all stashes
git stash clear
```

---

## 🏷️ Tagging

```bash
# List all tags
git tag

# Create a lightweight tag
git tag v1.0.0

# Create an annotated tag with a message
git tag -a v1.0.0 -m "Release version 1.0.0"

# Tag a specific commit
git tag -a v1.0.0 <commit-hash> -m "Release version 1.0.0"

# Push a specific tag to remote
git push origin v1.0.0

# Push all tags to remote
git push origin --tags

# Delete a local tag
git tag -d v1.0.0

# Delete a remote tag
git push origin --delete v1.0.0
```

---

## 🔍 Inspecting & Logging

```bash
# View the commit history
git log

# Compact one-line log
git log --oneline

# Visual branch graph
git log --oneline --graph --all

# Show changes introduced by each commit
git log -p

# Show stats (files changed, insertions, deletions)
git log --stat

# Show changes in the working directory vs staging
git diff

# Show changes between staging and last commit
git diff --staged

# Show changes between two commits
git diff <commit1> <commit2>

# Show details of a specific commit
git show <commit-hash>

# Search commit messages
git log --grep="search term"

# Find which commit introduced a line in a file
git blame filename.txt
```

---

## 🎓 GitHub Learning Resources

### Official GitHub Resources
| Resource | Description |
|---|---|
| [GitHub Skills](https://skills.github.com/) | Interactive, hands-on courses for learning GitHub directly in a repository |
| [GitHub Docs](https://docs.github.com/) | The official and comprehensive GitHub documentation |
| [GitHub Training Manual](https://githubtraining.github.io/training-manual/) | Open-source training manual used in GitHub workshops |
| [GitHub Git Cheat Sheet (PDF)](https://training.github.com/downloads/github-git-cheat-sheet.pdf) | Printable quick-reference card for Git commands |
| [GitHub Guides](https://guides.github.com/) | Short guides on GitHub workflows and features |
| [GitHub YouTube Channel](https://www.youtube.com/@GitHub) | Video tutorials, demos, and GitHub Universe talks |

### Learning Paths
| Resource | Description |
|---|---|
| [Hello World (GitHub Quickstart)](https://docs.github.com/en/get-started/quickstart/hello-world) | Beginner-friendly introduction to GitHub |
| [Introduction to Git](https://docs.github.com/en/get-started/using-git/about-git) | Understand the fundamentals of Git |
| [Git Handbook](https://guides.github.com/introduction/git-handbook/) | A concise overview of Git concepts |
| [Understanding the GitHub Flow](https://guides.github.com/introduction/flow/) | Learn the recommended GitHub collaboration workflow |
| [Mastering Markdown](https://guides.github.com/features/mastering-markdown/) | Write great README files and documentation |
| [Pro Git Book (free)](https://git-scm.com/book/en/v2) | The complete, in-depth reference book for Git (open source) |

### Practice & Community
| Resource | Description |
|---|---|
| [GitHub Explore](https://github.com/explore) | Discover trending repos and topics |
| [GitHub Community Discussions](https://github.com/orgs/community/discussions) | Ask questions and learn from the community |
| [GitHub Blog](https://github.blog/) | News, tips, and updates from the GitHub team |
| [Oh Shit, Git!?!](https://ohshitgit.com/) | Plain-English solutions for common Git mistakes |
| [Learn Git Branching](https://learngitbranching.js.org/) | Visual, interactive branching exercises |

---

## 💡 Tips & Best Practices

- **Write clear commit messages**: Use the imperative mood (e.g., "Add feature" not "Added feature").
- **Commit often**: Small, focused commits are easier to review and revert.
- **Use branches**: Keep `main`/`master` stable; develop features on separate branches.
- **Fetch before you push**: Use `git fetch` to review remote changes first, or `git pull --rebase` to avoid unnecessary merge commits when integrating upstream work.
- **Use `.gitignore`**: Keep secrets, build artifacts, and OS files out of your repository.
- **Review before committing**: Use `git diff --staged` to double-check what you're committing.
- **Never force-push to shared branches**: Use `--force-with-lease` at minimum, and avoid on `main`.

---

*Happy coding! 🎉 — Git-it-done*
