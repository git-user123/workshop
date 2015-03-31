## Tips & tricks
+ Auto-completion on Mac
 + Copy this [file] (https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash) to your home directory
 + add this to your .bashrc file:
    ```source ~/git-completion.bash```

+ remove untracked files from the working tree
 + ```git clean -df``` (include untracked directory)
 + ```git checkout .``` (just remove modified files, new files/directories stay)
