# git_HandsOn
There we are going to explain the usage of the script seqClass.py. 
We have a problem sequence and the script will turn if it is a DNA or RNA sequence. 
Also, we can find a motif in our problem sequence.

# TASK 1 
Initialize an empty Git repo in the git_HandsOn folder. Notice the message Initialized empty Git repository in: /path/to/git_hands_on/.git/. Explore the content of the .git folder.

```
git init

cd .git/

ls -l
```
# TASK 2
Check the status of the git_HandsOn project.
```
git status
```
# TASK 3
Add seqClass.py to the staging area and check the status of the project. In the output, notice that Git indicates the changes to be committed with new file: seqClass.py in green text. Here Git tells us the file was added to the staging area.

```
git add seqClass.py

git status

```
# TASK 4
Make your first commit!


```
git commit -m "Soy Alba Burillo y este es mi repositorio"
``` 

# TASK 5
use this command to check the difference between the working directory and the staging area. Changes to the file are marked with a + and are indicated in green. Then commit the changes in seqClass.py.

```
git diff
git add seqClass.py
git commit -m "New changes"
```

# TASK 6
log a list of your commits. Display the last commit using git show HEAD.

```
git log

git show HEAD
```


# TASK 7

Edit your script to modify the message it prints when the sequence is not RNA nor DNA. Monitor the change using git status. Then, undo it using git checkout.After doing some changes, we can review them with:

```
git status

git checkout
```

# TASK 8
Remove any line from your script. Then, add the changes to the staging area, and undo this action using git reset. Use git status to monitor these steps. Hint: This command resets the file in the staging area to be the same as the HEAD commit. It does not discard file changes from the working directory, it just removes them from the staging area, so you will need to use git checkout to recover the erased line in your working directory!.

```
git reset
```

# TASK 9
Edit your script to modify the help message, stage it and commit. Then use git revert to undo your commit.


```
git add seqClass.py
git commit -m "We add some changes"
git revert HEAD
```

# TASK 10
Create a new branch named motif and check on which branch you are located.

```
git branch motif
git checkout motif
```

# TASK 11

Switch branch to motif. Verify that you switched branches succesfully and that the commit history of both branches is identical.

```
git checkout motif
git branch
git log
```
# TASK 12

```
git add seqClass.py
git commit -m "We change some coments in the script"

git checkout master
git merge motif
git log
```

# TASK 13
In the master branch, modify the message that seqClass.py prints when it finds the motif, add and commit the changes. Then, switch to the motif branch and modify the message that seqClass.py prints when it does not find the motif, add and commit the changes. Finally, merge the motif branch back into master.


```
git add seqClass.py
git commit -m "We change the found message"
git checkout motif

git add seqClass.py
git commit -m "We change the not found message"
git checkout master
git merge motif
```

# TASK 14
Repeat the previous task but modifying in both cases the message that seqClass.py prints when it finds the motif.

```
git add seqClass.py
git commit -m "We change the found message 1"
git checkout motif
nano seqClass.py
git add seqClass.py
git commit -m "We change the found message 2"
git checkout master
git merge motif
````

# TASK 15
Delete the content of the line as it appears in the master branch as well as all Git's special markings including the words HEAD and motif. Then save the file, add and commit your changes.

```
git add seqClass.py
git commit -m "We delete a line"
```

# TASK 16
Delete the motif branch.

```
git branch -d motif
```

# TASK 17
Edit your script to add some comment lines explaining what every piece of code does, stage it and commit. Then push the commits to your remote repository. The changes will be visible at GitHub.

```
git add seqClass.py
git commit -m "Modified4 script"
```

# TASK 18
Through the GitHub webpage, add a README.md file explaining the usage of the script seqClass.py and commit. It can contain just a line, or something more elaborated. Then, pull the commit to your local repository.
```
git pull
```
# TASK 20
Clone ggsashimi repository from guigolab.

```
git clone ggsashimi  guigolab
```
