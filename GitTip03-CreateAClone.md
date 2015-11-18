# Create a local clone of your fork

**Tip:** When you fork a repo, it forked in GitHub, not in your local.

**Tip:** Usually you fork a repo first in GitHub, then create a local clone in your local(machine).

## Fork an example repository:
Forking a repository is a simple two-step process. We've created a repository for you to practice with!
1. On GitHub, navigate to the octocat/Spoon-Knife repository.
2. In the top-right corner of the page, click Fork.

That's it! Now, you have a fork of the original octocat/Spoon-Knife repository.

## Create a local clone of your fork: 
Let's suppose you have a fork of the Spoon-Knife repository as an example shown above, but you don't have the files in that repository on your computer. Let's create a clone of your fork locally on your computer.

1. On GitHub, navigate to your fork of the Spoon-Knife repository.
2. In the right sidebar of your fork's repository page, click  to copy the clone URL for your fork.
3. Open Terminal (for Mac and Linux users) or the command prompt (for Windows users).
4. Type git clone, and then paste the URL you copied in Step 2 above. It will look like this, with your GitHub username instead of YOUR-USERNAME:

    git clone https://github.com/YOUR-USERNAME/Spoon-Knife
    
5. Press Enter. Your local clone will be created.

    git clone https://github.com/YOUR-USERNAME/Spoon-Knife
    
Now, you have a local copy of your fork of the Spoon-Knife repository!

## Configure Git to sync your fork with the original Spoon-Knife repository
When you fork a project in order to propose changes to the original repository, you can configure Git to pull changes from the original, or upstream, repository into the local clone of your fork.

1. On GitHub, navigate to the octocat/Spoon-Knife repository.
2. In the right sidebar of the repository page, click  to copy the clone URL for the repository.
3. Open Terminal (for Mac and Linux users) or the command prompt (for Windows users).
4. Change directories to the location of the fork you cloned in Step 2: Create a local clone of your fork.

    $ cd Spoon-Knife

5. Type git remote -v and press Enter. You'll see the current configured remote repository for your fork.

    $ git remote -v
    
    origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
    
    origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)

6. Type git remote add upstream, and then paste the URL you copied in Step 2 and press Enter. It will look like this:

    $ git remote add upstream https://github.com/octocat/Spoon-Knife.git
    
7. To verify the new upstream repository you've specified for your fork, type git remote -v again. You should see the URL for your fork as origin, and the URL for the original repository as upstream.

    $ git remote -v
    
    origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
    
    origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
    
    upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
    
    upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)

Now, you can keep your fork synced with the upstream repository with a few Git commands. For more information, see "Syncing a fork."


    


