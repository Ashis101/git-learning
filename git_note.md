# What is Git
-- git is version control system that helps tracks and manages changes to 					files over time.

# What does it do?
-- Track changes across multiple files
   Compare versions of a project
   Travel back to older version
   Revert bac to a previous version
   Collaborate and share changes
   Combine changes

# git config

-- git config --global user.name "Your Name"
   git config --global user.password "Your Password"

** check configure or not
-- git config user.name

# .gitignore
  ** Create a file called .gitignore in the root of a repository.
  there is some pattern to tell git which files & folder to ignore
  	.DS_store will ignore files named .DS_STORE
  	FolderName/  will ignore an entity directory
  	*.log will ignore any files with the .log extension
  	
# Branch 
-- we are alwayse woring on a branch.the default branch name is "master".

** commit 548784asdhbsbkajnljcc454c (HEAD -> master) what is Head ?
-- Head is simply a pointer that refers to the current "location" in your repository.it points to a particular branch reference.so far Head always point to the latest commit you made on the master branch,but soon we'll see that we can move around and HEAD will change.


# HEAD 

-- we'll often come across the term HEAD in git.HEAD is simply a pointer that refers to the current "location" in your repository.It points to a particular branch reference.So far,HEAD always points to the latest commit you made on the master branch,but soon we'll see that we can move around and HEAD will change.


# Merging

-- Branching makes it super easy to work ithin self-contained contexts,but often we want to incorporate changes from one branch into another.

	. We merge branches,not specific commits
	. We always merge to the current HEAD branch

	-- To merge,follw this step 
	. Switch to the branch you want to merge the changes 	into (the receving branch)
	. Use the git merge command to merge changes from a specific branch into the current branch.
	
#resolve merge conflict

1.Open up the files with merge conflicts.
2.Edit the file to remove  the conflicts.Decide which branch's content you want to keep in each conflict.Or keep the content from both.
3.Remove the conflict "markers" int the document.
4.Add your changes and then make a commit.


# Diff

we can use the git diff command to view changes between commits,branches,files our working directory and more!

we often use git diff alongside commands like git status and git log,
to get a better picture of a repository and how it has changed over time

# Stashing

** My changes come with me to the destination branch 
** Git won't let me switch if it detects potential conflicts

 
# detaching and re-attaching

** detaching head happen when head refer to a commit not a branch (git chechout < id of commit>).
   
attaching head to a branch ,simple (git switch <branch-name>)   


# pointing head to a commit by counters (1,2,3)

** HEAD~1 refers to the commits before HEAD(parent)
   HEAD~2 refers to 2 commits before HEAD (grandparent)
   
# Discard Changes

** suppose you have made changes but don't want to keep them.to revert the file back to whatever it looked like when you last commited.

# Restore

** git restore is a brand new git command that helps with undoing operations.


# Revert

** Instead of creates a brand new commit which reverses/undos the changes from a commit.Because it result in a new commit you will be prompted to enter a commit message.

# Reflog

** git keeps a record of when the tips of branches and other referencees were updates in the repo 
we can view and update these reference logs using the git reflog command



