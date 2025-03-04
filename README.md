# Git-Advanced-Exercises
## Part 1: Refining Git History
### 1.Missing  file fix: 
```bash
Run git status and git log to assess the current state of your repository.
From the status you will see that you forgot to add test4.md in the last commit.
Challenge: Recover from this error by staging/adding test4.md and amending the commit message with an appropriate description. 
# SOLUTION 
$ git add test4.md

USER@DESKTOP-0LNSN88 MINGW32 ~/Desktop/Git-advanced (main)
$ git commit --amend -m"chore: create third and fourth files"
[main fee1cc0] chore: create third and fourth files
 Date: Mon Mar 3 15:31:14 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md

USER@DESKTOP-0LNSN88 MINGW32 ~/Desktop/Git-advanced (main)
$ git add .
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it

USER@DESKTOP-0LNSN88 MINGW32 ~/Desktop/Git-advanced (main)
$ git commit -m
error: switch `m' requires a value

USER@DESKTOP-0LNSN88 MINGW32 ~/Desktop/Git-advanced (main)
$ git commit -m "commit README"
[main 13b6c29] commit README
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

USER@DESKTOP-0LNSN88 MINGW32 ~/Desktop/Git-advanced (main)
$ git push
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 4 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (10/10), 877 bytes | 73.00 KiB/s, done.
Total 10 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
```
### 2.Editing Commit History:
```bash
Editing Commit History:

It's crucial to maintain accurate commit messages. Modify the message from "Create another file" to "Create second file".
Challenge: Utilize interactive rebasing (git rebase -i HEAD~2) to edit the commit message and ensure clarity. learn more about git rebase here

# SOLUTIONG
USER@DESKTOP-0LNSN88 MINGW32 ~/Desktop/Git-advanced (main)
$ git rebase -i HEAD~4
[detached HEAD e92e995] chore: Create second  file
 Date: Mon Mar 3 15:31:08 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.

USER@DESKTOP-0LNSN88 MINGW32 ~/Desktop/Git-advanced (main)
$ git log --oneline
9fe7de0 (HEAD -> main)  modify README.md
a817247 commit README
9b7fc82 chore: create third and fourth files
e92e995 chore: Create second  file
a7f6e35 chore: Create initial file
```

### 2.Keeping History Tidy - Squashing Commitst:
```bash
Squashing combines multiple commits into a single one. Let's merge "Create second file" into "Create initial file" for a cleaner history.
Challenge: Use interactive rebasing with the squash command to achieve this. learn more about squash here
# SOLUTION


```

