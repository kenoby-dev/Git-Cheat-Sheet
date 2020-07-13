# git - Undoing Changes

Get the history:
```
git log --oneline
```

Output:
```
<commit id> <message>
99887 Deleted unused files
67890 Added new files
12345 Initial commit 
```

View an old version:
```
git checkout 67890
```

Return to the current version:
```
git checkout master
```

Tag a release:
```
git tag -a v1.0 -m "Stable version"
```

Checkout based on tag:
```
git checkout v1.0
```

Undo committed changes:
```
git revert 99887
```

**Note**: creates a new commit that undoes the changes, like so:

```
66554 Revert "Delete unused files"
99887 Deleted unused files
67890 Added new files
12345 Initial commit 
```

Undo uncommitted changes (reset *tracked* files to most recent commit):
```
git reset --hard
```
**Note**: `--hard` updates the file, if you don't include the `--hard` switch, then the file/s are untracked and the contents are left as is.

Remove all *untracked* files:
```
git clean -f
```

**Note**: `git reset` and `git clean` operate on the working directory and *permanently* undo changes.
