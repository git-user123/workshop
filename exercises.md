# Exercises

## Tips & tricks
+ Auto-completion on Mac
 + Copy this [file] (https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash) to your home directory
 + add this to your .bashrc file:
    ```source ~/git-completion.bash```

## git tag (mark release points)
+ create tag
  + ```$git tag -a v0.1 -m "version 0.1"```
+ list tags & the commits that was tagged
  + ```$git tag```
  + ```$git show v0.1```
+ share the tag your created
  + share single tag: ```git push origin v0.1```
  + share all tags: ```git push origin --tags```
+ check out tag
  + ```git checkout -b version_0_1 v0.1```

  
