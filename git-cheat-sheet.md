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
     $ git check -b [branch_name] origin/[branch_name]

#### Delete local branch
     $ git branch -d [branch_name]  (to force using -D)

#### Delete remote branch
     $ git push origin :[branch_name]

#### To see the last commit on each branch
     $ git branch -v

#### Add all tracked files
     $ git add -u

#### Rever file (changes file)    
     $ git chechout -- <file_path>

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

#### Rebase your current HEAD onto <branch>. Don‘t rebase published commits!
     $ git rebase [branch_name]

#### Abort a rebase
     $ git rebase --abort    
