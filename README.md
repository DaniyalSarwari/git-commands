
## Short introduction

Git is a distributed Version Control System  VCS tool used to versioning, collaboration of a project

## Some usefull git commands

 - `git init`                           // This command initialize folder as a git repository
 - `git status`                         // check current status including in which branch currently the HEAD pointing to and the information of changes to be staged
 - `git add .`                          // start tracking changes in all the files (add to staging area)
 - `git add [filename]`                 // only add specific file to staging area
 - `git reset`                          // reset from staged to unstage
 - `git reset --hard`                   // reset from staged to unstaged also remove modifications
 - `git commit -m "[message]"`          // commit to local repository
 - `git push`                           // push changes to the upstream remote repository (best practice is to use local repo name and branch name **e.g git push origin main**)
 - `git fetch`                          // fetch the changes from remote repository but not merge with local repository.
 - `git merge`                          // merge the fetched changes *(from command **git fetch**)* to local 
repository.
 - `git pull`                           // fetch and merge the changes from the upstream remote to local repository (best practice is to use local repo name and branch name **e.g git pull origin main**)
 - `git branch -M [branch-name]`        // change active/working branch name **e.g git branch -M main**
 - `git remote add [set-repo-name] [url]`   // connect local repo to remote repo **e.g git remote add origin (link)**
 - `git remote -v`                      // show the remotely connected repo url to local repo
 - `git push -u [repo-name] [branch-name]` // push all local commits to specific branch of remote repo *(here -u flag create upstream so that to use only git push command without mentioning repo/branch name worth noting that here (repo-name) is not the actual name of remote repo)*
 - `git remote show`                    // display the locel name of connected repo
 - `git remote show [repo-name]`        // show the status of remote repo **e.g git remote show origin**

## Branches in git

To work in a same repository but in different context/module/features in a team or even individually then creating branches are helpful. Each git repository contains at least the one branch master/main. 

- `git branch` OR `git branch --list`   // display a list of branches
- `git branch -v`                       // display a list of branches with additional detail
- `git branch [branch-name]`            //create new branch 
- `git checkout [branch-name]`          //switch branch
- `git branch --delete [branch-name]`   //delete branch
- `git merge [branch-name]`             //merge changes of **(branch-name)** into the working/active branch

#### Short live / Long live Branches

In short live branches where we need to work on a small task of specific feature where we complete task merge into other branch and remove that branch.
In Long live branches *e.g production, development, testing etc* these branches use in lon run. 

## Additional Commands

- `git config --global user.name "[username]"` // setup username
- `git config --global user.name`              // display the setuped username
- `git config --global user.email "[email]"`   // setup email
- `git config --global user.email`             // display the setuped username
- `git log`                                    // check the history of commits
- `git log [branch-name-1..branch-name-2]`     // display difference of commits *(commits that are in "branch-name-2" but not in "branch-name-1")*
- `git log [repo-name]/[branch-name]`          // display commit history of specific branch of remote repo

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