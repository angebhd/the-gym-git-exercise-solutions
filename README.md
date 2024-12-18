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