![Logo](git-logo.jpg)
# Working with Git and GitHub
## 1. Checking the existance of Git
Type in terminal `git version`
If Git is installed, the message will show the version of the Git. 
Othewise it ruturn the error.
## 2. Git installation
Load the latest version of Git from the site (git-scm.com/downloads).
Install it with the default settings.
## 3. Git configuration
When you launch Git the first time, you need to introduce yourself by typing 2 following lines:
```
git config --global user.name "Your name"
git config --global user.email "Your email"
```
## 4. Initializing repository
In the terminal, navigate to the folder where we want to create the repository.
And run the command:
```
git init
```
## 5. Commiting the changes in the repository
After modifying some file(s), use this command to stage the changes you want to include in the commit:
```
git add <file>
```
To add all modified files:
```
git add .
```
Once changes are stages, they are ready to be committed.
To create a new commit with the staged changes, run the following command:
```
git commit -m "Commit message"
```
## 6. Checking the logs of the commits
To view the commit history and logs, run this command:
```
git log
git log --oneline
```
## 7. Switching between the commits
After you obtained the commit hash of the desired commit by checking the logs, run the following command:
```
git checkout <commit-hash>
```
In order to switch to the latest of your master branch, run:
```
git checkout master
```
## 8. Files ignoring
To exclude some files or directories from being tracked in a repository, you need to create a file called ***.gitignore*** and list the names or patterns of those filed or directories in it.
## 9. Creating Git branches
By default, the main branch name in Git - *master*.
To create a new branch, type the command:
```
git branch <branch_name>
```
List of branches in the repository can be viewed with the command:
```
git branch
```
The current branch will be marked with an asterisk: **\*master**

## 10. Branch merging and conflict solving
To merge the desired branch with the current branch:
```
git merge <branch_name>
```
If the same part of the file has been changed in both branches, then a conflict might apper that will require an aciton from the user.
VSCode suggests a few solving options.
In order to solve the conflict, you either need to choose one of the options, or resolve the conflict on your own.
After solving the conflict, you need to commit the merge.

## 11. Branch deletion
To delete a branch you need to move to a different branch, merge the changes for the branch you want to delte and type the command:
```
git branch -d <branch_name>
```
If you want to delte the brange without merging changes from it, use this:
```
git branch -D <branch_name>
```

## 12. Connecting local repository to remote repository
1) You need to create a local repostiry first.
2) Then you need to create a remote repository.
3) After that you need to "befriend your local and remote repositories, by tying this command:
```
git remote add origin <link>
```
4) Create the upstream branch on your remote repostiroy and push the changes from your local repositroy to that branch:
```
git push --set-upstream origin <branch name>
git push -u -origin <branch name>
```
origin = <remote repository name>

## 13. To fetch and merge changes from a remote repositrory into your local branch, use this command:
```
git pull origin <remote branch name>
git pull
```

## 14. To see connected remote repositories:
```
git remote
git remote -v
```

## 15. To create a copy of an existing remote repository on your local machine:
```
git clone <link>
```

