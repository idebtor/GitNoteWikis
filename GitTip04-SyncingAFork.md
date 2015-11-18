
# Syncing a fork
Sync a fork of a repository to keep it up-to-date with the upstream repository.

**Tip:** Before you can sync your fork with an upstream repository, you must configure a remote that points to the upstream repository in Git.

1. Open Terminal (for Mac and Linux users) or the command prompt (for Windows users).
2. Change the current working directory to your local project.
3. Fetch the branches and their respective commits from the upstream repository. Commits to master will be stored in a local branch, upstream/master.

    $ git fetch upstream
4. Check out your fork's local master branch.

    $ git checkout master
5. Merge the changes from upstream/master into your local master branch. This brings your fork's master branch into sync with the upstream repository, without losing your local changes.

    $ git merge upstream/master
  
**Tip:** Syncing your fork only updates your local copy of the repository. To update your fork on GitHub, you must **push** your changes.

