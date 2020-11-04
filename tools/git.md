# Git

## Configuration
@tags: git configuration

```
# Set up user informations
git config --global user.name "constance"
git config --global user.email constance@gmail.com

# Activate git color
git config --global color.diff auto
git config --global color.status auto
git config --global color.branch auto
```

## First steps
@tags: git init diff show clone

```
# Clone a repository
$ git clone https://github.com/ConstanceBeguier/tensorflow-examples.git

# Show git history
$ git log [-p]

# Show one commit
$ git show fa3978

# Show diff between two commits
$ git diff fa3978 506715

# Create a git repository
$ git init
```

## Project status
@tags: git status checkout stash

```
# Project status
$ git status

# Remove uncommited changes on a file
$ git checkout file.go

# Stash the local changes
$ git stash

# Unstash the last stashed changes
$ git stash pop

# Show all stashed changes
$ git stash list

# Clear all stashed changes
$ git stash clear
```

## Contribute to a project
@tags: git pull push add commit revert reset

```
# Retrieve the last project commited version
$ git pull --rebase

# Create a local commit
$ git add -p
$ git add file.go
$ git commit -m "New commit description"
$ git pull --rebase
$ git push origin my_branch

# Delete a local commit
$ git revert fa3978
$ git reset fa3978 [--hard]

# Push the delete changes to the distant repository
$ git push --force

# Modify the commits order
$ git rebase -i fa3978

# Modify the description of the last local commit
$ git commit --amend
```

## Branches
@tags: git branch rebase merge cherry-pick

```
# Show all local branches
$ git branch

# Show remove branches
$ git branch -r

# Create a branch
$ git branch my_branch

# Go to a branch
git checkout my_branch

# Push commit from my local branch
$ git push origin my_branch

# Merge my branch into master
$ git checkout my_branch
$ git rebase master
$ git checkout master
$ git merge my_branch

# Apply a commit from another branch
$ git cherry-pick fa3978

# Delete locally a branch
$ git branch -D my_branch

# Delete a branch on the remote repository
$ git push origin :my_branch
$ git push origin --delete my_branch
```

## Tags
@tags: git tag

```
# Show existing tags
$ git tag -l

# Create locally a tag on the last commit
$ git tag v12

# Create locally a tag on an old commit
$ git tag -a v12 ba5f78

# Push a tag
$ git push origin v12

# Push all local tags
$ git push --tags

# Delete locally a tag
$ git tag -D v12

# Delete a tag on the remote repository
$ git push origin :v12
$ git push origin --delete v12

# Checkout on a tag
$ git checkout v12
```

## Config remote repository
@tags: git remote

```
# Add a remote repository
$ git remote add repo_name repo_url

# Show all remote repositories
$ git remote -v

# Update the url of a remote repository
$ git remote set-url repo_name new_url
```

## Other functionalities
@tags: git bisect tree grep blame

Vim Fugitive is a plugin to have some git command directly in vim (e.g. :Gblame).

```
# Grep into a git repository
$ git grep toto

# Repository structure
$ git tree

# Blame
$ git blame file.go

# Bisect to search a commit
$ git bisect start
$ git bisect bad # The actual version contains the bug
$ git bisect good af135c # The version af135c does not contain the bug
$ git bisect reset # To quit the bisect mode
```
