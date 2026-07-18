# Git Commands

Useful git commands to start journey with git and github.


## Starter
* `git config --global user.name "[YOUR_NAME]"` : Set your user name.
* `git config --global user.email "[YOUR_EMAIL]"` : Set your email.
* `git config --global core.editor "code --wait"` : Sets vs code as default editor for git.

## Utility
* `git init` : Marks the current directory as a git repo.
* `git status` : Checks status of current repo.
* `.gitignore` : Files and folders mentioned inside this file will be ignored by git.
* `git restore` :
    * `git restore [FILE_NAME]` : Restores all the progress for the file to the last commit.
    * `git restore .` : Restores all the progress to the last commit.
* `git checkout [COMMIT_ID]` : Takes to the mentioned commit state.
* `git checkout HEAD~[n]` : Takes n steps back from the head.
* `git checkout [BRANCH_NAME]` : Takes to last commit of the mentioned branch.

## Commit
* `git add` :
    * `git add [FILE-1_NAME] [FILE-2_NAME] ...` : Adds particular file or files to staging area.
    * `git add .` : Adds all files to staging area.
* `git commit -m "[YOUR_MESSAGE]"` : Create commits with given message.
* `git commit -am "[YOUR_MESSAGE]"` : Adds all files to the staging area and commits at the same time.
* `git log` : Gives all the details about previous commits.
* `git log --oneline` : Gives short details about previous commits.

## Branch
* `git branch` : Shows all the branches.
* `git branch [BRANCH_NAME]` : Creates new branch with given name.
* `git checkout [BRANCH_NAME]` : Switches the head to the mentioned branch.
* `git checkout -b [BRANCH_NAME]` : Creates a new branch with the given name and switches to it immediately.
* `git merge [BRANCH_NAME]` : Merges the mentioned branch with current branch.
* `git branch -d [BRANCH_NAME]` : Deletes the branch.
* `git rebase [BRANCH_NAME]` : Merges mentioned branch with current branch making the mentioned branch's last commit as it's base. So basically it will take the first node of the current branch, and will put it on the last node of the mentioned branch making it a linear branch that will look like it continues from where the mentioned branch finished.
    * _It's a slight risky command as it modifies the commit history so don't use it on the main/master branch._
    * _In case of conflicts first solve the conflicts manually, then use "git add file-name or ." to stage all changes and then use "git rebase --continue" to resume the process._
* `git branch -M [NEW_BRANCH_NAME]` : Updates the current name of the branch with the new name.

## Diff
* `git diff --staged` : Shows the difference between staged files and last committed files.
* `git diff [COMMIT_ID-1] [COMMIT_ID-2]` : Shows the difference between two given commit ids.
* `git diff [BRANCH-1] [BRANCH-2]` : Shows the difference between two given branches.

## Stash
* `git stash` : Stores your current in progress works in stash (it's branch independent).
* `git stash pop` : Takes out all the stashed progress into the current branch.
* `git stash list` : Shows all the stashed progress.
* `git stash apply [STASH_ID]` : Gives the stashed progress for the given stash-id.

## Remote
* `git remote -v` : Shows all remote configs.
* `git remote add [REMOTE_NAME] [url]` : Creates connection between your local project and github repo.
* `git remote rename [OLD_NAME] [NEW_NAME]` : Changes the remote name.
* `git remote remove [REMOTE_NAME]` : Deletes the remote name.
* `git push [REMOTE_NAME] [BRANCH_NAME]` : Pushes code of current branch to remote.
* `git push -u [REMOTE_NAME] [BRANCH_NAME]` : Pushes code of current branch to remote and sets upstream at the same time. The advantage of the upstream is from the next time can just write "git push" to push changes on remote without mentioning the remote_name and branch_name repeatedly, it will automatically push current branches code to remote. And second advantage is when one will use "git status" command, it will also compare local commits with remote.
* `git clone [url]` : Clones a repo.
* `git fetch [REMOTE]` : Downloads the latest changes from a remote repository but does not integrate them into your current working branch.
* `git pull [REMOTE] [BRANCH]` : Fetches changes from the remote repository and merges them into the current branch.

---

> Replace all the **[TEXTS]** with your own values.
