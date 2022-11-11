# Git exercise 
## Bundle 1
```bash
Denys@Envy15X360-PC:~$ pwd
/home/Denys
Denys@Envy15X360-PC:~$ mkdir Gym_Git_Exercise_Solutions
Denys@Envy15X360-PC:~$ cd Gym_Git_Exercise_Solutions/
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ code .
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git branch -M main
fatal: not a git repository (or any of the parent directories): .git
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git init
Initialized empty Git repository in /home/Denys/Gym_Git_Exercise_Solutions/.git/
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git branch -M main
error: refname refs/heads/master not found
fatal: Branch rename failed
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ touch README.md
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git add README.md 
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git commit -m "first commit"
[master (root-commit) 7cefe68] first commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git branch -M main
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git status
On branch main
nothing to commit, working tree clean
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git remote add origin https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git push 
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 231 bytes | 231.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git checkout -b dev
Switched to a new branch 'dev'
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git checkout dev
Already on 'dev'
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git checkout -b test
Switched to a new branch 'test'
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git status
On branch test
nothing to commit, working tree clean
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git checkout dev
Switched to branch 'dev'
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git branch -D test
Deleted branch test (was 7cefe68).
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        home.html

nothing added to commit but untracked files present (use "git add" to track)
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git add --all 
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git status
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   home.html

Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash
Saved working directory and index state WIP on dev: 7cefe68 first commit
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash list
stash@{0}: WIP on dev: 7cefe68 first commit
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git add about.html 
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash
Saved working directory and index state WIP on dev: 7cefe68 first commit
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash list
stash@{0}: WIP on dev: 7cefe68 first commit
stash@{1}: WIP on dev: 7cefe68 first commit
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git add team.html 
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash
Saved working directory and index state WIP on dev: 7cefe68 first commit
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash list
stash@{0}: WIP on dev: 7cefe68 first commit
stash@{1}: WIP on dev: 7cefe68 first commit
stash@{2}: WIP on dev: 7cefe68 first commit
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash pop stash@{0}:
'stash@{0}:' is not a stash reference
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   team.html

Dropped stash@{0} (56c1ce26bbe32972d74f4a8f65185889dd66dfcb)
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ ls
README.md  team.html
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git add team.html 
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash
Saved working directory and index state WIP on dev: 7cefe68 first commit
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash list
stash@{0}: WIP on dev: 7cefe68 first commit
stash@{1}: WIP on dev: 7cefe68 first commit
stash@{2}: WIP on dev: 7cefe68 first commit
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html

Dropped stash@{1} (1f80385ba6e13a6a38361439f34746dd39183834)
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ ls
about.html  README.md
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash list
stash@{0}: WIP on dev: 7cefe68 first commit
stash@{1}: WIP on dev: 7cefe68 first commit
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ ^C
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html
        new file:   home.html

Dropped stash@{1} (47c81cbaa9f4d048ed4100d4bada90e3372bf945)
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git add -all
error: did you mean `--all` (with two dashes ?)
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git add --all
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git commit -m "2nd commit"
[dev 9c0e020] 2nd commit
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git push orgin dev
fatal: 'orgin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 536 bytes | 536.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions/pull/new/dev
remote: 
To https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git
 * [new branch]      dev -> dev
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash list
stash@{0}: WIP on dev: 7cefe68 first commit
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git stash pop
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   team.html

Dropped refs/stash@{0} (6914ed6d68ca7577a58cd3a3a6bb5f4f96ac8c9f)
Denys@Envy15X360-PC:~/Gym_Git_Exercise_Solutions$ git reset --hard
HEAD is now at 9c0e020 2nd commit
```
##  Bundle 2
### exercise 2

