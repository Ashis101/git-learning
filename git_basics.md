# What is Git Repo
-- Git Repo is a workspace which tracks and manages files within a folder.

# Git Command

> git status
  ** gives information on the current status of a git repository and it's contents
  
> git init 
  ** Use git init to create a new git repository.before we can do anything git-related, we must initialize a repo first.
  
> git add file1 file2
  ** use git add to specific files to the stagging area.separete files with spaces to add multiple at once.
  
> git commit -m "My Message"
  ** commit changes from staging area.when making a commit,we need to provide a message that summarizes the changes and work snapshotted in the commit.
  
> git commit -m "somthing"
> git add forgotten_file
> git commit --amend

  ** Suppose you just made a commit and then realized you forgot to include a file! Or,maybe you made a typo in the commit message that you want to correct.rather than making a new seperate commit,can "redo" the previous commit using the --amend option
  
  
# Branch  

> git branch
** use git branch to view your existing branches. the default branch in every git repo is master, through you can configure this.  
  
> git branch <branch-name> 
** to make a new branch based upon the current HEAD.This just creates the branch.it does not switch you to that branch ( the HEAD statys the same ) 
  
> git branch -m <new-name>
** Renaming the current HEAD branch

> git branch -m <old-name> <new-name>
** Renaming any local branch 

> git checkout -b  hello-you
** Create, and move to a new branch with the name hello-you

> git  switch <branch-name>
** switch to another branch

> git switch -c <branch-name>
** use git switch with -c flag to create a new branch and switch to it all in one go. remember -c as short for "create"

> git branch --merged
** which branch are merged now

> git branch --no-merged
** which branch are not merged

--- Renaming remote branch
> git push origin --delete <old-name>
** first, delete the current/old branch

> git push -u origin <local-branch>
** not posible to create new branch in remote repository.make it first on local then upload to remote server.


> git push -u origin <new-name>
** Then, simply push the new local branch with the correct name.

--- upload download from remote branch

> git branch --track feature/login origin/feature/login
** here first creating brach under branch and put remote staff into that branch.

> git checkout --track origin/feature/login
** download remote branch in local. 

---- Syncronizing your local + remote branch
> git pull

** pull is combination of ,first fetch and then merge.
> git push

> git -v 
** show the information about pull and push.how many commits are not yet publish or how many are not downloaded.
  
> git fetch origin
** Get all the change history of the origin for this branch  
  
> git pull origin
** Update the current branch from its origin using a single command
  
# Merging

git merge --squash <branch-name>
** when you are in main branch then merge another branch to it, --squash  does not allow to commits from another branch to merge with main 

# DIFF

> git diff 
** list all the changes in our working directory that are not staged for the next commit.

> git diff HEAD
** list all changes in the woring tree since your last commit

> git diff --staged or --cached
** list changes between the staging area and our last commit.

> git diff HEAD {filename} or git diff --staged {filename}
**we can view the changes within a specific file by providing git diff with a filename.

> git diff {branch1} {branch2}  
** list the changes between the tips of branch1 and branch2

> git diff {commit1} {commit2}
** comapre two commits,provided git diff with the commit hashes of the commits in question.


# Stash

> git stash

** save changes that you are not yet ready to commit.you can stash changes and then come back to them later.

running git stash will take all uncommited changes and stash them,reverting the changes in your working copy

> git stash pop

** to remove the most recently stashed changes in your stash and re-apply them to your working copy.

> git stash apply 

** apply whatever is stash away,without removing if from the stash.usefull in stash changes to multiple branches

> git stash drop <stash-id>

** delete particular staff

# checkout

> git checkout commit <commit-id>

** check what is in that commit.

> git checkout HEAD~1

** pointing head to a commit

> git checkout HEAD <filename> 

** to discard any changes in that file,reverting back to the HEAD

# Restore

> git restore <file-name>

** the above command is not "undoable" if you have uncommited changes in the file they will be lost.

> git restore --source HEAD~1 <file-name> 

** git restore <file-name> restore using HEAD as the default source but we can change that using the --source option.

> git restore --staged <file-name>

** if you have accidentally added a file to your staging area with git add you don't wish to include it in the next commit,you can use git restore to remove it from staging.

> git reset <commit-hash> 

** will reset the repo bac to a specific commit, the commit are gone. 
 
 









  
  
  