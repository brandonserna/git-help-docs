# Useful commands

```sh
# Status shows differences in files between the last commit and now.
git status

# Log
git log --oneline

# Remotes
git remote

# List remotes
git ls-remote --heads

# Ammend 
git commit --amend -m 'add new pages'

# Restore from changes 
git restore -- index.html

# Undo last commit
git reset --soft HEAD~1
git status

# Stash -- save inprogress work outside of commits
git stash
git stash list
git stash pop

# Blame 
#The output from a git blame command will show each line of a file as a row. From left to right, each row will include:
# A commit ID
# The name of the committer
# The timestamp of the change made
# The content of the line
git blame README.md

# Diff 
# Difference between current state and last commit.
git diff

# Checkout 
# A use of checkout can be restoring modified files to a previous state
git checkout -- index.html
git status

# Tag
git tag 0.1.0
git log --oneline

# Remove files
git rm [file]

# Delete branch
git branch -d NAME
```

