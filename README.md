# Gym-Git-Exercise-Solutions

## Bundle 1

### Exercise 1

1. Create a project folder & initialize git

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

