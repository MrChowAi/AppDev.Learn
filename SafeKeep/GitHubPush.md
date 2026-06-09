Full Workflow Summary
Step	Command	What it does
1	git status	See what changed
2	git add .	Stage all changes
3	git commit -m "message"	Save snapshot
4	git push	Send to GitHub


Full Guidance.

1. Check what changed
- git status 
his shows: "untracked file: test.txt" (Git sees it but isn't tracking it yet)

2. Stage the file (add to the "to be committed" box)
- git add test.txt
  or to stage all changed files:
- git add .
    Now git status will show "Changes to be committed"

3. Commit the file (save a snapshot)
- git commit -m "..." "Add test.txt file"
    The -m means "message" — always write what you changed, Message as to be in quotes ""

4. Push to GitHub
- git push
Now your file is live on GitHub.


