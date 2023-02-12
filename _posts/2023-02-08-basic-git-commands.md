---
title: Basic Git Commands 
author: alkaison
date: 2023-02-08 16:00:00 +0530
categories: [Blogging, Git & GitHub]
tags: [git, github, git terminal, version control]
---

### Git Init 

- To setup git tracking in a project use this command and you are good to go. 

```terminal
git init
```

- Git now knows that it should watch the folder you initiated it on. Git creates a hidden folder to keep track of changes.

### Staging / Adding files to Git repo 

- Staged files are files that are ready to be committed to the repository you are working on.
- When you first add files to an empty repository, they are all untracked. To get Git to track them, you need to stage them, or add them to the staging environment.

```terminal
git add <filename with extension>
```

#### Staging all files in folder 

- Any of this commands can be used to stage all the modified files in the repository.

```terminal
git add --all
```

```terminal
git add --A
```

```terminal
git add .
```

### Git Commit 

- Adding commits keep track of our progress and changes as we work. Git considers each commit change point or "save point".
- It is a point in the project you can go back to if you find a bug, or want to make a change.
- When we commit, we should always include a message. It helps other contributers and ourself to know what changes we made in past. 

```terminal
git commit -m "<Enter your message here>"
```

### Git Commit without Stage 

- Sometimes, when you make small changes, using the staging environment seems like a waste of time. It is possible to commit changes directly, skipping the staging environment. 

```terminal
git commit -a -m "<Enter your message here>"
```

### Git Status 

- To know the status of the current repository and check for the modified files, you can use this command. 

```terminal
git status
```

#### More compact way 

- To get the status instantly in more compact way, use this command.

```terminal
git status --short
```

### Git Log 

- To check the history of the past commits and changes you can use this commands. 
- Log is used to view the history of commits for a repo. 

```terminal
git log
```

> Use <kbd>q</kbd> to exit the log viewing mode. You can use <kbd>DOWN ARROW</kbd> to view more past logs.
{: .prompt-tip}

### Git Help 

- If you are having trouble remembering commands or options for commands, you can use Git help. 

- See all the available options for the specific command: 

```terminal
git <command> -help
```

- See all possible commands: 

```terminal
git help -all
```

> If you find yourself stuck in the list view, <kbd>SHIFT + G</kbd> to jump the end of the list, then <kbd>q</kbd> to exit the view.
{: .prompt-tip}