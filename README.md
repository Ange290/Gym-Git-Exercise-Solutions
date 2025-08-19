# Gym-Git-Exercise-Solutions

## Bundle 1

### Exercise 1



```bash

User@ANGE-LAPTOP2 MINGW64 ~/Documents (main)
$ mkdir Exercise1

User@ANGE-LAPTOP2 MINGW64 ~/Documents (main)
$ cd Exercise1/

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git init
Initialized empty Git repository in C:/Users/User/Documents/Exercise1/.git/

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (master)
$ git branch -m main

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git commit -m "Add new file"
[main (root-commit) 0f3bbc1] Add new file
 1 file changed, 3 insertions(+)
 create mode 100644 README.md

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git remote add origin https://github.com/Ange290/Exercise1.git
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 251 bytes | 251.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Ange290/Exercise1.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git checkout -b dev
Switched to a new branch 'dev'

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git push origin main
Everything up-to-date

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git branch
* dev
  main

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git push -u origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Ange290/Exercise1/pull/new/dev
remote:
To https://github.com/Ange290/Exercise1.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git checkout -b test
Switched to a new branch 'test'

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (test)
$ git branch
  dev
  main
* test

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (test)
$ git checkout dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git  branch -d test
Deleted branch test (was 0f3bbc1).

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git branch
* dev
  main

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git push origin dev
Everything up-to-date

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ ^C

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$


```
### Exercise 2

```bash
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git stash -m "Add home file"
Saved working directory and index state On dev: Add home file

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git stash list
stash@{0}: On dev: Add home file

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git stash -m "Add about file"
Saved working directory and index state On dev: Add about file

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git stash list
stash@{0}: On dev: Add about file
stash@{1}: On dev: Add home file

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git stash -m "Add team file"
Saved working directory and index state On dev: Add team file

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git stash list
stash@{0}: On dev: Add team file
stash@{1}: On dev: Add about file
stash@{2}: On dev: Add home file

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (df8548843faa95b5bae974e24621a87175ac0a07)

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git stash list
stash@{0}: On dev: Add team file
stash@{1}: On dev: Add home file

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (3080d4177c3f6bab9d2a5a0ec98763376c89fa51)

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html


User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git commit -m "Create two file home, about"
[dev 8289cd2] Create two file home, about
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 519 bytes | 519.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Ange290/Exercise1.git
   6f3519e..8289cd2  dev -> dev

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git stash list
stash@{0}: On dev: Add team file

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (f37d6b88d24b983bce1facbfa6bdf7886e2972f7)

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git reset --hard
HEAD is now at 8289cd2 Create two file home, about

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$

```

## Bundle 2

### Exercise 1

```bash
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git branch
* dev
  main

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/bundle-2)
$ git branch
  dev
* ft/bundle-2
  main

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/bundle-2)
$ git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        service.html

nothing added to commit but untracked files present (use "git add" to track)

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/bundle-2)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/bundle-2)
$ git commit -m "Create service file"
[ft/bundle-2 d0a5d1d] Create service file
 1 file changed, 11 insertions(+)
 create mode 100644 service.html

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 440 bytes | 440.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Ange290/Exercise1/pull/new/ft/bundle-2
remote:
To https://github.com/Ange290/Exercise1.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/bundle-2)
$
```
