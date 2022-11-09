# Git exercise 1

```
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