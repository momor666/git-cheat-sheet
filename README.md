# Git Cheat Sheet

## Commands

### Identifying differences

Unstaged differences:

`git diff`

Staged differences:

`git diff --staged`

Differences between two specific versions:

`git diff versionA versionB`

Differences in a range of versions:

`git diff version1..version2`

`git diff branchA..branchB`

Only show affected files:

`git diff --name-only version1..version2`

### Viewing history

View all changes to a specific file:

`git log -p filename`

Using `-p` generates a patch of the differences. Removing this will show the commit messages:

`git log -p --follow filename`

`--follow` will show changes to a file across renames

View all files under source control:

`git ls-files`

## Configuration

### Useful aliases

    alias.co=checkout
    alias.ci=commit
    alias.st=status
    alias.br=branch
    alias.hist=log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short
    alias.unstage=reset HEAD --

### Configuring P4Merge

`git config --global merge.tool p4merge`

`git config --global mergetool.p4merge.cmd 'p4merge $BASE $LOCAL $REMOTE $MERGED'`
