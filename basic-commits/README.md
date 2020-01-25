# Git Kata: Basic Commits
This kata will introduce you to the `git add` and `git commit` commands.

This is a very introductory kata. if you have used `git status`, `git log --oneline --graph`, `git add` and `git commit` extensively you should probably skip it.

You can look at the bottom of this file, if you have not yet done basic git configuration.

## Setup:

1. Run `. setup.sh` (or `.\setup.ps1` in PowerShell)

## The task

1. Use `git status` to see which branch you are on.
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

2. What does `git log` look like?
fatal: your current branch 'master' does not have any commits yet

3. Create a file
4. What does the output from `git status` look like now?
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        file.txt

5. `add` the file to the staging area
6. How does `git status` look now?
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   file.txt

7. `commit` the file to the repository
$ git commit -m "setp 7"
[master (root-commit) 16833b7] setp 7
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 file.txt

8. How does `git status` look now?
$ git status
On branch master
nothing to commit, working tree clean

9. Change the content of the file you created earlier
10. What does `git status` look like now?
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   file.txt

11. `add` the file change
12. What does `git status` look like now?
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   file.txt


13. Change the file again
14. Make a `commit`
$ git commit -m "setp 14"
[master b1a8be0] setp 14
 1 file changed, 1 insertion(+)

15. What does the `status` look like now? The `log`?
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   file.txt

$ git log
commit b1a8be0e44adf31ff97d08289f8c4d9f83bdce8d (HEAD -> master)
Author: pasuco-podelo <56372512+pasuco-podelo@users.noreply.github.com>
Date:   Fri Jan 24 21:38:23 2020 -0800

    setp 14

16. Commit the newest change
$ git commit -m "step 16"
[master 3586c40] step 16
 1 file changed, 1 insertion(+), 1 deletion(-)

## Useful commands
- `git add`
- `git commit`
- `git commit -m "My commit message"`
- `git log`
- `git log -n 5`
- `git log --oneline`
- `git log --oneline --graph`
- `touch filename` to create a file (or `sc filename ''` in PowerShell)
- `echo content > file` to overwrite file with content (or `sc filename 'content'` in PowerShell)
- `echo content >> file` to append file with content (or `ac filename 'content'` in PowerShell)


## Git Initial Configuration
1. `git config --global user.name "John Doe"`
1. `git config --global user.email "johndoe@example.com`

For the vim scared:
- `git config --global core.editor nano`

For the windows peeps:
- `git config --global core.editor notepad`

Other editor options:
- `git config --global core.editor "atom --wait"`
- `git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst"`
