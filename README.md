## Create a new repository from the command line
````
echo "# Python_Examples"
cd /path to your local project/
git init
git add * (adding everything)
git commit -m "Message of commit"
git remote add origin https://github.com/Chrikon/Python_Examples.git
git push -u origin master
````
---

## or push an existing repository from the command line
````
git remote add origin https://github.com/Chrikon/Python_Examples.git
git commit -m "Message in a bottle"
git push -u origin master
````
  ---
## Sync a fork in a repository to keep it up-to-date with the upstream repository.

1. Open Terminal.

2. Change to the git local directory of project.
````
cd /path to project
````

3. Fetch the branches and their respective commits from the upstream repository. Commits to master will be stored in a local branch, upstream/master.
````
git fetch orgin
````
4. if you are not sure execute
````
git remote -v
````
 5. in order to get something like the below output:
 ````
 origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
 origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
 ````
 6. the first name is what you are looking for

 7. we check out your fork's local master branch.
````
git checkout master
````
8. merge the changes from origin/master into your local master branch. This brings your fork's master branch into sync with the origin repository, without losing your local changes.
````
git merge origin/master
````
9. If your local branch didn't have any unique commits, Git will instead perform a "fast-forward"
