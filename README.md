
## Git cheetsheet


### **Git configuration**

**git config --global user.name "[name]"**
- sets the name you want attahced to your commit

**git config --global user.email "[email address]"**
- sets the email you want attached to your commit

**git config --global pull.rebase true** 
- tells git to make a rebase instead of a merge when pulling

**git config --global credential.helper cache**
- which tells git to keep your password cached in memory for (by default) 15 minutes

**git config --global credential.helper "cache --timeout=3600"**


### **Git basics**

**git add -A** 
- stages All

**git add .** 
- stages new and modified, without deleted

**git add -u**
- stages modified and deleted, without new

**git status**
- list all new or modified files to be commited

**git diff**
- shows the changes between the working directory and the index. This shows what has been changed, but is not staged for a commit

**git diff --cached**

- shows the changes between the index and the HEAD(which is the last commit on this branch). This shows what has been added to the index and staged for a commit.

**git diff HEAD**

- shows all the changes between the working directory and HEAD (which includes changes in the index). This shows all the changes since the last commit, whether or not they have been staged for commit or not.

_More details about git diff_:
_[http://www.gitguys.com/topics/git-diff/](http://www.gitguys.com/topics/git-diff/)_

**git log**
- lists version history for the current branch

**git commit -m**
- commits all the files from the staging area

**git commit -a**
- git automatically stage every file that is already tracked before doing the commit, letting you skip _git add_ part

### **Working with remotes**

**git fetch [remote-name]**
- default name for a remote project is origin
- the command goes to the remote project and pulls down all the data from the remote project that you don't have yet
- it doesn't automatically merge it any of your work => merge manually

**git pull [remote-name]**
- fetches data from the server you originally cloned from and automatically tries to merge it into the code you're currently working on

**git push [remote-name] [branch-name]**
- uploads all local branch commits to GitHub

### **Stashing**

**git stash**
- stashing takes the dirty state of the working directory (modified tracked files and staged changes) and saves it on a stack of unfinished changes that you can reapply at any time

**git stash list**
- lists the stashed that you have stored

**git stash apply**
- applies tha latest stash (stash@{0})

**git stash apply <stash_id>**
- applies a specific stash

_**git stash apply** command only tries to apply the stashed work and does not remove it from the stashed work._

**git stash pop**
- applies the stash and then immediately drops it from the stach

### **Squash**

**git reset --soft HEAD~N**
**git commit -m**
- squashes last N commits

**git rebase -i HEAD~N**
- gives the possibility to squash 

### **Make the current commit the only (initial) commit in a Git repository**
http://stackoverflow.com/questions/9683279/make-the-current-commit-the-only-initial-commit-in-a-git-repository
