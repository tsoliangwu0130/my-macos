## Git Cheat Sheet

### [Git References](https://git-scm.com/book/en/v2/Git-Internals-Git-References)

`HEAD`: The latest commit

`HEAD^` / `HEAD~1`: The previous commit before the latest commit

`HEAD~n`: The previous n commit(s) before the latest commit

### [Clone](https://git-scm.com/docs/git-clone)

Clone an existing repository

```
$ git clone <git_url>
```

### [Initialize](https://git-scm.com/docs/git-init)

Initialize a new repository

```
$ git init
```

### [Remote](https://git-scm.com/docs/git-remote)

List all `remotes`

```
$ git remote -v
```

Show information about `remote`

```
$ git remote show <remote>
```

Add a new `remote` repository

```
$ git remote add <remote> <git_url>
```

### [Status](https://git-scm.com/docs/git-status)

Show files status

```
$ git status
```

### [Differences](https://git-scm.com/docs/git-diff)

Show differences

```
$ git diff
```

Show all conflicted files

```
$ git diff --name-only --diff-filter=U
```


### [Add](https://git-scm.com/docs/git-add)

Add `files` for next commit

```
$ git add <file>
```

Add all files under current directory for next commit

```
$ git add .
```

Add all files in entire project for next commit

```
$ git add --all
```

### [Remove](https://git-scm.com/docs/git-rm)

Remove `file` from the working tree

```
$ git rm <file>
```

### [Commit](https://git-scm.com/docs/git-commit)

Commit all added files

```
$ git commit
```

Modify the latest commit

```
$ git commit --amend
```

### [Tag](https://git-scm.com/docs/git-tag)

List all tags

```
$ git tag
```

Mark current commit with a `tag`

```
$ git tag <tag>
```

### [Stash](https://git-scm.com/docs/git-stash)

Save changes away and revert back to the `HEAD` commit

```
$ git stash
```

List all stashes

```
$ git stash list
```

Pop a stash and apply it on top of the current working tree

```
$ git stash pop
```

### [Log](https://git-scm.com/docs/git-log)

Show entire commits log

```
$ git log
```

Show commits log for a `file`

```
$ git log <file>
```

Show author and modification date for a `file`

```
$ git blame <file>
```

### [Branch](https://git-scm.com/docs/git-branch)

List all existing branches

```
$ git branch -av
```

Delete a `branch` locally

```
$ git branch -d <branch>
```

Delete a `branch` on the `remote`

```
$ git branch -dr <remote/branch>
```

Create a new `branch`

```
$ git branch <branch>
```

### [Checkout](https://git-scm.com/docs/git-checkout)

Switch to `branch`

```
$ git checkout <branch>
```

Create and switch to a new `branch` based on current branch

```
$ git checkout -b <branch>
```

Create and switch to a new `branch` based on a `remote` branch

```
$ git checkout --track <remote/branch>
```

### [Pull](https://git-scm.com/docs/git-pull)

Fetch and merge all changes from a `remote` and `branch`

```
$ git pull <remote> <branch>
```

### [Push](https://git-scm.com/docs/git-push)

Push commits to a `remote` and `branch`

```
$ git push <remote> <branch>
```

Push tags

```
$ git push --tags
```

### [Merge](https://git-scm.com/docs/git-merge)

Merge `branch` to current branch

```
$ git merge <branch>
```

### [Reset](https://git-scm.com/docs/git-reset)

Discard all changes in current working tree

```
$ git reset --hard HEAD
```

Discard all changes in current working tree since a `commit`

```
$ git reset --hard <commit>
```

Reset commit to a `commit` and preserve changes as unstaged

```
$ git reset <commit>
```

### [Cherry-pick](https://git-scm.com/docs/git-cherry-pick)

Apply the changes from a `commit`

```
$ git cherry-pick <commit>
```

### [Rebase](https://git-scm.com/docs/git-rebase)

Rebase your `HEAD` commit on to a `branch`

```
$ git rebase <branch>
```

**Warning: DO NOT do rebase if you are not sure what you are doing.**

### [Submodule](https://git-scm.com/docs/git-submodule)

Initialize submodules recorded

```
$ git submodule init
```

Update submodules by cloning missing submodules

```
$ git submodule update
```

Update every submodule to latest commit on origin

```
$ git submodule foreach --recursive git pull origin master
```

### References

1. [Pro Git Book English](https://git-scm.com/book/en/v2)
2. [Pro Git Book 繁體中文](https://git-scm.com/book/zh-tw/v1)
