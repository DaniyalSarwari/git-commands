
## Short introduction

Git is a distributed Version Control System  VCS tool used to versioning, collaboration of a project

## Some usefull git commands

 - `git init`                           // This command initialize folder as a git repository
 - `git status`                         // check current status including in which branch currently the HEAD pointing to and the information of changes to be staged
 - `git add .`                          // start tracking changes in all the files (add to staging area)
 - `git commit -m "[message]"`          // commit to local repository
 - `git reset`                          //reset from staged to unstage
 - `git reset --hard`                   // reset from staged to unstaged also remove modifications
 - `git log`                            // check the history of commits
 - `git log [branch-name..branch-name]` //display difference of commits (from..to)

## Commands for branches

- `git branch`                          // display a list of branches
- `git branch -v`                       // display a list of branches with additional detail
- `git branch [branch-name]`            //create new branch 
- `git branch --delete [branch-name]`   //delete branch

## Additional Commands

- `git config --global user.name "[username]"` // setup username
- `git config --global user.name`              // display the setuped username
- `git config --global user.email "[email]"`   //setup email
- `git config --global user.email`             //display the setuped username