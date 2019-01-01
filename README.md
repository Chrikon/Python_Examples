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
  # Syncing a fork

Sync a fork of a repository to keep it up-to-date with the upstream repository.

Before you can sync your fork with an upstream repository, you must configure a remote that points to the upstream repository in Git.

*Open Terminal.

*Change the current working directory to your local project.
````
cd /path to project
````

*Fetch the branches and their respective commits from the upstream repository. Commits to master will be stored in a local branch, upstream/master.
````
        git fetch orgin
````
*if you are not sure execute
````
        git remote -v
````
 *in order to get something like the below output:
 ````
        // origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
        // origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
 ````
 *the first name is what you are looking for

 *WE check out your fork's local master branch.
````
        git checkout master
````
*Merge the changes from origin/master into your local master branch. This brings your fork's master branch into sync with the origin repository, without losing your local changes.
````
        git merge origin/master
````
*If your local branch didn't have any unique commits, Git will instead perform a "fast-forward"