```bash
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout ft/service-redesign
error: pathspec 'ft/service-redesign' did not match any file(s) known to git
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-So
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git add .
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit -m "ft service"
[ft/service-redesign 96b765f] ft service
 1 file changed, 1 insertion(+)
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push origin dev
error: src refspec dev does not match any
error: failed to push some refs to 'https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git'
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 331 bytes | 331.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote: 
To https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
Branch 'ft/service-redesign' set up to track remote branch 'ft/service-redesign' from 'origin'.
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git add .
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit -m "ft from main"
[main c0e6035] ft from main
 1 file changed, 1 insertion(+)
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout  ft/service-redesign 
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git merge main
Auto-merging service.html
CONFLICT (content): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   service.html

no changes added to commit (use "git add" and/or "git commit -a")
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git add service.html 
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   service.html

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit -m "after merging"
[ft/service-redesign 5b4345d] after merging
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 456 bytes | 456.00 KiB/s, done.
Total 4 (delta 3), reused 0 (delta 0)
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
To https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git
   96b765f..5b4345d  ft/service-redesign -> ft/service-redesign

```

##  BUndle 3
### Exercise 1
```bash   
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ touch team.html
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-So
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git add team.html 
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status
On branch ft/team-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit -m "ft add team page"
[ft/team-page 9058435] ft add team page
 1 file changed, 12 insertions(+)
 create mode 100644 team.html
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 470 bytes | 470.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote: 
To https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page
Branch 'ft/team-page' set up to track remote branch 'ft/team-page' from 'origin'.
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout ft/team-page 
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git log
commit 90584357a7c7bfdd7e577476f631bf6c012a8fb8 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Thu Nov 10 10:52:57 2022 +0000

commit 90584357a7c7bfdd7e577476f631bf6c012a8fb8 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Thu Nov 10 10:52:57 2022 +0000

    ft add team page

commit 5b4345d89389100c451c8b7605896f115ee2f045 (origin/ft/service-redesign, ft/service-redesign)
Merge: 96b765f c0e6035
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Thu Nov 10 10:45:47 2022 +0000

    after merging

commit c0e60350d9da2f4201f2b4a32c02bb25edf4bf86 (main, ft/contact-page)
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Thu Nov 10 10:32:52 2022 +0000

    ft from main

commit 96b765f75be74d710d23974f95ef81b3e241f509
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Thu Nov 10 10:30:34 2022 +0000

    ft service

commit 49f2a820187e5eca107bed53060a6a29e7653f3e (origin/main, origin/HEAD)
Merge: 7cefe68 49a78bb
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Wed Nov 9 16:22:42 2022 +0200

    Merge pull request #1 from MugaboDenys/ft/bundle2
    
    Ft/bundle2

commit 49a78bb9cc6d0751be724d77a4fbe546a88b7263 (origin/ft/bundle2)
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Wed Nov 9 15:34:35 2022 +0200

    service page

commit a13b98c961165aac0b4fb0db965a38b910867cad
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Wed Nov 9 15:32:19 2022 +0200

    service page

commit 805aa168ae30b3f9be7ceeefc5827967eca270cf (origin/dev)
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Wed Nov 9 15:22:54 2022 +0200

    create service page

commit 9c0e020f3536a2c5d4d944da869eda2249177eed
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Wed Nov 9 15:15:43 2022 +0200

    2nd commit

commit 7cefe68832280b0219549983416766fa3ea25e5d
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Wed Nov 9 14:54:59 2022 +0200

    first commit

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout ft/contact-page 
error: Your local changes to the following files would be overwritten by checkout:
        team.html
Please commit your changes or stash them before you switch branches.
Aborting
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status
On branch ft/team-page
Your branch is up to date with 'origin/ft/team-page'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   team.html

no changes added to commit (use "git add" and/or "git commit -a")
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git restore
fatal: you must specify path(s) to restore
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git restore team.html
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout ft/contact-page 
Switched to branch 'ft/contact-page'
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git cherry-pick 90584357a7c7bfdd7e577476f631bf6c012a8fb8
[ft/contact-page 8d0132f] ft add team page
 Date: Thu Nov 10 10:52:57 2022 +0000
 1 file changed, 12 insertions(+)
 create mode 100644 team.html
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git add contact.html 
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status
On branch ft/contact-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   contact.html

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit -m "created contact page"
[ft/contact-page a089bfc] created contact page
 1 file changed, 12 insertions(+)
 create mode 100644 contact.html
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 742 bytes | 247.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote: 
To https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
Branch 'ft/contact-page' set up to track remote branch 'ft/contact-page' from 'origin'.
```
##  Bundle 3
### Exercise 2
 ```bash   
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git add faq.html 
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status
On branch ft/faq-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   faq.html

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit -m "created faq page"
[ft/faq-page 1f6d2e7] created faq page
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push origin ft/faq-page 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 457 bytes | 457.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page
remote: 
To https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git log
commit 1f6d2e7015924c63c362e06d32ce8cc3604f1683 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Thu Nov 10 12:07:44 2022 +0000

    created faq page

commit a089bfcff3f38912da119e18f6888fabab7378d2 (origin/ft/contact-page, ft/contact-page)
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Thu Nov 10 11:46:59 2022 +0000

    created contact page

commit 8d0132fbc39e0660624c981670af8db0e601dc0d
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Thu Nov 10 10:52:57 2022 +0000

    ft add team page

commit c0e60350d9da2f4201f2b4a32c02bb25edf4bf86 (main)
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Thu Nov 10 10:32:52 2022 +0000

    ft from main

commit 49f2a820187e5eca107bed53060a6a29e7653f3e (origin/main, origin/HEAD)
Merge: 7cefe68 49a78bb
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Wed Nov 9 16:22:42 2022 +0200

    Merge pull request #1 from MugaboDenys/ft/bundle2
    
    Ft/bundle2

commit 49a78bb9cc6d0751be724d77a4fbe546a88b7263 (origin/ft/bundle2)
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Wed Nov 9 15:34:35 2022 +0200

    service page

commit a13b98c961165aac0b4fb0db965a38b910867cad
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Wed Nov 9 15:32:19 2022 +0200

    service page

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git revert 8d0132fbc39e0660624c981670af8db0e601dc0d
Removing team.html
[ft/faq-page 744b2b3] Revert "ft add team page"
 1 file changed, 12 deletions(-)
 delete mode 100644 team.html
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-So
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status
On branch ft/faq-page
nothing to commit, working tree clean
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git add .
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit "bandle 3 exercise 1"
error: pathspec 'bandle 3 exercise 1' did not match any file(s) known to git
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit -m "bandle 3 exercise 1"
[ft/faq-page 7d6173a] bandle 3 exercise 1
 1 file changed, 1 insertion(+), 1 deletion(-)
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push --set-upstream origin ft/faq-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 537 bytes | 268.00 KiB/s, done.
Total 5 (delta 3), reused 0 (delta 0)
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
To https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git
   1f6d2e7..7d6173a  ft/faq-page -> ft/faq-page
Branch 'ft/faq-page' set up to track remote branch 'ft/faq-page' from 'origin'.
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status
On branch ft/faq-page
Your branch is up to date with 'origin/ft/faq-page'.

nothing to commit, working tree clean
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout -b ft/home-page
Switched to a new branch 'ft/home-page'
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git branch -D ft/home-page 
Deleted branch ft/home-page (was 7d6173a).
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout main 
M       home.html
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git add home.html 
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   home.html

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit -m "redesigned homepage"
[main 9ac0010] redesigned homepage
 1 file changed, 3 insertions(+), 1 deletion(-)
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout ft/home-page-redesign 
Switched to branch 'ft/home-page-redesign'
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git sta
stage    stash    status   
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status 
On branch ft/home-page-redesign
nothing to commit, working tree clean
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git rebase main 
First, rewinding head to replay your work on top of it...
Fast-forwarded ft/home-page-redesign to main.
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git add home.html 
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit -m "changed in home"
[ft/home-page-redesign a5cddda] changed in home
 1 file changed, 1 insertion(+), 1 deletion(-)
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push
fatal: The current branch ft/home-page-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 621 bytes | 621.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0)
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions/pull/new/ft/home-page-redesign
remote: 
To https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
Branch 'ft/home-page-redesign' set up to track remote branch 'ft/home-page-redesign' from 'origin'.
```


