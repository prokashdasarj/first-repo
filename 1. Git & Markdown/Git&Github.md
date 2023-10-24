# ⚡Git & GitHub CheatSheet⚡

Git is a version control system, which allows us to track changes in our files. 

## Git

**Configure Git (Local)** 

    git config --global user.name "userName"
    git config --global user.email "useremail.com"
    git config --list

**4 Stages of git environment:** 

    Untracked - Modified - Staged - Unchanged

**Git tracking Start:**

    git init (We get a .git folder)

**Show all changes since the previous commit:**

    git status (State of our code)

**Pick changes to go into next commit:**

    git add <file|folder|.> (working => staging)

**Going back drom Staging to working**
    
    git reset <file|folder|.> (Staging => working)


**Creates a commit with a message attached:**

    git commit -m "message"

**Update previous commit instead of creating new one**

    git commit -m "message" --amend

**View the commit history**

    git log
    git log --all
    git log --all --graph

**Features of Git**

    git config --global alias.shortcut <command> Creates an alias (a shortcut)

    git config --global alias.s "status" (git s = git status)

    .gitignore (Tell git which files/folders it SHOULD NOT track)
    
    rm -rf .git (Remove git from project)


## GitHub

Github is a website which helps us to upload our project on internet so that we can share and colaborate with others.

**Configure our Git to Access Github Account**

    git config --global credential.username <username>

**Link to a Github Repo (Remote)**

    git remote add <NamingTheRepo> <repoUrl>

**Remove a Linked repo**

    git remote remove <remoteName>
 
**See all the remote repos**

    git remote (List all remote repositories that are linked)
    git remote -v (List all remote repositories but with more detail)
 
**Push/Upload to Github**

    git push <repoName> <branchName> (git push origin main)
    git push origin main --set-upstream (Set Shortcut for next push)
    or 
    git push -u origin main (Set Shortcut for next push)

**Download/Pull Code from GitHub**

    git clone <HttpsRepoUrl>

## Easy Git and Github Workflow

    Create a Github Repo
    Clone the repo
    Change we wanna make
    git add .
    git commit -m "commit massage"
    git push

**Git Branches**

    git branch (Shows a list of available branches)
    git checkout -b <branchName> (Create and go to a new branch)
    git checkout feature1 (Go to a another branch)
    git branch -M <NameWeWant> (Rename the branch)
    git branch -d <branchName> (Delete a branch and Have to run from a diff branch)

**Git Merge**

    git diff <OtherBranchName> (Shows the diff between branches)
    git merge <OtherBranchName> -m "message" (Merging current branch to other branch)
    Pull Request from Github Wensite

**Get Remote changes to Local Machine**

    git pull <repoName> <branchName> (git pull origin main)

**Updates all remote tracking branches**

    git fetch

**Undo the Changes**

    Undo the Chnages from Staging Area:
    git reset <file|folder|.> (Staging => Working)
    
    Undo the changes from Commit History:
    git reset Head~1 (Goes one step back)
    git reset <commitHashCode> (C/H => Working)
    git reset --hard <commitHashCode> (C/H => Working)
    git commit -m "message" --amend (Save into the previous commit insted of creating new commit)

**Forking in Github**

Forking means creating a new rough copy of other repos in our Account.  

**Pull Request** 

Creating Pull request means letting someone know to marge the changes we make in their repo. 

**Issue** 

Issue creating means letting someone know that there is a problem in the code and can they fix it!

**Head**

HEAD points to which branch we are currently working on.

**Merge Conflicts**

![](Screenshot%20(2).png)

**To resolve a merge conflict**

![](Screenshot%20(3).png)

**Feature Branch Workflow**

A popular process that companies use when adding new features to their software

![](Screenshot%20(5).png)
![](Screenshot%20(6).png)

**Merge Conflicts in the Feature Branch Workflow**

A merge conflict can happen if 2 or more pull requests change the same file and the same line.

![](Screenshot%20(9).png)
![](Screenshot%20(10).png)

This Cheat-sheet is written on Markdown. Check Out [MarkDown Notes](Markdown.md) here.