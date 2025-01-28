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

```bash
git add .
git commit -m "User friendly message."
```

### See Commit History
Like who and when someone commit code and what changes he did.

```bash
git log
git log --oneline
git log <banch_name>
git show <commit_id>
```


```bash
git log
```

#### Output
```bash
commit bf3be7266fd9bf67392c3f24b7c8424adc109e6e (HEAD -> master)
Author: = <=>
Date:   Tue Jan 28 21:38:20 2025 +0500

    Add initial code.
```


```bash
# For short log's
git log --oneline
```

#### Output
```bash
bf3be72 (HEAD -> master) Add initial code.
```

* Every commit has unique ID, Author name, & message.


### To see what change occure in particular commit
```bash
git show 
```

#### Output
```bash
C:\Practice\Git\Play with git> git show 961a339
commit 961a339e951b73d77e709af9615b7735cb58c3eb (HEAD -> master)
Author: = <=>
Date:   Tue Jan 28 21:46:01 2025 +0500

    Add isAbove18 functionality in index.

diff --git a/index.js b/index.js
index fa0cc57..fa77fb0 100644
--- a/index.js
+++ b/index.js
@@ -1,6 +1,11 @@
 let description = "This is git dummy crash course";
 let name = "M Huzaifa Abdulahad";
 let dob = "30-07-2007";
+
 function sayHi() {
   console.log("Hi Mr, ", name);
 }
+
+function isAbove18() {
+  return true;
+}
```

### To see line by line change did why which author & time
```bash
git blame <file_name>
```


#### Output
```bash
C:\Practice\Git\Play with git> git blame index.js
^bf3be72 (= 2025-01-28 21:38:20 +0500  1) let description = "This is git dummy crash course";
^bf3be72 (= 2025-01-28 21:38:20 +0500  2) let name = "M Huzaifa Abdulahad";
^bf3be72 (= 2025-01-28 21:38:20 +0500  3) let dob = "30-07-2007";
961a339e (= 2025-01-28 21:46:01 +0500  4) 
^bf3be72 (= 2025-01-28 21:38:20 +0500  5) function sayHi() {
^bf3be72 (= 2025-01-28 21:38:20 +0500  6)   console.log("Hi Mr, ", name);
^bf3be72 (= 2025-01-28 21:38:20 +0500  7) }
961a339e (= 2025-01-28 21:46:01 +0500  8) 
961a339e (= 2025-01-28 21:46:01 +0500  9) function isAbove18() {
961a339e (= 2025-01-28 21:46:01 +0500 10)   return true;
961a339e (= 2025-01-28 21:46:01 +0500 11) }
```


