## Git_Commands
list of git commands and functions 

# BASICS (Setup & Configuration)
git --version	Shows the installed Git version.
git config --global user.name "Your Name"	Sets your global username.
git config --global user.email "your@email.com"	Sets your global email for commits.
git config --list	Displays all current Git configurations.
git help <command>	Shows help information for a command.

# REPOSITORY CREATION
git init	Initializes a new local Git repository in the current directory.
git clone <repo_url>	Clones (downloads) a remote repository to your local system.

# STAGING & SNAPSHOTS
git status	Displays the current state of the working directory and staging area.
git add <file>	Adds a specific file to the staging area.
git add .	Adds all changes (new, modified, deleted files) to the staging area.
git reset <file>	Unstages a file (removes it from the staging area).
git diff	Shows the difference between your working directory and the staging area.
git diff --staged	Shows the difference between the staging area and the last commit.
git commit -m "message"	Commits staged changes with a descriptive message.
git commit -am "message"	Adds and commits all tracked files in one step.

# BRANCHING & MERGING
git branch	Lists all branches in the repository.
git branch <branch_name>	Creates a new branch.
git checkout <branch_name>	Switches to a different branch.
git switch <branch_name>	Alternative to checkout for switching branches.
git checkout -b <branch_name>	Creates and switches to a new branch.
git merge <branch_name>	Merges the specified branch into the current branch.
git branch -d <branch_name>	Deletes a branch that has been merged.
git branch -D <branch_name>	Force-deletes a branch (even if not merged).
git log --oneline --graph --decorate --all	Displays all branches visually with commit history.

# REMOTE REPOSITORIES
git remote	Lists remote connections.
git remote -v	Shows remote URLs.
git remote add origin <url>	Adds a remote repository (commonly named “origin”).
git remote remove <name>	Removes a remote connection.
git fetch	Downloads changes from a remote repository without merging.
git pull	Fetches and merges changes from the remote repository into your current branch.
git push	Uploads local commits to a remote repository.
git push origin <branch>	Pushes a specific branch to the remote.
git push -u origin <branch>	Sets the upstream tracking branch (for first push).
git push origin --delete <branch>	Deletes a remote branch.

# UNDOING CHANGES
it restore <file>	Restores a file from the last commit (undoes changes in working directory).
git restore --staged <file>	Unstages a file but keeps changes in working directory.
git reset --soft HEAD~1	Undoes last commit but keeps changes staged.
git reset --mixed HEAD~1	Undoes last commit and unstages changes.
git reset --hard HEAD~1	Completely removes last commit and changes.
git revert <commit_id>	Creates a new commit that reverses a specific commit.
git clean -fd	Deletes untracked files and directories.

# INSPECTING HISTORY
git log	Shows commit history.
git log --oneline	Displays compact commit history.
git show <commit_id>	Shows details about a specific commit.
git blame <file>	Shows who changed each line in a file.
git reflog	Shows all actions done in the repository (useful for recovery).

# STASHING
git stash	Saves current changes temporarily (cleaning working directory).
git stash list	Lists all stashed changes.
git stash apply	Applies last stashed changes without deleting them.
git stash pop	Applies and removes the most recent stash.
git stash drop	Deletes a specific stash.

# TAGGING
git tag	Lists all tags.
git tag <tag_name>	Creates a lightweight tag.
git tag -a <tag_name> -m "message"	Creates an annotated tag.
git show <tag_name>	Displays tag details.
git push origin <tag_name>	Pushes a tag to remote.
git push origin --tags	Pushes all tags to remote.

# ADVANCED / MISCELLANEOUS
git cherry-pick <commit_id>	Applies a specific commit from another branch.
git rebase <branch>	Reapplies commits on top of another branch (cleaner history).
git bisect	Helps find which commit introduced a bug.
git archive	Creates a zip or tar archive of a specific commit or branch.
git submodule add <url>	Adds a submodule (another repo inside a repo).
git gc	Cleans up unnecessary files and optimizes local repo.

# .GITIGNORE
.gitignore    A file listing patterns of files/folders Git should ignore.
