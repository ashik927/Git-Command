Getting & Creating Projects

git init   =>	  Initialize a local Git repository
git clone   =>	   ssh://git@github.com/[username]/[repository-name].git	Create a local copy of a remote repository


Basic Snapshotting

git status   =>	  	Check status
git add [file-name.txt]   =>	  	Add a file to the staging area
git add -A   =>	  	Add all new and changed files to the staging area
git commit -m "[commit message]"   =>	  	Commit changes
git rm -r [file-name.txt]   =>	  	Remove a file (or folder)
git clean   =>	  	Removes untracked files from the working directory. This is the logical counterpart to git reset, which (typically) only operates on tracked files.
git commit --amend   =>	  	Passing the --amend flag to git commit lets you amend the most recent commit. This is very useful when you forget to stage a file or omit important information from the commit message.
git rebase   =>	  	Rebasing lets you move branches around, which helps you avoid unnecessary merge commits. The resulting linear history is often much easier to understand and explore.
git rebase -i   =>	  	The -i flag is used to begin an interactive rebasing session. This provides all the benefits of a normal rebase, but gives you the opportunity to add, edit, or delete commits along the way.
git reflog   =>	  	Git keeps track of updates to the tip of branches using a mechanism called reflog. This allows you to go back to changesets even though they are not referenced by any branch or tag.
git revert   =>	  	Undoes a committed snapshot. When you discover a faulty commit, reverting is a safe and easy way to completely remove it from the code base.



Branching & Merging

git branch   =>	  	List branches (the asterisk denotes the current branch)
git branch -a   =>	  	List all branches (local and remote)
git branch [branch name]   =>	  	Create a new branch
git branch -d [branch name]   =>	  	Delete a branch
git push origin --delete [branch name]   =>	  	Delete a remote branch
git checkout -b [branch name]   =>	  	Create a new branch and switch to it
git checkout -b [branch name]   =>	   origin/[branch name]	Clone a remote branch and switch to it
git branch -m [old branch name] [new branch name]   =>	  	Rename a local branch
git checkout [branch name]   =>	  	Switch to a branch
git checkout -   =>	  	Switch to the branch last checked out
git checkout -- [file-name.txt]   =>	  	Discard changes to a file
git merge [branch name]   =>	  	Merge a branch into the active branch
git merge [source branch] [target branch]   =>	  	Merge a branch into a target branch
git stash   =>	  	Stash changes in a dirty working directory
git stash clear   =>	  	Remove all stashed entries
git-reset or git merge --abort   =>	  	Use git-reset or git merge --abort to cancel a merge that had conflicts.


Sharing & Updating Projects

git push origin [branch name]   =>	  	Push a branch to your remote repository
git push -u origin [branch name]   =>	  	Push changes to remote repository (and remember the branch)
git push   =>	  	Push changes to remote repository (remembered branch)
git push origin --delete [branch name]   =>	  	Delete a remote branch
git pull   =>	  	Update local repository to the newest commit
git pull origin [branch name]   =>	  	Pull changes from remote repository
git remote add origin ssh://git@github.com/[username]/[repository-name].git   =>	  	Add a remote repository
git remote set-url origin ssh://git@github.com/[username]/[repository-name].git   =>	  	Set a repository's origin branch to SSH


Inspection & Comparison

git log   =>	  	View changes
git log --summary   =>	  	View changes (detailed)
git log --oneline   =>	  	View changes (briefly)
git diff [source branch] [target branch]   =>	  	Preview changes before merging