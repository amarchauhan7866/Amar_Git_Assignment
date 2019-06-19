
# Q.1 Initialize a local git repository
  Run git status command  
  Create a file README.md  


```
Ans:- 


[root@ninjaopstree ~]# mkdir devops1
[root@ninjaopstree ~]# cd devops1
[root@ninjaopstree devops1]# git init
Initialized empty Git repository in /root/devops1/.git/  

```

###################################

```
[root@ninjaopstree devops1]# git status
# On branch master
#
# Initial commit
#
nothing to commit (create/copy files and use "git add" to track)  

````

[root@ninjaopstree devops1]# touch README.md 

# Q.2 Run git status command  
     Add file README.md in your local repository  
     Add My first interaction with Git content in README.md  


```
[root@ninjaopstree devops1]# git status
# On branch master
#
# Initial commit
#
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#       README.md
nothing added to commit but untracked files present (use "git add" to track)

```

````
[root@ninjaopstree devops1]# git add README.md
[root@ninjaopstree devops1]# git commit -m "Readme file create" README.md
[master (root-commit) 34f6f2f] Readme file create
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
[root@ninjaopstree devops1]#

```

# Q.3 Run git status command
      Update file README.md in your local repository
     Run git status command  
     Create files README1.md README2.md README3.md README4.md

# Ans:

```
[root@ninjaopstree devops1]# git status
# On branch master
# Changes not staged for commit:
#   (use "git add <file>..." to update what will be committed)
#   (use "git checkout -- <file>..." to discard changes in working directory)
#
#       modified:   README.md
#
no changes added to commit (use "git add" and/or "git commit -a")
[root@ninjaopstree devops1]#

```

[root@ninjaopstree devops1]# git add README.md  
[root@ninjaopstree devops1]# git commit -m "updated readme file" README.md  
[master 122c8aa] updated readme file  
 1 file changed, 1 insertion(+)  
[root@ninjaopstree devops1]#  

# Now Creating the Multiple file

[root@ninjaopstree devops1]# touch README1.md README2.md README3.md README4.md  
[root@ninjaopstree devops1]# ls  
README1.md  README2.md  README3.md  README4.md  README.md


############################################################

# Q.4 
 
## Run git status command
Add all the newly added files in your local repository without giving their name.  
Run git status command  
Remove files README1.md README2.md from local repository  
Add content in Temporary content in README3.md  

```
[root@ninjaopstree devops1]# git status
# On branch master
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#       README1.md
#       README2.md
#       README3.md
#       README4.md
nothing added to commit but untracked files present (use "git add" to track)
[root@ninjaopstree devops1]#

````



############################################

```
[root@ninjaopstree devops1]# git add .
[root@ninjaopstree devops1]# git commit -m "All Readme file added" .
[master 299f490] All Readme file added
 4 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README1.md
 create mode 100644 README2.md
 create mode 100644 README3.md
 create mode 100644 README4.md
[root@ninjaopstree devops1]#

```

## [root@ninjaopstree devops1]# git status
# On branch master  
nothing to commit, working directory clean  


[root@ninjaopstree devops1]# git rm README1.md README2.md
rm 'README1.md'
rm 'README2.md'

# Q.5 
## Run git status command
## Find out the content that is added in README3.md

# Ans:-

```
[root@ninjaopstree devops1]# git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD <file>..." to unstage)
#
#       deleted:    README1.md
#       deleted:    README2.md
#
# Changes not staged for commit:
#   (use "git add <file>..." to update what will be committed)
#   (use "git checkout -- <file>..." to discard changes in working directory)
#
#       modified:   README3.md
#
[root@ninjaopstree devops1]#

```

############################

```
[root@ninjaopstree devops1]# git diff README3.md
diff --git a/README3.md b/README3.md
index e69de29..3b2aed8 100644
--- a/README3.md
+++ b/README3.md
@@ -0,0 +1 @@
+this is a new file
[root@ninjaopstree devops1]#

```

# Q.6 

## Undo the changes in README3.md file
## Run git status command
## Create a branch ninja from current branch
## Create sensei branch from ninja branch and switch to sensei branch
## List out all the local branches
## Delete sensei branch
## Find out the current branch
## List out all the commits that have been done

# Ans:-

#########################################

```
[root@ninjaopstree devops1]# git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD <file>..." to unstage)
#
#       deleted:    README1.md
#       deleted:    README2.md
#
[root@ninjaopstree devops1]#

```


## [root@ninjaopstree devops1]# git branch ninja
## [root@ninjaopstree devops1]# git branch
    * master
    ninja
[root@ninjaopstree devops1]# git checkout ninja
D       README1.md
D       README2.md
Switched to branch 'ninja'
[root@ninjaopstree devops1]# git branch
  master
* ninja
[root@ninjaopstree devops1]# git branch sensei
[root@ninjaopstree devops1]# git branch
  master
* ninja
  sensei
[root@ninjaopstree devops1]#

############################################################

[root@ninjaopstree devops1]# git branch -d sensei
Deleted branch sensei (was 299f490).
[root@ninjaopstree devops1]#


[root@ninjaopstree devops1]# git branch
  master
* ninja



########################################


root@ninjaopstree devops1]# git log
commit 299f49001239372220978f09c4359503715efda1
Author: amarchauhan7866 <amarchauhan7866@gmail.com>
Date:   Thu Jun 20 04:24:49 2019 +0530

    All Readme file added

commit 122c8aa4b7a9d6a2f65ae1f30fe6d6f4d6cf4ddb
Author: amarchauhan7866 <amarchauhan7866@gmail.com>
Date:   Thu Jun 20 04:01:16 2019 +0530

    updated readme file

commit 34f6f2f55f47451149196ab5caa2a1752820bea2
Author: amarchauhan7866 <amarchauhan7866@gmail.com>
Date:   Thu Jun 20 03:57:01 2019 +0530

    Readme file create




