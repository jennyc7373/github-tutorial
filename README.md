# GitHub Tutorial

_By: Jenny Chen_

---
## Git vs. GitHub
**Git** is what people use to create repositories to track their changes.

**GitHub** is a server that brings people together in the repositories that was created.

---
## Initial Setup
1. Create an account in [Github](https://github.com/)
2. Go to [IDE](https://ide.cs50.io/) and to create an account you will need to connect it to your github account. 
3. To finish setting up go to this [link](https://github.com/hstatsep/ide50).

* While going through the setup in the directions in the link, you may wonder what is an SSH key and why is it important.
   * An SSH key is for public or private access to repositories in Github. SSH allows the user to just log on automatically without signing in to their account again. 
   * By adding this key it allows you to have access to other repositories easily and faster. If not you will have to keep on log in over again everytime. 

---
## Repository Setup
To set up you will need to create a repository.

> ###### Github

1. Sign into Github
2. In the top right corner, click the plus sign and create a new repository.
3. Then name your repository and can not use space but replace space with a dash.
   * You can't use space because the url will be using the name you set to your repository and an url doesn't and can't have space in it.

                Ex: lemon-soda
4. Click 'create repository'.
5. It will then lead you to directions to do in your **ide** so you can connect your remote to your local repository.

> ###### IDE

You need to type...
        
1. `git init` 

**git init**: is to initialize git in your directory for version control.
* Always _initialize git_ inside a repository and not in a parent directory.

2. `git add` READ.ME

**git add**: 

3. `git commit -m` "message"

**git commit -m**: 

4. `git remote add origin`git@github.com:username/repository-name.git

**git remote add origin**:connects remote to local repo

5. `git push` -u origin master

**git push**:send all changes to local repo or can be the opposite.

#### Another way to set up is...
1. git init
2. git remote add origin git@github.com:username/repository-name.git
3. git push -u origin master
4. git add .
5. git commit -m "___"

---
## Workflow & Commands
If you want to continue to work in your ide, some commands you will be constantly using are...

* `git status`:Keeps you updated (tell if there are changes or not)
   * An optional command to see which files have been edited since the last commit (they will be red)
   * Another optional command to see which files are staged for the commit (they will be green)

* `git add .`: add the files you create or the files you make changes on your repository
* `git commit -m`: to save all the changes you made and leaving a message about what was changed
* `git push`: push all changes to the remote(Github)

---
## Rolling Back Changes
Sometimes you will make mistakes in ide and to undo it you will be using commands like...

* `git checkout` -- filename is for undoing edits
* `git reset` HEAD -filename is for undoing adds
* `git reset` HEAD~1 is for git commit
* `git revert` for git push

---
## Error Handling
If you did `init` in the wrong directory use `rm -rf .git`

> To remove a repository in the remote just go to repository and click on setting, scroll down, click delete.

> To remove a repository in the local just right click your mouse on the repository you want to delete.

---
## Collaboration
There will be times when you want to collaborate with someone else or they want to collaborate with you which then you will be using fork, `clone`, and pull request.
1. Go into someone elses repository in Github and click `fork`.
2. Click the clone botton and copy SSH to clipboard.
3. Go to your IDE, type `git clone` _the url_.
4. You will then see a new folder in your IDE. 

From there on you can make the changes you want. 
Once you finish editing you can go back to Github and click on new pull request to ask the owner for approval.
* The owner can choose to pull it so then the changes will be pushed to their repository or they can just not pull.
