---
title: Configuring Git for the first time 
author: alkaison
date: 2023-02-07 16:00:00 +0530
categories: [Blogging, Git & GitHub]
tags: [git, github, git bash, version control]
---

### Installing Git Setup

Choose your operating system and download the Git setup from official website [here](https://git-scm.com/downloads). After download follow the steps and install it.

> Don't change any options, let it be on default.
{: .prompt-warning }

> If you are planning to first learn only Git and later on GitHub, you can skip below steps. We will be connecting Git and GitHub for pushing our code on GitHub.
{: .prompt-info}

### Get GitHub Account

- Go to [GitHub](https://github.com) site and sign up with a new email ID and create your account. 

- If you have account on GitHub already login and follow the steps below.

### Generating SSH Keys 

- Read the information carefully and then only use the commands.

#### Set Username

- Enter the below command and replace the text within the quotes with your GitHub username or whatever you wish your username to be.

```bash
git config --global user.name “Enter your username here”
```

#### Set Email ID

- Enter your email ID within the quotes and press <kbd>ENTER</kbd>.

```bash
git config --global user.email “Enter your email here”
```

#### SSH Key

- Type the command to check if theres existing SSH Key on the system.

```bash
ls -al ~/.ss
```

#### Get New SSH Key 

- Enter the command to generate new SSH Key for the system, if there's no key aleardy existing. Replace the text within quotes with your email ID. Press <kbd>ENTER</kbd> till the end.

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

#### Copy the SSH Key

- It is used to check pid of the SSH Keys.

```bash
eval "$(ssh-agent -s)"
```

- It is used to view the SSH Keys on terminal and copy it.

```bash
tail ~/.ssh/id_ed25519.pub
```

### Connect SSH Key 

- Go to  GitHub profile and open settings. 

- Under settings go to SSH and GPG Keys.

- Add the SSH Key which we copied from Git Bash terminal.

- Verify your GitHub Email ID and you are done.

> Your account is now linked with your GitHub profile and now you are ready for using git and open source projects.
{: .prompt-tip}