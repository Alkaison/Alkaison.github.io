---
title: Git Branch & Merge PR's
author: alkaison
date: 2023-02-10 16:00:00 +0530
categories: [Blogging, Git & GitHub]
tags: [git, github, git branch, git terminal, version control]
---

- In Git, a branch is a new/separate version of the main repository.

- Branches allow you to work on different parts of a project without impacting the main branch. When the work is complete, a branch can be merged with the main project.

- We can even switch between branches and work on different projects without them interfering with each other.

### New Git Branch 

```terminal
git branch <name of branch>
```

### Check All Branches 

```terminal
git branch
```

### Switching to other branches 

```terminal
git checkout <branch name>
```

### Making a new branch and directly switching to it 

```terminal
git checkout -b <branch name>
```

### Deleting a branch

```terminal
git branch -d <branch name>
```

### Merging two branches 

- It’s preferred to change/switch to master branch before any branch needs to be merged with it.

```terminal
git merge <branch name>
```

- This will merge the specified branch with our master branch. 