# .gitignore file
 + specify intentionally untracked files to ignore
   + [here] (https://github.com/git-user123/project-a/blob/master/.gitignore) is a simple example 
   + basically a pattern match

# Inspection & Comparison 
## git log (view commit history)
 + ```git log```
  + most recent commits show up first
  + SHA-1 checksum
  + author info
 + ```git log -p```
  + show difference introduced in each commit
 + ```git log -p -2``` 
  + last 2 commits
 + ```git log --pretty=oneline``` 
  + useful when looking at a lot of commits
 + time limiting options
  + ```git log --since=yesterday```
  + ```git log --since="2 weeks ago"```
  + ```git log --since="2015-01-01"```

## git diff (show changes between commits, branches, etc)
 + ```git diff```
   + show unstaged changes in your working directory
 + ```git diff --cached```  (same as ```git diff --staged```)
   + changes between index and your last commit (staged changes)
   + these changes are made by ```git add```
   + git index: where files are placed when you want committed to the git repository.
   + this is what would be committing if do ```git commit``` without "-a" option
 + ```git diff HEAD```
   + changes in working directory since your last commit
   + this is what would be committing if do ```git commit -a```
 + ```git diff [branch_a] [branch_b]```
   + changes between two branches
 + ```git diff [commit_1_hash] [commit_2_hash]```
 + ```git diff -w```
   + ignore whitespace change

## git blame (Who last modified each line of a file?)
 + ```git blame <file_name>```
 + Specify the line range in the file
  + ```git blame -L2,4 <file_name>```  (line 2 to 4)
  + ```git blame -L2,+3 <file_name>``` (3 lines since Line 2)

# Workflow managment
## git tag (mark release points)
+ create tag
  + ```git tag -a v0.1 -m "version 0.1"```
+ list tags
  + ```git tag``` (list tags)
  + ```git show v0.1``` (info about the commits that were tagged)
+ share the tag your created
  + share single tag: ```git push origin v0.1```
  + share all tags: ```git push origin --tags```
+ check out tag
  + ```git checkout -b version_0_1 v0.1```
+ tags on github

## git stash (save unfinished changes that could be re-apply later)
 + restore clean local working directory
 + ```git stash```
  + stash your work
 + ```git stash list```
 + ```git stash show -p```
  + display the changes stashed
 + ```git stash apply```
  + apply the change & keep it on stack for later use
 + ```git stash pop```
  + apply the change & then drop it from stack
 + ```git stash drop```

# Branching
## Long-running branch
 + usually represent states in your project lifecycle
 + production, testing, development
 + master branch
   + only has entirely stable code
   + other parallel dev branches, once stable, merge into master

## topic branch 
 + single topic, short lifespan
 + created for new features, bug fixes, or experiments

## Branch strategy
 + **one long-running branch only**
   + one master branch, all topic branches are based off 'master'
   + **golden rule**: everything that gets merged into "master" must be stable
   + best suited for small agile team
   + recommend merge new stuff from master into your development branch

## Basic branching
 + Create new branch
  + `git checkout -b bugfix`
   + shorthand for `git branch bugfix` followed by `git checkout bugfix`
 + List all branch
  + `git branch`
 + Swtich to other branch
  + `git checkout other_branch`
 + Delete a branch
  + `git branch -d branch_to_delete`
 + Merge a branch to other branch
  + `git merge dest_branch`
