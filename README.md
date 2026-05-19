# Git Commands Reference 📋

A complete cheat sheet of Git commands needed while working on any project.

---

## ⚙️ Setup

| Command                                            | What it does                                                       |
| -------------------------------------------------- | ------------------------------------------------------------------ |
| `git config --global user.name "Your Name"`        | Set your global username                                           |
| `git config --global user.email "you@example.com"` | Set your global email                                              |
| `git config --list`                                | View all config settings                                           |
| `git init`                                         | Initialize a new local repository                                  |
| `git clone <url>`                                  | Clone a remote repo to your machine                                |
| `.gitignore`                                       | File listing paths git should not track (node_modules, .env, etc.) |

---

## 📝 Daily Basics

| Command                   | What it does                                             |
| ------------------------- | -------------------------------------------------------- |
| `git status`              | Show staged, unstaged, and untracked files               |
| `git add .`               | Stage all changes                                        |
| `git add <file>`          | Stage a specific file                                    |
| `git commit -m "message"` | Commit staged changes with a message                     |
| `git commit --amend`      | Edit the last commit message or add staged changes to it |
| `git diff`                | Show unstaged changes                                    |
| `git diff --staged`       | Show staged changes vs last commit                       |
| `git rm <file>`           | Remove a tracked file from the repo and staging          |
| `git mv <old> <new>`      | Rename or move a tracked file                            |

---

## 🌿 Branching

| Command                  | What it does                                    |
| ------------------------ | ----------------------------------------------- |
| `git branch`             | List all local branches                         |
| `git checkout -b <name>` | Create and switch to a new branch               |
| `git switch <name>`      | Switch to an existing branch                    |
| `git switch -c <name>`   | Create and switch to a new branch (modern way)  |
| `git merge <branch>`     | Merge a branch into the current branch          |
| `git rebase <branch>`    | Reapply your commits on top of another branch   |
| `git branch -d <name>`   | Delete a branch (safe — only if merged)         |
| `git branch -D <name>`   | Force-delete a branch regardless of merge state |

---

## ☁️ Remote

| Command                             | What it does                                   |
| ----------------------------------- | ---------------------------------------------- |
| `git remote add origin <url>`       | Add a remote connection (usually named origin) |
| `git remote -v`                     | List all remotes and their URLs                |
| `git push origin <branch>`          | Upload local commits to the remote branch      |
| `git push -u origin <branch>`       | Push and set upstream tracking for the branch  |
| `git pull origin <branch>`          | Fetch and merge changes from the remote        |
| `git fetch origin`                  | Download remote changes without merging        |
| `git push origin --delete <branch>` | Delete a branch on the remote                  |

---

## 🕐 History

| Command                           | What it does                               |
| --------------------------------- | ------------------------------------------ |
| `git log`                         | Show full commit history                   |
| `git log --oneline --graph --all` | Compact visual history with branch graph   |
| `git show <commit>`               | Show details and diff of a specific commit |
| `git blame <file>`                | See who last changed each line of a file   |
| `git log --author="Name"`         | Filter commit history by a specific author |
| `git shortlog -s -n`              | Count and rank commits per contributor     |

---

## ↩️ Undo / Fix

| Command                       | What it does                                         |
| ----------------------------- | ---------------------------------------------------- |
| `git restore <file>`          | Discard unstaged changes in a file                   |
| `git restore --staged <file>` | Unstage a file while keeping changes                 |
| `git reset --soft HEAD~1`     | Undo last commit, keep changes staged                |
| `git reset HEAD~1`            | Undo last commit, keep changes unstaged              |
| `git reset --hard HEAD~1`     | Undo last commit and discard ALL changes permanently |
| `git revert <commit>`         | Create a new commit that undoes a past commit        |
| `git clean -fd`               | Remove all untracked files and directories           |

---

## 📦 Stash

| Command                     | What it does                                 |
| --------------------------- | -------------------------------------------- |
| `git stash`                 | Temporarily save uncommitted work to a stack |
| `git stash push -m "label"` | Stash with a descriptive label               |
| `git stash list`            | List all stashed entries                     |
| `git stash pop`             | Apply the most recent stash and remove it    |
| `git stash apply stash@{1}` | Apply a specific stash without removing it   |
| `git stash drop stash@{0}`  | Delete a specific stash entry                |

---

## 🤝 Collaboration

| Command                         | What it does                                          |
| ------------------------------- | ----------------------------------------------------- |
| `git cherry-pick <commit>`      | Apply a specific commit from another branch           |
| `git merge --squash <branch>`   | Squash all branch commits into one before merging     |
| `git rebase -i HEAD~3`          | Interactively squash, reorder, or edit recent commits |
| `git bisect start / bad / good` | Binary search through history to find a bug           |

---

## 🏷️ Tags

| Command                             | What it does                                   |
| ----------------------------------- | ---------------------------------------------- |
| `git tag`                           | List all tags in the repository                |
| `git tag v1.0`                      | Create a lightweight tag at the current commit |
| `git tag -a v1.0 -m "Release v1.0"` | Create an annotated tag with a message         |
| `git push origin --tags`            | Push all local tags to the remote              |
| `git tag -d v1.0`                   | Delete a local tag                             |

---

## 🚀 Advanced

| Command                                       | What it does                                                 |
| --------------------------------------------- | ------------------------------------------------------------ |
| `git reflog`                                  | View full history of all HEAD movements — great for recovery |
| `git worktree add ../hotfix hotfix/bug`       | Work on two branches simultaneously in separate folders      |
| `git submodule add <url>`                     | Add a nested repository as a submodule                       |
| `git archive --format=zip HEAD > release.zip` | Export a snapshot of the repo as a zip file                  |

---

## 💡 Pro Tips

- **Commit often** with clear messages — use prefixes like `feat:`, `fix:`, `chore:`, `docs:`
- **Always branch** before starting a feature — never commit directly to `main`
- **Use `git stash`** when switching context mid-work without committing
- **Use `git log --oneline --graph`** constantly to stay oriented
- **Never `git reset --hard`** on shared/remote branches — use `git revert` instead
- **Pull before you push** to avoid unnecessary merge conflicts
- **Write your `.gitignore` first** before the initial commit

---

_Generated with ❤️ — Happy coding!_
