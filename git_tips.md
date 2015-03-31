## Git terminology
 + Origin
  + orginal remote directory
  + default name Git gives to the server you cloned from
 + HEAD
  + You can think of `HEAD` as the "current branch"
  
## Tips & tricks
+ Auto-completion on Mac
 + Copy this [file] (https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash) to your home directory
 + add this to your .bashrc file:
    `source ~/git-completion.bash`

+ remove untracked files from the working tree
 + `git clean -df` (include untracked directory)
 + `git checkout .` (just remove modified files, new files/directories stay)

+ `git fetch` vs `git pull`
 + `git pull` = `git fetch` followed by `git merge`.

+ HOW-TO: Undo a Merge
 + always keep in mind that you can return to the state before you started the merge at any time. 
  + `git merge --abort`
 + In case you've made a mistake while resolving a conflict and realize this only after completing the merge
  + undo it: just roll back to the commit before the merge happened with `git reset --hard`

+ **HOW-TO**: Resolve merge conflict
 + Git marks the problematic area in the file by enclosing it in `<<<<<<< HEAD` and `>>>>>>> [other/branch/name]`.
 + A line with `=======` separates the two conflicting changes.
 + Merge pratices
   + `git checkout master`
   + `git pull origin master`
   + `git merge <dev_branch>` 
   + clean up conflict lines
   + commit the changes made to resolve conflicts
