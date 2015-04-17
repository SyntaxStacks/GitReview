#Git Review

###What we'll cover:

* Forking a repo
* Cloning your fork
* Adding the upstream remote 
* Setting master to track upstream master
* Creating a branch
* Commit a change to a file
* Commit a new file
* Squashing commits
* Amending a commit
* Pushing your changes to Github

##Forking a repo

Forking a repo creates a duplicate repo that is independent from the original
project. You can code without fear of impacting the code base. To create a
fork, click the "fork" button in the top right hand corner of the repo page.
[img]

##Cloning your fork
The following command can be used to clone your fork to your local machine.

```
git clone <repository_url>
```
##Adding the upstream remote 
```
git remote add upstream <main_repo_url>
```

##Setting master to track upstream master
To get the latest changes from the upstream project we will set master to track the upstream master branch
```
# fetch the latest changes
git fetch --all
git branch -u upstream/master master
```

##Creating a branch

Now that our master branch is pointing at upstream/master, we can create a branch with
the following command:
```
#Create a branch
git branch <branch_name>

#Switch to created branch
git checkout <branch_name>

#Do both of these actions at the same time
git checkout -b <branch_name>
```

#Commit a change to the repo

Open up the 'contributors' file and add your name to the file. Now lets commit
our changes.
```
git commit -a
```

Your default editor should open up at this time. Create a commit message. You
can do this in one command using "-m" with git commit
```
git commit -a -m"this is a commit message"
```

##Commiting a new file

First create a new file
```
touch <file_name>
```

Now, Stage the new file to be committed
```
git add <file_name>
```

Finally, commit the file
```
git commit -a -m"added a new file"
```

##Amending a commit

Make a change to one of the files in the repo. Now add the change to the
latest commit with the following command:
```
git commit -a --amend
```

##Pushing changes to Github

Once the changes are ready to be merged into the master branch of the main
project's repo,  Push your local branch to the origin of your fork

```
git push origin <branch_name>
```

##Creating a Pull Request

We can create a pull request in Github from the main repository. Pull requests are used for code review
before we merge new changes into the master branch of the main repository. 
