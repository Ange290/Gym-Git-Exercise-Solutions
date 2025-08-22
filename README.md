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
### Exercise 2

```bash
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git branch
  dev
  ft/bundle-2
  ft/service-redesign
* main

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/service-redesign)
$ git merge main
Auto-merging service.html
CONFLICT (content): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/service-redesign)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/service-redesign)
$ git commit -m "resolve conflicts"
On branch ft/service-redesign
nothing to commit, working tree clean

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 406 bytes | 406.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Ange290/Exercise1.git
   0a359ba..89dc05a  ft/service-redesign -> ft/service-redesign

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/service-redesign)
$

```

## Bundle 3
### Exercise 2

```bash
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/service-redesign)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/team-page)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/team-page)
$ git commit -m "Creating team page"
[ft/team-page 1aa03ee] Creating team page
 1 file changed, 18 insertions(+)
 create mode 100644 team.html

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 506 bytes | 506.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Ange290/Exercise1/pull/new/ft/team-page
remote:
To https://github.com/Ange290/Exercise1.git
 * [new branch]      ft/team-page -> ft/team-page

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 3 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/team-page)
$ git log
commit 1aa03ee7314733fa106b2bf1c2bb984d810260d1 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Ange290 <uange209@gmail.com>
Date:   Wed Aug 20 11:30:39 2025 +0200

    Creating team page

commit 89dc05a6a2a4334a68b564311b32f7fe344aea00 (origin/ft/service-redesign, ft/service-redesign)
Merge: 0a359ba 950314d
Author: Ange290 <uange209@gmail.com>
Date:   Wed Aug 20 11:01:59 2025 +0200
:
commit 1aa03ee7314733fa106b2bf1c2bb984d810260d1 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Ange290 <uange209@gmail.com>
Date:   Wed Aug 20 11:30:39 2025 +0200

    Creating team page

commit 89dc05a6a2a4334a68b564311b32f7fe344aea00 (origin/ft/service-redesign, ft/service-redesign)
Merge: 0a359ba 950314d
Author: Ange290 <uange209@gmail.com>
Date:   Wed Aug 20 11:01:59 2025 +0200

:
Author: Ange290 <uange209@gmail.com>
Date:   Wed Aug 20 11:30:39 2025 +0200

    Creating team page

commit 89dc05a6a2a4334a68b564311b32f7fe344aea00 (origin/ft/service-redesign, ft/service-redesign)
Merge: 0a359ba 950314d
Author: Ange290 <uange209@gmail.com>
Date:   Wed Aug 20 11:01:59 2025 +0200

    Merge branch 'main' into ft/service-redesign


User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/contact-page)
$ git cherry-pick 1aa03ee7314733fa106b2bf1c2bb984d810260d1
[ft/contact-page 1018857] Creating team page
 Date: Wed Aug 20 11:30:39 2025 +0200
 1 file changed, 18 insertions(+)
 create mode 100644 team.html 
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/contact-page)    
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/contact-page)    
$ git commit -m "Add changes in contact file"
[ft/contact-page 248ca75] Add changes in contact file
 1 file changed, 1 insertion(+)

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/contact-page)    
$ git push origin ft/contact-page
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 328 bytes | 328.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)        
remote: Resolving deltas: 100% (2/2), completed with 2 local objects 
To https://github.com/Ange290/Exercise1.git
   0561152..248ca75  ft/contact-page -> ft/contact-page

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/faq-page)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/faq-page)
$ git commit -m "add faq file"
[ft/faq-page 23d7162] add faq file
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads    
Compressing objects: 100% (3/3), done.      
Writing objects: 100% (3/3), 419 bytes | 419.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Ange290/Exercise1.git 
   201edae..23d7162  ft/faq-page -> ft/faq-page

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/faq-page)
$ git status
23d7162 (HEAD -> ft/faq-page, origin/ft/faq-page) add faq file
0751d0a (origin/ft/contact-page, ft/contact-page) add
6f9bed6 add
f3f012c Add changes
1a1a09d (main) merge
248ca75 Add changes in contact file
b4e4456 Delete files
4ac31eb Merge pull request #6 from Ange290/ft/team-page
82afcd1 (origin/ft/team-page, ft/team-page) Reapply "Creating team page"
224cf70 Merge pull request #5 from Ange290/ft/faq-page
:
23d7162 (HEAD -> ft/faq-page, origin/ft/faq-page) add faq file
0751d0a (origin/ft/contact-page, ft/contact-page) add
6f9bed6 add
f3f012c Add changes
1a1a09d (main) merge
248ca75 Add changes in contact file       
b4e4456 Delete files
4ac31eb Merge pull request #6 from Ange290/ft/team-page
82afcd1 (origin/ft/team-page, ft/team-page) Reapply "Creating team page"
224cf70 Merge pull request #5 from Ange290/ft/faq-page
ef74ef5 Add changes
bade97d Revert "Creating team page"       
23d7162 (HEAD -> ft/faq-page, origin/ft/faq-page) add faq file
0751d0a (origin/ft/contact-page, ft/contact-page) add
6f9bed6 add
f3f012c Add changes
1a1a09d (main) merge
248ca75 Add changes in contact file
b4e4456 Delete files
4ac31eb Merge pull request #6 from Ange290/ft/team-page
82afcd1 (origin/ft/team-page, ft/team-page) Reapply "Creating team page"
224cf70 Merge pull request #5 from Ange290/ft/faq-page
:
23d7162 (HEAD -> ft/faq-page, origin/ft/faq-page) add faq file
0751d0a (origin/ft/contact-page, ft/contact-page) add
6f9bed6 add
f3f012c Add changes
1a1a09d (main) merge
248ca75 Add changes in contact file       
b4e4456 Delete files
4ac31eb Merge pull request #6 from Ange290/ft/team-page
82afcd1 (origin/ft/team-page, ft/team-page) Reapply "Creating team page"
224cf70 Merge pull request #5 from Ange290/ft/faq-page
ef74ef5 Add changes
bade97d Revert "Creating team page"       
201edae Create fag file and add  changes  
fb87349 Revert "Reapply "Create fag file and add  changes""
b4ab691 Reapply "Create fag file and add  changes"
:
23d7162 (HEAD -> ft/faq-page, origin/ft/faq-page) add faq file
0751d0a (origin/ft/contact-page, ft/contact-page) add
6f9bed6 add
f3f012c Add changes
1a1a09d (main) merge
248ca75 Add changes in contact file
b4e4456 Delete files
4ac31eb Merge pull request #6 from Ange290/ft/team-page
82afcd1 (origin/ft/team-page, ft/team-page) Reapply "Creating team page"
224cf70 Merge pull request #5 from Ange290/ft/faq-page
:
23d7162 (HEAD -> ft/faq-page, origin/ft/faq-page) add faq file
0751d0a (origin/ft/contact-page, ft/contact-page) add
6f9bed6 add
f3f012c Add changes
1a1a09d (main) merge
248ca75 Add changes in contact file
b4e4456 Delete files
4ac31eb Merge pull request #6 from Ange290/ft/team-page
82afcd1 (origin/ft/team-page, ft/team-page) Reapply "Creating team page"
224cf70 Merge pull request #5 from Ange290/ft/faq-page

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/faq-page)
$ git revert 82afcd1
hint: Waiting for your editor to close the file...
[ft/faq-page 486ad1e] Revert "Reapply "Creating team page""
 1 file changed, 18 deletions(-)
486ad1e (HEAD -> ft/faq-page) Revert "Reapply "Creating team page""
23d7162 (origin/ft/faq-page) add faq file
0751d0a (origin/ft/contact-page, ft/contact-page) add
6f9bed6 add
f3f012c Add changes
1a1a09d (main) merge
248ca75 Add changes in contact file
b4e4456 Delete files
4ac31eb Merge pull request #6 from Ange290/ft/team-page
82afcd1 (origin/ft/team-page, ft/team-page) Reapply "Creating team page"
224cf70 Merge pull request #5 from Ange290/f:
486ad1e (HEAD -> ft/faq-page) Revert "Reapply "Creating team page""
23d7162 (origin/ft/faq-page) add faq file
0751d0a (origin/ft/contact-page, ft/contact-page) add
6f9bed6 add
f3f012c Add changes
1a1a09d (main) merge
248ca75 Add changes in contact file
b4e4456 Delete files
4ac31eb Merge pull request #6 from Ange290/ft/team-page
82afcd1 (origin/ft/team-page, ft/team-page) Reapply "Creating team page"
224cf70 Merge pull request #5 from Ange290/ft/faq-page
ef74ef5 Add changes
bade97d Revert "Creating team page"
201edae Create fag file and add  changes
fb87349 Revert "Reapply "Create fag file and add  changes""

```
### Exercise 2
```bash
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git commit -m"Make changes"
[main 6a7a64e] Make changes
 1 file changed, 1 insertion(+)
 User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git push origin main
Enumerating objects: 12, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 16 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (8/8), 852 bytes | 213.00 KiB/s, done.
Total 8 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), completed with 2 local objects.
To https://github.com/Ange290/Exercise1.git
   8f094ee..bac4112  main -> main
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/home-page-redesign)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/home-page-redesign)
$ git commit -m"Make changes on home page"
[ft/home-page-redesign 1d5bb28] Make changes on home page
 1 file changed, 5 insertions(+)
 
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/home-page-redesign)
$ git push origin ft/home-page-redesign
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 16 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 788 bytes | 394.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 3 local objects.
To https://github.com/Ange290/Exercise1.git
   486ad1e..cabe33e  ft/home-page-redesign -> ft/home-page-redesign

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/home-page-redesign)
$

```
## Bundle 4

