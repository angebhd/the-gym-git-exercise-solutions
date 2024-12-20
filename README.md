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


## Bundle 2
### Exercise 1

```bash
git checkout -b ft/bundle-2
    Switched to a new branch 'ft/bundle-2'

touch services.html
git add services.html
git commit -m "Adding services page"
    [ft/bundle-2 4362342] Adding services page
     1 file changed, 11 insertions(+)
     create mode 100644 services.html

git push --set-upstream origin ft/bundle-2
    Enumerating objects: 4, done.
    Counting objects: 100% (4/4), done.
    Delta compression using up to 8 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 438 bytes | 438.00 KiB/s, done.
    Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (1/1), completed with 1 local object.
    remote: 
    remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
    remote:      https://github.com/angebhd/the-gym-git-exercise/pull/new/ft/bundle-2
    remote: 
    To https://github.com/angebhd/the-gym-git-exercise.git
     * [new branch]      ft/bundle-2 -> ft/bundle-2
    branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
```

### Exercise 2

```bash
git checkout main 
    Switched to branch 'main'
    Your branch is ahead of 'origin/main' by 1 commit.
      (use "git push" to publish your local commits)

git pull
    remote: Enumerating objects: 1, done.
    remote: Counting objects: 100% (1/1), done.
    remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
    Unpacking objects: 100% (1/1), 901 bytes | 450.00 KiB/s, done.
    From https://github.com/angebhd/the-gym-git-exercise
       fff9b52..0b616a5  main       -> origin/main
    Updating 479933e..0b616a5
    Fast-forward
     services.html | 11 +++++++++++
     1 file changed, 11 insertions(+)
     create mode 100644 services.htm

git status
    On branch main
    Your branch is up to date with 'origin/main'.

    Untracked files:
      (use "git add <file>..." to include in what will be committed)
    	team.html

    nothing added to commit but untracked files present (use "git add" to track)

git checkout -b ft/service-redesign
    Switched to a new branch 'ft/service-redesign'

git status
    On branch ft/service-redesign
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
    	modified:   services.html

    Untracked files:
      (use "git add <file>..." to include in what will be committed)
    	team.html

    no changes added to commit (use "git add" and/or "git commit -a")

git add services.html
git commit -m "Redesigning services page"
    [ft/service-redesign 0062aac] Redesigning services page
     1 file changed, 1 insertion(+)

git push --set-upstream origin ft/service-redesign
    Enumerating objects: 5, done.
    Counting objects: 100% (5/5), done.
    Delta compression using up to 8 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 381 bytes | 381.00 KiB/s, done.
    Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
    remote: 
    remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
    remote:      https://github.com/angebhd/the-gym-git-exercise/pull/new/ft/service-redesign
    remote: 
    To https://github.com/angebhd/the-gym-git-exercise.git
     * [new branch]      ft/service-redesign -> ft/service-redesign
    branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

git checkout main
    Switched to branch 'main'
    Your branch is up to date with 'origin/main'.

git status
    On branch main
    Your branch is up to date with 'origin/main'.

    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
    	modified:   services.html

    Untracked files:
      (use "git add <file>..." to include in what will be committed)
    	team.html

    no changes added to commit (use "git add" and/or "git commit -a")

git add services.html
git commit -m "Redesigning services.html from main branch"
    [main 6cc8099] Redesigning services.html from main branch
     1 file changed, 1 insertion(+)

git push --set-upstream origin main
    Enumerating objects: 5, done.
    Counting objects: 100% (5/5), done.
    Delta compression using up to 8 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 360 bytes | 360.00 KiB/s, done.
    Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
    To https://github.com/angebhd/the-gym-git-exercise.git
       0b616a5..6cc8099  main -> main
    branch 'main' set up to track 'origin/main'.

git checkout ft/service-redesign
    Switched to branch 'ft/service-redesign'
    Your branch is up to date with 'origin/ft/service-redesign'.

git diff main
    diff --git a/services.html b/services.html
    index 9d66ba9..d35044e 100644
    --- a/services.html
    +++ b/services.html
    @@ -7,6 +7,6 @@
     </head>
     <body>
         <h1>Git Services</h1>
    -    <p> New paragraph from main </p>
    +    <p> New changes from <span>ft/service-redesign</span> branch </p>
     </body>
     </html>
    \ No newline at end of file

git merge main
    Auto-merging services.html
    CONFLICT (content): Merge conflict in services.html
    Automatic merge failed; fix conflicts and then commit the result.

git status
    On branch ft/service-redesign
    Your branch is up to date with 'origin/ft/service-redesign'.

    You have unmerged paths.
      (fix conflicts and run "git commit")
      (use "git merge --abort" to abort the merge)

    Unmerged paths:
      (use "git add <file>..." to mark resolution)
    	both modified:   services.html

    Untracked files:
      (use "git add <file>..." to include in what will be committed)
    	team.html

    no changes added to commit (use "git add" and/or "git commit -a")

git add services.html 
git commit -m 'Resolving merge conflict on serveices.html'
    [ft/service-redesign fa49b5f] Resolving merge conflict on serveices.html

git push --set-upstream origin ft/service-redesign
    Enumerating objects: 7, done.
    Counting objects: 100% (7/7), done.
    Delta compression using up to 8 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 393 bytes | 393.00 KiB/s, done.
    Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
    To https://github.com/angebhd/the-gym-git-exercise.git
       0062aac..fa49b5f  ft/service-redesign -> ft/service-redesign
    branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

```

