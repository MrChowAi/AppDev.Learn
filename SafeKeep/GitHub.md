Here are the essential Git commands you'll use, with plain English descriptions.

Setup & Configuration
Command	What it does
git init	Creates a new Git repository in your current folder
git config --global user.name "Your Name"	Sets your name for commits
git config --global user.email "you@email.com"	Sets your email for commits
Working with Files
Command	What it does
git status	Shows which files are changed, staged, or untracked
git add <file>	Stages a specific file (prepares it for commit)
git add .	Stages all changed files in current folder
git add --all	Stages all changed files in entire repository
git reset <file>	Unstages a file (removes it from staging)
git reset	Unstages all files
git rm --cached <file>	Removes a file from Git but keeps it on your computer
Committing (Saving Snapshots)
Command	What it does
git commit -m "message"	Saves staged changes with a description
git commit --amend	Changes the last commit (adds files or fixes message)
Branching
Command	What it does
git branch	Lists all branches (shows current with *)
git branch <name>	Creates a new branch
git branch -d <name>	Deletes a branch
git branch -M <name>	Renames current branch
git checkout <branch>	Switches to a different branch
git checkout -b <branch>	Creates and switches to a new branch
git merge <branch>	Merges another branch into current branch
Remote (GitHub)
Command	What it does
git remote add origin <url>	Connects local repo to GitHub
git remote remove origin	Removes the connection to GitHub
git remote -v	Shows connected GitHub URLs
git push -u origin main	Pushes commits to GitHub (first time)
git push	Pushes commits to GitHub (after setup)
git pull	Fetches and merges changes from GitHub
git fetch	Downloads changes from GitHub without merging
git clone <url>	Copies a GitHub repo to your computer
History & Viewing
Command	What it does
git log	Shows commit history
git log --oneline	Shows commit history (one line per commit)
git diff	Shows unstaged changes (not yet added)
git diff --staged	Shows staged changes (ready to commit)
git show <commit-hash>	Shows what changed in a specific commit
Undoing Things
Command	What it does
git restore <file>	Discards changes to a file (reverts to last commit)
git restore --staged <file>	Unstages a file (keeps changes)
git reset --soft HEAD~1	Undoes last commit but keeps changes staged
git reset --mixed HEAD~1	Undoes last commit but keeps changes unstaged
git reset --hard HEAD~1	Undoes last commit and deletes changes (⚠️ permanent)
git clean -fd	Deletes untracked files and folders (⚠️ permanent)
Cleanup & Removal
Command	What it does
Remove-Item -Recurse -Force .git	Deletes Git entirely (PowerShell)
rm -rf .git	Deletes Git entirely (Mac/Linux)