### Exercise 1

```bash
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git remote
origin
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git remote add git-copy https://github.com/Ange290/Exercise2.git

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git remote
git-copy
origin
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git commit -m"add change on homepage"
[main f95d382] add change on homepage
 1 file changed, 1 insertion(+)
 User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 306 bytes | 306.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Ange290/Exercise1.git
   9c3e311..f95d382  main -> main
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git push git-copy main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 298 bytes | 298.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Ange290/Exercise2.git
   8c9cb91..986bc59  main -> main

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$   

```

### Exercise 2
```bash
User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/footer)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/footer)
$ git commit -m"Add footer on home page"
[ft/footer b53c6e4] Add footer on home page
 1 file changed, 3 insertions(+)

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/footer)
$ git add .

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/footer)
$ git commit -m "Add new changes on home page"
[ft/footer 64d9507] Add new changes on home page
 1 file changed, 1 insertion(+)

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/footer)
$ git  push origin ft/footer
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 16 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 615 bytes | 307.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)        
remote: Resolving deltas: 100% (4/4), completed with 2 local objects 
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting: 
remote:      https://github.com/Ange290/Exercise1/pull/new/ft/footer 
remote:
To https://github.com/Ange290/Exercise1.git
 * [new branch]      ft/footer -> ft/footer

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/footer)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'git-copy/main'.

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (main)
$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/squashing)       
$ git merge squash ft/footer
merge: squash - not something we can merge

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/squashing)       
$ git merge --squash ft/footer
Updating 986bc59..64d9507
Fast-forward
Squash commit -- not updating HEAD
 home.html | 4 ++++
 1 file changed, 4 insertions(+)

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/squashing)       
$ git commit -m"footer changes squashing"
[ft/squashing cfbc1d6] footer changes squashing
 1 file changed, 4 insertions(+)

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/squashing)       
$ git push origin ft/squashing
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 372 bytes | 372.00 KiB/s, done.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/Ange290/Exercise1/pull/new/ft/squashing
remote:
To https://github.com/Ange290/Exercise1.git
 * [new branch]      ft/squashing -> ft/squashing

User@ANGE-LAPTOP2 MINGW64 ~/Documents/Exercise1 (ft/squashing)
$

```