# The-Gym git exercises
## Bundle 1
### Exercise 1

```bash
mkdir the-gym-git-exercise
cd the-gym-git-exercise
git init
    Initialized empty Git repository in /home/mickael-angebhd/Desktop/The Gym/the-gym-git-exercise/.git/

touch index.html
touch styles.css
git status
    On branch main
    No commits yet
    Untracked files:
      (use "git add <file>..." to include in what will be committed)
	    index.html
	    styles.css
    nothing added to commit but untracked files present (use "git add" to track)


git branch --move main master
git status
    On branch master
    No commits yet
    Untracked files:
      (use "git add <file>..." to include in what will be committed)
	    index.html
	    styles.css
    nothing added to commit but untracked files present (use "git add" to track)

git branch --move master main
git status
    On branch main
    No commits yet
    Untracked files:
      (use "git add <file>..." to include in what will be committed)
    	index.html
    	styles.css
    nothing added to commit but untracked files present (use "git add" to track)

git add index.html 
git add styles.css 
git commit -m "Adding new files"
    [main (root-commit) fff9b52] Adding new files
     2 files changed, 0 insertions(+), 0 deletions(-)
     create mode 100644 index.html
     create mode 100644 styles.css

git remote add origin https://github.com/angebhd/the-gym-git-exercise.git
git push -u origin main
    Enumerating objects: 3, done.
    Counting objects: 100% (3/3), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (2/2), done.
    Writing objects: 100% (3/3), 243 bytes | 243.00 KiB/s, done.
    Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
    To https://github.com/angebhd/the-gym-git-exercise.git
     * [new branch]      main -> main
    branch 'main' set up to track 'origin/main'.

git checkout -b dev
    Switched to a new branch 'dev'

git status
    On branch dev
    nothing to commit, working tree clean
git branch
    * dev
      main

git checkout -b test
    Switched to a new branch 'test'

git checkout dev
    Switched to branch 'dev'

git branch -d test
    Deleted branch test (was fff9b52).
```

### Exercise 2

```bash
touch home.html
git status
    On branch main
    Your branch is up to date with 'origin/main'.

    Untracked files:
      (use "git add <file>..." to include in what will be committed)
    	home.html
    nothing added to commit but untracked files present (use "git add" to track)

git add home.html
git stash
    Saved working directory and index state WIP on main: fff9b52 Adding new files

git status
    On branch main
    Your branch is up to date with 'origin/main'.

    nothing to commit, working tree clean

touch about.html
git add about.html
git stash
    Saved working directory and index state WIP on main: fff9b52 Adding new files

touch team.html
git add team.html
git stash
    Saved working directory and index state WIP on main: fff9b52 Adding new files

git stash list
    stash@{0}: WIP on main: fff9b52 Adding new files
    stash@{1}: WIP on main: fff9b52 Adding new files
    stash@{2}: WIP on main: fff9b52 Adding new files

git stash pop --index 1
    <stdin>:15: trailing whitespace.

    warning: 1 line adds whitespace errors.
    On branch main
    Your branch is up to date with 'origin/main'.

    Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
    	new file:   about.html

    Dropped refs/stash@{1} (e350af9c9cfed1fd865d35619bf5c7daca385a18)

git stash list
    stash@{0}: WIP on main: fff9b52 Adding new files
    stash@{1}: WIP on main: fff9b52 Adding new files

git add about.html
git stash pop --index 1
    <stdin>:15: trailing whitespace.

    warning: 1 line adds whitespace errors.
    On branch main
    Your branch is up to date with 'origin/main'.

    Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
    	new file:   home.html

    Untracked files:
      (use "git add <file>..." to include in what will be committed)
    	about.html

    Dropped refs/stash@{1} (473237a35f6655e2a6fb6450d4c84c65cbec8d38)
git add about.html
git status
    On branch main
    Your branch is up to date with 'origin/main'.

    Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
    	new file:   about.html
    	new file:   home.html


git commit -m "Adding home and about files"
    [main 479933e] Adding home and about files
     2 files changed, 22 insertions(+)
     create mode 100644 about.html
     create mode 100644 home.html

git stash list
    stash@{0}: WIP on main: fff9b52 Adding new files

git stash pop --index 0
    <stdin>:15: trailing whitespace.

    warning: 1 line adds whitespace errors.
    On branch main
    Your branch is ahead of 'origin/main' by 1 commit.
      (use "git push" to publish your local commits)

    Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
    	new file:   team.html

    Dropped refs/stash@{0} (1ab4876117d1294834b22a9cd34b54268841d207)

git reset
git stash list
git status
    On branch main
    Your branch is ahead of 'origin/main' by 1 commit.
      (use "git push" to publish your local commits)

    Untracked files:
      (use "git add <file>..." to include in what will be committed)
    	team.html

    nothing added to commit but untracked files present (use "git add" to track)

```