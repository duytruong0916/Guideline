# ------------- github git command Guidelines----------------

# Initializing a Repository in an Existing Directory

1. ---$ cd [directory]
2. ---$ git init
3. $ git add *.c
4. $ git add LICENSE
5. $ git commit -m 'Initial project version'
6. $ git push 

# Cloning an Existing Repository
----$ git clone <url>

# Work with branch

1. Before creating a new branch, pull the changes from upstream. Your master needs to be up to date.
------$ git pull

2. Create the branch on your local machine and switch in this branch :

-----$ git checkout -b [name_of_your_new_branch]

3. Push the branch on github:

------$ git push origin [name_of_your_new_branch].

4. Delete a branch on your local filesystem :

------$ git branch -d [name_of_your_new_branch]

5. To force the deletion of local branch on your filesystem :

------$ git branch -D [name_of_your_new_branch]

6. Delete the branch on github :

----$ git push origin :[name_of_your_new_branch]

