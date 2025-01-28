# Git Commands
## By M Huzaifa Abdulahad

## Initialize Git
To initialize a new Git repository in your project directory, use the following command:
```bash
git init
```

## Git Flow
```bash
Working Directory
                 to
                 Staging Area
                             to
                             Local Repo
                                       to
                                       Remote Repo
```


## Check what is being changed
```bash
git diff <file_name>
git diff
```
### Output
* ++ represent addition in any file
* -- represent deletion from file.
* ++ This is added in the file.
* -- This is delete from the file.


## Adding File to VCS
```bash
git add <file_name>
# Add all files from current dir (.)
git add . 
```

## Remove File from Stagging Area
```bash
git rm <path || file_name>
git rm -f <path || file_name>
# force remove
git rm -f ./utils/index.js
```

## Introduction to Commit
Regularly committing your code creates checkpoints throughout your project. For instance, if you're building a game, after completing level-1, you commit your changes. Once level-2 and level-3 are done, you commit again. If an issue arises at level-3, you can easily revert to the version from level-2 by checking out the commit made at that stage. These timely commits help you track your progress and allow you to roll back to a stable version whenever needed.