## Bundle 3
### Exercise 1

```bash
git checkout main
    Switched to branch 'main'
    Your branch is up to date with 'origin/main'.

git checkout -b ft/team-page
    Switched to a new branch 'ft/team-page'

git add team.html
git commit -m "Creating team.html"
    [ft/team-page 8bb45ac] Creating team.html
     1 file changed, 11 insertions(+)
     create mode 100644 team.html

git push --set-upstream origin ft/team-page
    Enumerating objects: 4, done.
    Counting objects: 100% (4/4), done.
    Delta compression using up to 8 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 438 bytes | 438.00 KiB/s, done.
    Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (1/1), completed with 1 local object.
    remote: 
    remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
    remote:      https://github.com/angebhd/the-gym-git-exercise/pull/new/ft/team-page
    remote: 
    To https://github.com/angebhd/the-gym-git-exercise.git
     * [new branch]      ft/team-page -> ft/team-page
    branch 'ft/team-page' set up to track 'origin/ft/team-page'.

git checkout main
    Switched to branch 'main'
    Your branch is up to date with 'origin/main'.

git checkout -b ft/contact-page
    Switched to a new branch 'ft/contact-page'

git checkout ft/team-page 
    Switched to branch 'ft/team-page'
    Your branch is up to date with 'origin/ft/team-page'.

git log
    commit 8bb45acc333f078ef8b9418d0307758896c30309 (HEAD -> ft/team-page, origin/ft/team-page)
    Author: Asifiwe Buhendwa <mickaelbhd@gmail.com>
    Date:   Thu Dec 19 17:43:34 2024 +0200

        Creating team.html

    commit 6cc8099a087195598fb0e40017d2df342f643db8 (origin/main, origin/HEAD, main, ft/contact-page)
    Author: Asifiwe Buhendwa <mickaelbhd@gmail.com>
    Date:   Thu Dec 19 16:51:52 2024 +0200

        Redesigning services.html from main branch

    commit 0b616a5c36d8f3afd59d9e292b2bd2f2cd9bd36f
    Merge: fff9b52 4362342
    Author: Ange BUHENDWA <mickaelbhd@gmail.com>
    Date:   Thu Dec 19 16:20:06 2024 +0200

        Merge pull request #1 from angebhd/ft/bundle-2

        Bundle 2 Exercise 1
git checkout ft/contact-page
    Switched to branch 'ft/contact-page'

git cherry-pick 8bb45acc333f078ef8b9418d0307758896c30309
    [ft/contact-page 6457bbb] Creating team.html
     Date: Thu Dec 19 17:43:34 2024 +0200
     1 file changed, 11 insertions(+)
     create mode 100644 team.html

touch contact.html
git add contact.html
git commit -m "Adding contact page"
    [ft/contact-page 5c01582] Adding contact page
     1 file changed, 11 insertions(+)
     create mode 100644 contact.html

git push --set-upstream origin ft/contact-page 
    Enumerating objects: 7, done.
    Counting objects: 100% (7/7), done.
    Delta compression using up to 8 threads
    Compressing objects: 100% (6/6), done.
    Writing objects: 100% (6/6), 715 bytes | 715.00 KiB/s, done.
    Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (3/3), completed with 1 local object.
    remote: 
    remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
    remote:      https://github.com/angebhd/the-gym-git-exercise/pull/new/ft/contact-page
    remote: 
    To https://github.com/angebhd/the-gym-git-exercise.git
     * [new branch]      ft/contact-page -> ft/contact-page
    branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

git checkout -b ft/faq-page
    Switched to a new branch 'ft/faq-page'

touch faq.html
git add faq.html
git commit -m "Creating faq page"
    [ft/faq-page 8f7a61f] Creating faq page
     1 file changed, 11 insertions(+)
     create mode 100644 faq.html

git push --set-upstream origin ft/faq-page 
    Enumerating objects: 4, done.
    Counting objects: 100% (4/4), done.
    Delta compression using up to 8 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 431 bytes | 431.00 KiB/s, done.
    Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (1/1), completed with 1 local object.
    remote: 
    remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
    remote:      https://github.com/angebhd/the-gym-git-exercise/pull/new/ft/faq-page
    remote: 
    To https://github.com/angebhd/the-gym-git-exercise.git
     * [new branch]      ft/faq-page -> ft/faq-page
    branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

git checkout ft/team-page      
    Switched to branch 'ft/team-page'
    Your branch is up to date with 'origin/ft/team-page'.

git status
    On branch ft/team-page
    Your branch is up to date with 'origin/ft/team-page'.

    nothing to commit, working tree clean

git revert 8bb45acc333f078ef8b9418d0307758896c30309
    [ft/team-page ae9d415] Revert "Creating team.html"
     1 file changed, 11 deletions(-)
     delete mode 100644 team.html
git status
    On branch ft/team-page
    Your branch is ahead of 'origin/ft/team-page' by 1 commit.
      (use "git push" to publish your local commits)

    nothing to commit, working tree clean
git push --set-upstream origin ft/team-page 
    Enumerating objects: 3, done.
    Counting objects: 100% (3/3), done.
    Delta compression using up to 8 threads
    Compressing objects: 100% (2/2), done.
    Writing objects: 100% (2/2), 260 bytes | 260.00 KiB/s, done.
    Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (1/1), completed with 1 local object.
    To https://github.com/angebhd/the-gym-git-exercise.git
       8bb45ac..ae9d415  ft/team-page -> ft/team-page
    branch 'ft/team-page' set up to track 'origin/ft/team-page'.
    
```

