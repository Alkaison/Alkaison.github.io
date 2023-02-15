---
title: Git Undo and Revert 
author: alkaison
date: 2023-02-12 16:00:00 +0530
categories: [Blogging, Git & GitHub]
tags: [git, github, git undo, git revert]
---

- 'revert’ is the command we use when we want to take a previous commit and add it as a new commit, keeping the log intact. 

- First thing, we need to find the point we want to return to. To do that, we need to go through the log. To avoid the very long log list, use the --oneline option which gives just one line per commit showing. 

  1. The first seven characters of the commit hash. 
  2. The commit message. 

```terminal
git log --oneline
```

### Git Revert HEAD 

- We can revert the latest commit using ‘git revert HEAD’ (revert the latest change, and then commit). By adding the option --no-edit, we can skip the commit message editor (getting the default revert message).

```terminal
git revert HEAD --no-edit
```

### Git Revert to any commit 

- To revert to earlier commits, use ‘git revert HEAD~x’ (x being a number. 1 going back one more, 2 going back two more, etc.) 

- Command to go back by one commit 

```terminal
git revert HEAD~1
```

### Git Reset 

- ‘reset’ is the command we use when we want to move the repository back to a previous commit, discarding any changes made after that commit.

- First, get the seven characters of the commit hash from the log for the commit that you want to go back for.

- Then we reset our repository back to that specific commit using ‘git reset commithash’ (commithash being the first 7 characters of the commit hash we found in the log).

```terminal
git reset 6199a6f
```

### Git Undo Reset 

- Even though the commits are no longer showing up in the log, it is not removed from Git. If we know the commit hash, we can reset to it using

```terminal
git reset <commithash>
```

### Git Amend 

- 'commit --amend' is used to modify the most recent commit. It combines changes in the staging environment with the latest commit, and creates a new commit. This new commit replaces the latest commit entirely.

- One of the simplest things you can do with --amend is to change a commit message 

```terminal
git commit --amend -m "Commit message here"
```

- Using this, the previous is replaced with our amended one.

#### Git Amend Files 

- Adding files with '--amend' works the same way as above. Just add them to the staging environment before committing. 