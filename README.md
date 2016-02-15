
## ** Git cheetsheet**


### **_Git configuration_**

**git config --global user.name "[name]"**
- sets the name you want attahced to your commit

**git config --global user.email "[email address]"**
- sets the email you want attached to your commit

**git config --global pull.rebase true** 
- tells git to make a rebase instead of a merge when pulling

**git config --global credential.helper cache**
- which tells git to keep your password cached in memory for (by default) 15 minutes

**git config --global credential.helper "cache --timeout=3600"**


### **_Git basics_**

**git add -A **
- stages All

**git add .** 
- stages new and modified, without deleted

**git add -u **
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

