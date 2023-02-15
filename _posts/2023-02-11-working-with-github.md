---
title: Working with GitHub 
author: alkaison
date: 2023-02-11 16:00:00 +0530
categories: [Blogging, Git & GitHub]
tags: [git, github, github repository, local and remote files]
---

### New GitHub Account

- Create a [GitHub](https://github.com "GitHub Website")  account to create your remote repositories. Now, create a new repo where we will be uploading our files from local repo. 

![Github New Remote Repository](/assets/img/github-new.png)

- Note - Local repository (repo.) means the repo. which is on our system whereas, remote repo. means the one which is on other remote system/server, for eg. - GitHub, GitLab, Bitbucket, etc. 

### Push local repo to GitHub 

- Copy the url or the link of the repo that we just created.

- Paste the copied url in the below git command. 


```terminal
git remote add origin <paste copied URL here>
```

> <kbd>CTRL</kbd> + <kbd>V</kbd> won't work in terminal. Use <kbd>SHIFT</kbd> + <kbd>INSERT</kbd> to paste the link into the terminal.
{: .prompt-warning }

### Add Remote Destinations 

- It specifies that we are adding a remote repository, with the specified URL, as an origin to our local Git repo.

- Finally, pushing our master branch to the origin URL (remote repo) and set it as the default remote branch.

```terminal
git push --set-upstream origin master
```

- Go back into GitHub and see that the repository has been updated. 

### Pushing local repo to GitHub 

- First commit all the changes. Then push all the changes to our remote origin i.e. remote repo on github.

```terminal
git push origin
```

### Pull local repo from GitHub 

- Git pull is used to pull all changes from a remote repository into the branch we are working on. It is a combination of fetch and merge. Use it to update your local Git.

```terminal
git pull origin
```

### Pull Branch from GitHub 

- First, check which branches we have and where are we working at the moment by using this command. 

```terminal
git branch
```

- Since we do not have the new branch on out local Git which is to be pulled from the Github. So, to see all local and remote branches, use -

```terminal
git branch -a
```

#### For viewing only remote branches 

```terminal
git branch -r
```

- Now, the new branch is seen in the console but it is not available on 
our local repo. So, let’s check it out using 

```terminal
git checkout <branch name>
```

- Now run the below command to pull that branch on our local repo. 

```terminal
git pull
```

- We can now check the available branches using the command.

```terminal
git branch
```

### Push branch to GitHub 

- First, let’s create a new local branch which we will be pushing to 
Github. Enter the command as 

```terminal
git checkout -b <branch name>
```
- You can check the status of the files in this current branch using 

```terminal
git status
```

- Commit all the uncommitted changes for all the files in this branch using 

```terminal
git commit -a -m “<Message>”
```

- Now push this branch from our local repo to Github using 

```terminal
git push origin <branch name>
```

### Git Clone from GitHub 

- We can clone a forked repo from Github on our local repo. A clone is a full copy of a repository, including all logging and versions offiles. Move back to the original repository, and click the green "Code" button to get the URL to clone. Copy the URL.

- Now in the git bash, enter the following command to clone the copied repo onto your local machine

```terminal
git clone <copied URL>
```

- To specify a specific folder to clone to, add the name of the folder after the repository URL, like this 

```terminal
git clone <copied URL> <folder Name>
```