## Bundle 4
### exercise 1

```bash
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git remote add git-copy https://github.com/MugaboDenys/Gym-git-exercise-clone.git
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git add home.html 
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit -m "changes on hompage"
[main 314732a] changes on hompage
 1 file changed, 1 insertion(+), 6 deletions(-)
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push origin
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 744 bytes | 372.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0)
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
To https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git
   d493bdb..314732a  main -> main
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push git-copy 
Enumerating objects: 32, done.
Counting objects: 100% (32/32), done.
Delta compression using up to 8 threads
Compressing objects: 100% (30/30), done.
Writing objects: 100% (32/32), 5.17 KiB | 481.00 KiB/s, done.
Total 32 (delta 14), reused 0 (delta 0)
remote: Resolving deltas: 100% (14/14), done.
To https://github.com/MugaboDenys/Gym-git-exercise-clone.git
 * [new branch]      main -> main
```
##  Bundle 4
### Exercise 2
```bash
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status
On branch ft/footer
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        footer.html

nothing added to commit but untracked files present (use "git add" to track)
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git add footer.html 
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit -m "create footer page"
[ft/footer eee9e13] create footer page
 1 file changed, 12 insertions(+)
 create mode 100644 footer.html
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git add footer.html 
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit -m "changes in footer page"
[ft/footer 0e11060] changes in footer page
 1 file changed, 1 insertion(+)
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push
fatal: The current branch ft/footer has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/footer

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push --set-upstream origin ft/footer
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 754 bytes | 251.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions/pull/new/ft/footer
remote: 
To https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/footer -> ft/footer
Branch 'ft/footer' set up to track remote branch 'ft/footer' from 'origin'.
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git merge --squash ft/footer 
Updating 9ac0010..0e11060
Fast-forward
Squash commit -- not updating HEAD
 footer.html | 13 +++++++++++++
 home.html   |  2 +-
 2 files changed, 14 insertions(+), 1 deletion(-)
 create mode 100644 footer.html
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git commit -m "footer after squash"
[ft/squashing d6bb9bc] footer after squash
 2 files changed, 14 insertions(+), 1 deletion(-)
 create mode 100644 footer.html
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git log
commit d6bb9bcfb114b37895bb24564247ad08e2cde48e (HEAD -> ft/squashing)
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Thu Nov 10 13:39:38 2022 +0000

    footer after squash

commit 9ac0010199bae69284aa60355ed012b78a33002c (main)
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Thu Nov 10 12:31:56 2022 +0000

    redesigned homepage

commit c0e60350d9da2f4201f2b4a32c02bb25edf4bf86
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Thu Nov 10 10:32:52 2022 +0000

    ft from main

commit 49f2a820187e5eca107bed53060a6a29e7653f3e (origin/main, origin/HEAD)
Merge: 7cefe68 49a78bb
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Wed Nov 9 16:22:42 2022 +0200

    Merge pull request #1 from MugaboDenys/ft/bundle2
    
    Ft/bundle2

commit 49a78bb9cc6d0751be724d77a4fbe546a88b7263 (origin/ft/bundle2)
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Wed Nov 9 15:34:35 2022 +0200

    service page

commit a13b98c961165aac0b4fb0db965a38b910867cad
Author: Mugabodenys <mugabodan2020@gmail.com>
Date:   Wed Nov 9 15:32:19 2022 +0200

    service page

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git status 
On branch ft/squashing
nothing to commit, working tree clean
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push
fatal: The current branch ft/squashing has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/squashing

denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ git push --set-upstream origin ft/squashing
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 636 bytes | 636.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions/pull/new/ft/squashing
remote: 
To https://github.com/MugaboDenys/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/squashing -> ft/squashing
Branch 'ft/squashing' set up to track remote branch 'ft/squashing' from 'origin'.
denys@ENVY15x360cn0xxx1:~/Projects/Gym-Git-Exercise-Solutions$ 
```