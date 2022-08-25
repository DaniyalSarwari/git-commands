
## Short introduction

Git is a distributed Version Control System  VCS tool used to versioning, collaboration of a project

## Some usefull git commands

 - `git init`                           // This command initialize folder as a git repository
 - `git status`                         // check current status including in which branch currently the HEAD pointing to and the information of changes to be staged
 - `git add .`                          // start tracking changes in all the files (add to staging area)
 - `git add [filename]`                 // only add specific file to staging area
 - `git commit -m "[message]"`          // commit to local repository
 - `git push`                           // push changes to the remote repository
 - `git pull`                           // pull change from the remote repository
 - `git reset`                          // reset from staged to unstage
 - `git reset --hard`                   // reset from staged to unstaged also remove modifications
 - `git log`                            // check the history of commits
 - `git log [branch-name-1..branch-name-2]` //display difference of commits *(commits that are in "branch-name-2" but not in "branch-name-1")*

## Branches in git

To work in a same repository but in different context/module/features in a team or even individually then creating branches are helpful. Each git repository contains at least the one branch master/main. 

- `git branch` OR `git branch --list`   // display a list of branches
- `git branch -v`                       // display a list of branches with additional detail
- `git branch [branch-name]`            //create new branch 
- `git checkout [branch-name]`          //switch branch
- `git branch --delete [branch-name]`   //delete branch
- `git merge [branch-name]`             //merge changes of **(branch-name)** into the working/active branch

## Additional Commands

- `git config --global user.name "[username]"` // setup username
- `git config --global user.name`              // display the setuped username
- `git config --global user.email "[email]"`   //setup email
- `git config --global user.email`             //display the setuped username

## Conflict in git

conflict happens when you try to merge two branches and changes occur at same file on the same line.
To resolve conflict you must review it to keep both changes or changes of any specific branch, the easy way to the change through UI tool.

## Stash in git

To save changes temporarily if you don't want to commit.

- `git stash` OR `git stash save [provide-name]` // save changes temporarily to clipboard
- `git stash list`                               // show list of available stash
- `git stash apply [stash-name]`                 // apply the stash and keep that in the stash list **e.g git stash apply stash@{0}** *(here stash-name is not the name that you suggest to save)*
- `git stash clear`                              // clear all the stashes
- `git stash pop`                                // pop the last stash from list *(also remove from stash list)*
- `git stash drop [stash-name]`                  // drop and remove the stash **(e.g git stash drop stash@{0})**