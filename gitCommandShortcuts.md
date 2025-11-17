# Useful-git-commands

---

# 🚀 **TOP 40 Most Useful Git Commands & Shortcuts**

*(Categorized so you don’t lose your mind.)*

---

# 🟩 **1. Essential Everyday Commands**

```
git status                  # See what's happening
git add .                   # Stage everything
git commit -m "msg"         # Commit
git push                    # Push to remote
git pull                    # Fetch + merge (default)
git pull --rebase           # Safer, cleaner pull
git log --oneline           # Clean commit history
```

---

# 🟦 **2. Branching & Switching**

```
git branch                  # List branches
git branch feature          # Create branch
git switch feature          # Switch branches
git switch -c feature       # Create + switch
git checkout <file>         # Restore a file
git branch -d feature       # Delete local branch
git push origin --delete feature   # Delete remote branch
```

---

# 🟨 **3. Merging & Rebasing**

```
git merge feature           # Merge feature → main
git rebase main             # Rebase feature ON main
git rebase --continue       # After fixing conflicts
git rebase --abort          # Panic button
```

---

# 🟥 **4. Undoing Mistakes (the lifesaver section)**

```
git reset HEAD~1            # Undo last commit (keep changes)
git reset --hard HEAD~1     # Undo last commit AND delete changes
git restore <file>          # Undo changes in file
git restore .               # Undo changes in entire folder
git revert <commit>         # Undo by creating a new reverse commit
```

---

# 🟧 **5. Stashing (when your workspace is messy but you need to switch branches)**

```
git stash                   # Stash dirty work
git stash pop               # Restore stashed work
git stash list              # View stashes
git stash clear             # Remove all stashes
```

---

# 🟪 **6. Shortcuts & Power Moves**

```
git log --oneline --graph --all
git diff                    # See unstaged changes
git diff --staged           # See staged changes
git add -p                  # Add changes chunk by chunk
git commit --amend          # Fix commit message or add forgotten file
git push --force-with-lease # Safe force push after rebase
```

---

# 🟫 **7. Cloning, Remotes & Updates**

```
git clone <url>             # Clone project
git remote -v               # Show remotes
git fetch                   # Download branches without merging
git fetch --all             # Fetch everything
git pull origin main        # Pull specific branch
```

---

# 🟩 **8. Tagging & Releases**

```
git tag                     # List tags
git tag v1.0                # Create tag
git push --tags             # Push tags
```

---

# ⚡ **Ultra-Power Git Aliases (Save HOURS)**

Put these in your `~/.gitconfig`:

```
[alias]
  s = status
  co = checkout
  br = branch
  cm = commit -m
  aa = add .
  lg = log --oneline --graph --decorate --all
  st = stash
  df = diff
```

Then you can do:

```
git s
git co feature
git lg
git aa && git cm "update"
```

Feels like VS Code autocomplete but inside your terminal.

---

# 🧠 **Top 10 Commands You’ll Actually Use Daily**

1. `git status`
2. `git add .`
3. `git commit -m ""`
4. `git push`
5. `git pull --rebase`
6. `git switch -c feature`
7. `git merge feature`
8. `git rebase main`
9. `git log --oneline`
10. `git reset HEAD~1` *(when you screw up)*

---

