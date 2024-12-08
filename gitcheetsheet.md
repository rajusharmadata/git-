# Git Cheatsheet 🚀

## Basic Configuration

```bash
# Set up global user name and email
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Check current configuration
git config --list
```

## Repository Initialization

```bash
# Create a new repository
git init

# Clone an existing repository
git clone [repository-url]
git clone [repository-url] [directory-name]
```

## Basic Workflow

### Checking Status

```bash
# Show status of working directory
git status

# Show brief status
git status -s
```

### Adding Changes

```bash
# Add specific file
git add [filename]

# Add all changes
git add .

# Add all modified files (excluding new files)
git add -u

# Interactive staging
git add -p
```

### Committing Changes

```bash
# Commit with message
git commit -m "Commit message"

# Commit all modified files
git commit -am "Commit message"

# Amend last commit (modify most recent commit)
git commit --amend

# Amend commit without changing message
git commit --amend --no-edit
```

## Branching

```bash
# List branches
git branch

# Create new branch
git branch [branch-name]

# Switch to branch
git checkout [branch-name]

# Create and switch to new branch
git checkout -b [branch-name]

# Delete a branch
git branch -d [branch-name]

# Force delete a branch
git branch -D [branch-name]

# Rename current branch
git branch -m [new-branch-name]
```

## Merging and Rebasing

```bash
# Merge branch into current branch
git merge [branch-name]

# Rebase current branch onto another branch
git rebase [branch-name]

# Interactive rebase
git rebase -i [commit-hash]
```

## Remote Repositories

```bash
# Add remote repository
git remote add origin [repository-url]

# List remote repositories
git remote -v

# Push changes to remote repository
git push origin [branch-name]

# Pull changes from remote repository
git pull origin [branch-name]

# Fetch changes without merging
git fetch origin
```

## Viewing Changes

```bash
# Show differences
git diff

# Show differences staged for commit
git diff --staged

# Show commit history
git log

# Show compact log with one line per commit
git log --oneline

# Show branches and their commits
git log --graph --oneline --all
```

## Undoing Changes

```bash
# Unstage a file
git reset [filename]

# Discard local changes
git checkout -- [filename]

# Revert a commit
git revert [commit-hash]

# Reset to a previous commit
git reset [commit-hash]

# Hard reset (discard all local changes)
git reset --hard [commit-hash]
```

## Stashing

```bash
# Stash current changes
git stash

# List all stashes
git stash list

# Apply most recent stash
git stash apply

# Apply specific stash
git stash apply stash@{n}

# Pop (apply and remove) latest stash
git stash pop

# Clear all stashes
git stash clear
```

## Advanced Operations

```bash
# Find commits by search term
git log -S "search term"

# Cherry-pick a commit
git cherry-pick [commit-hash]

# Create annotated tag
git tag -a v1.0 -m "Version 1.0"

# Push tags to remote
git push --tags
```

## Ignore Files

```bash
# Create .gitignore file in project root
# Example contents:
# node_modules/
# *.log
# .env
```

## Troubleshooting

```bash
# Check Git version
git --version

# Get help for a command
git help [command]
```

## Best Practices

- Commit often
- Write clear, descriptive commit messages
- Use feature branches
- Pull before pushing
- Never force push to shared branches

## Common Workflows

1. Feature Branch Workflow
2. Gitflow Workflow
3. Forking Workflow

## Tips

- Use meaningful branch names
- Keep commits atomic (one purpose per commit)
- Use `.gitignore` to prevent unnecessary files from being tracked
