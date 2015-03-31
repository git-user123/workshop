# Exercises

## Tips & tricks
+ Auto-completion on Mac
 + Copy this [file] (https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash) to your home directory
 + add this to your .bashrc file:
    ```source ~/git-completion.bash```

## git tag (mark release points)
+ create tag
  + ```git tag -a v0.1 -m "version 0.1"```
+ list tags & the commits that was tagged
  + ```git tag```
  + ```git show v0.1```
+ share the tag your created
  + share single tag: ```git push origin v0.1```
  + share all tags: ```git push origin --tags```
+ check out tag
  + ```git checkout -b version_0_1 v0.1```
+ tags on github

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

## git blame