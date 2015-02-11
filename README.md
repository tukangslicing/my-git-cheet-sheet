#### Create Branch

     $ git checkout -b [name_of_your_new_branch]

#### Create a new tracking branch based on a remote branch
     $ git branch --track [new_branch] [remote-branch]

#### Show local branch
     $ git branch [name_of_your_new_branch]

#### Show url repo
     $ git remote show origin 

#### Show remote branch
     $ git branch -a

#### Checkout local branch
     $ git checkout [branch_name]

#### Checkout remote branch
     $ git checkout -b [branch_name] origin/[branch_name]

#### Delete local branch
     $ git branch -d [branch_name]  (to force using -D)

#### Delete remote branch
     $ git push origin :[branch_name]
     
#### Cleaning Old Local Branches With Git  (delete at once all local branches that have already been merged to master)   
     $ git branch --merged | grep -v "\*" | xargs -n 1 git branch -d

#### To see the last commit on each branch
     $ git branch -v

#### Add all tracked files
     $ git add -u

#### Rever file (changes file)    
     $ git chechout -- <file_path>

#### View a file in another branch
     $ git show branch:<file_path>

#### Commit
     $ git commit -am "[commit_message]"
     $ git commit -a (with multi line message)

#### Push
     $ git push origin [branch_name]

#### Log
     $ git log
     $ git log -3
     $ git log -since=yesterday


#### Merge branch "test_branch" into the current branch, but do not make a new commit automatically
     $ git merge --no-commit test_branch

#### Merge a large set of commits on a dev branch into master as one commit ("squash" commit):
     $ git merge [working_branch_name] --squash

#### Get the changes that have happened to master branch since I made my working branch:
     $ git rebase master    

#### Temporarily clear my stage so I can switch to another branch ("stashing"):
     $ git stash

#### Get my stashed stuff back:
     $ git stash apply    

#### How can I git stash a specific file?
     $ git add <file_path>
     $ git stash --keep-index
     $ git reset
**Last step is optional, but usually you want it. It removes changes from index.**
    

#### Rebase your current HEAD onto <branch>. Don‘t rebase published commits!
     $ git rebase [branch_name]

#### Abort a rebase
     $ git rebase --abort    
 
 
#### what "git remote prune" ?

When you use 

     $ git push origin :staleStuff
     
it automatically removes 

     origin/staleStuff
     
so when you ran 

     git remote prune origin

you have pruned some branch that was removed by someone else. It’s more likely that your co-workers now need to run 

     git prune

to get rid of branches you have removed.

#### How do I make Git ignore file mode (chmod) changes?

     $ git config core.fileMode false
     
check [resource](http://stackoverflow.com/questions/1580596/how-do-i-make-git-ignore-file-mode-chmod-changes)
