# git-cheatsheet
Commonly used git commands

* Get help on a command
~~~
git <COMMAND> --help
~~~
* Create a repository in the current directory<br/>
~~~
git init
~~~
* Create a repository from an existing one<br/>
~~~
git clone git://host.org/project.git
~~~
* Changes made in working directory<br/>
~~~
git status
~~~
* Changes made to tracked files<br/>
~~~
git diff
~~~
* History of changes<br/>
~~~
git log
~~~
* What changed between ID1 and ID2<br/>
~~~
git diff <ID1> <ID2>
~~~
* History of changes for file with diffs<br/>
~~~
git log -p <FILE> <DIRECTORY>
~~~
* All local branches (star [*] marks the current branch)<br/>
~~~
git branch
~~~
* Return to the last commited state (cannot be undone!)<br/>
~~~
git reset -hard
~~~
* Revert the last commit (creates a new commit)<br/>
~~~
git revert HEAD
~~~
* Revert specific commit (creates a new commit)<br/>
~~~
git revert <ID>
~~~
* Fix the last commit (after editing the broken files)<br/>
~~~
git commit -a -amend
~~~
* Checkout the ID version of a file<br/>
~~~
git checkout <ID> <FILE>
~~~
* Fetch lastest changes from origin (this does not merge them)<br/>
~~~
git fetch
~~~
* Pull latest changes from origin (does a fetch followed by a merge)<br/>
~~~
git pull
~~~
* Apply a patch that someone sent you<br/>
~~~
git am -3 patch.mbox
~~~
In case of conflict, resolve the conflict and<br/>
~~~
git am --resolved
~~~
* Commit all your local changes<br/>
~~~
git commit -a
~~~
* Prepare a patch for other developers<br/>
~~~
git format-patch origin
~~~
* Push changes to origin<br/>
~~~
git push
~~~
* Make a version or milestone<br/>
~~~
git tag v1.0
~~~
* Switch to a branch
~~~
git checkout <BRANCH>
~~~
* Marge BRANCH1 into BRANCH2
~~~
git checkout <BRANCH2>
git merge <BRANCH1>
~~~
* Create branch BRANCH based on HEAD
~~~
git branch <BRANCH>
~~~
* Create branch BRANCH based on OTHER and switch to it
~~~
git checkout -b <BRANCH> <OTHER>
~~~
* Delete branch BRANCH
~~~
git branch -d <BRANCH>
~~~
* View merge conflicts
~~~
git diff
~~~
* View merge conflicts against base file
~~~
git diff -base <FILE>
~~~
* View merge conflicts against base file
~~~
git diff -base <FILE>
~~~
* View merge conflicts against your changes
~~~
git diff -ours <FILE>
~~~
* View merge conflicts against other changes
~~~
git diff -theirs <FILE>
~~~
* Discard a conflicting patch
~~~
git reset -hard
git rebase -skip
~~~
* After resolving conflicts, merge with
~~~
git add <CONFLICTING_FILE>
git rebase -continue
~~~