### Exercise 3

```bash
git branch
      dev
      ft/bundle-2
      ft/contact-page
      ft/faq-page
      ft/service-redesign
    * ft/team-page
      main
git checkout ft/faq-page 
    Switched to branch 'ft/faq-page'
    Your branch is up to date with 'origin/ft/faq-page'.
git checkout -b ft/home-page-redesign
    Switched to a new branch 'ft/home-page-redesign'
git checkout main       
    Switched to branch 'main'
    Your branch is up to date with 'origin/main'.
    git status 
    On branch main
    Your branch is up to date with 'origin/main'.

    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
    	modified:   home.html

    no changes added to commit (use "git add" and/or "git commit -a")
git add home.html 
git commit -m "Modifications on home page"
    [main 1f6f020] Modifications on home page
     1 file changed, 1 insertion(+), 1 deletion(-)
git checkout ft/home-page-redesign 
    Switched to branch 'ft/home-page-redesign'
git rebase main
    Successfully rebased and updated refs/heads/ft/home-page-redesign.
git log
    commit 4408013574300be22de80666b09091f163b8cd0d (HEAD -> ft/home-page-redesign)
    Author: Asifiwe Buhendwa <mickaelbhd@gmail.com>
    Date:   Thu Dec 19 17:59:44 2024 +0200

        Creating faq page

    commit 984c3c4edb5228b3e57e115fdbb138678f61af71
    Author: Asifiwe Buhendwa <mickaelbhd@gmail.com>
    Date:   Thu Dec 19 17:54:16 2024 +0200

        Adding contact page

    commit 1762c98876b61121f959d8dabcf755937ba0ff1d
    Author: Asifiwe Buhendwa <mickaelbhd@gmail.com>
    Date:   Thu Dec 19 17:43:34 2024 +0200

        Creating team.html

    commit 1f6f020e132c4534430b45bf1554b35749cf6b35 (main)
    Author: Asifiwe Buhendwa <mickaelbhd@gmail.com>
    Date:   Fri Dec 20 11:35:30 2024 +0200

        Modifications on home page
git status        
    On branch ft/home-page-redesign
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
    	modified:   home.html

    no changes added to commit (use "git add" and/or "git commit -a")
git add home.html 
git commit -m "Adding a paragraph to the home page"
    [ft/home-page-redesign 2515104] Adding a paragraph to the home page
     1 file changed, 2 insertions(+)
git push --set-upstream origin ft/home-page-redesign 
    Enumerating objects: 17, done.
    Counting objects: 100% (17/17), done.
    Delta compression using up to 8 threads
    Compressing objects: 100% (15/15), done.
    Writing objects: 100% (15/15), 1.57 KiB | 1.57 MiB/s, done.
    Total 15 (delta 8), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (8/8), completed with 1 local object.
    remote: 
    remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting
    remote:      https://github.com/angebhd/the-gym-git-exercise/pull/new/ft/home-page-redesign
    remote: 
    To https://github.com/angebhd/the-gym-git-exercise.git
     * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
    branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

```