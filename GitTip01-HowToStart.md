# How to start Git

1. Installing Git Only.[Go to 2.]
  - To check Git installation, check its version using the command ```git --version```.
  - If you have not installed it, follow the this wiki page instruction [Git installation instructions](https://www.udacity.com/wiki/ud775/install-git)

2. Installing Git and GitHub

  - Download and install the latest version of GitHub Desktop. This will automatically install Git and keep it up-to-date for you.

3. Setting up Git

  - On your computer, open the Git Shell application.
  - Go to the folder where you would like to work on.
  - Tell Git your name so your commits will be properly labeled. Type everything after the $ here:

    ```$ git config --global user.name "YOUR NAME"```

  - Tell Git the email address that will be associated with your Git commits. The email you specify should be the same one found in your email settings. To keep your email address hidden, see "Keeping your email address private".

    ```$ git config --global user.email "YOUR EMAIL ADDRESS"```

4. Basic Git Commands
  - ```git --version``` To check Git version installed
  - ```git init``` - To create a new git repo(or repository)
  - ```git clone [/local/repository/path]``` - To create a working copy of a local repo
  - ```git clone [repo URL]``` - To create a working copy of a local repo from a remote server(GitHub)
  - ```git add [filename]``` - To stage(propose changes) the file(s)
  - ```git commit -m [my comments]``` - To commit files staged to the HEAD, but not in your remote repo yet
  - ```git push origin master``` - To send the changes in the local repo(HEAD) to master.
  - ```git push``` - To send the changes in the remote repo (you may check it by git remote show origin.)
  - ```git remote add origin [repo URL]``` - If you have cloned an existing repo and want to connect your repo to a remote server, add it with this command. Then you now push your changes to the selected remote server.
  - ```git checkout -b bugfix5``` To create a new branch named "bugfix5" and switch to it
  - ```git checkout master``` - To switch back to master
  - ```git branch -d bugfix5``` - To delete the branch
  - ```git push origin [branch]``` To push the branch to the remote repo to make it available to others
  - ```git pull``` - To update the local repo to the newest commit
  - ```git merge [branch]``` - To merge another branch into the active branch (e.g. master)
  - ```git checkout [commit ID]``` - To checkout a certain commit; going back to the old version.
  - ```git checkout -- [filename]```  - To revert the file
  - ```git diff [commit ID] [commit ID]``` - To compare the two versions of the code in those commits.
  - ```git tag [1.0.0 123bcde456]``` To create a new tag named 1.0.0 and first 10 chars of commit ID
  - ```git log```   - To show a list of the recent commits, including commit IDs; Press q to quit.
  - ```git log --pretty=oneline``` - To see a very compressed log where each commit is one line:
  - ```git log --graph --oneline --decorate --all``` To see all branches, decorated
  - ```git log --name-status``` - To see which files have changed
  - ```git config --global color.ui auto```     - To use colorful git output
  - ```git config --global core.editor "atom --wait"``` - To set the default editor in Git to use Atom
  - ```git config --global core.editor "subl -n -w"``` - To set the default editor in Git to use Sublime Text
  - ```git config --global push.default upstream```
  - ```git config --global merge.confictstyle diff3```
  - ```git config format.pretty oneline``` - To show log on just one line per commit
  - ```git config color.ui.true``` - To display the console in color
  - ```git fetch origin``` - To give up all changes and commits at local, fetch the remote repository
  - ```git reset --hard origin/master``` - To give up all changes and commits at local, fetch the remote repository

  **Note**: You may enter the first four or more characters of the commit ID rather than pasting the entire ID

5. Setting up workspace
   - Save [this file](https://github.com/idebtor/Note123OnGit/blob/master/git-completion.bash) in your home directory with the name ```git-completion.bash```.
   - Save [this file](https://github.com/idebtor/Note123OnGit/blob/master/git-prompt.sh) in your home directory with the name ```git-prompt.sh```.
   - Copy and paste the following contents at the bottom of ```.bash_profile``` if you already have one in your home directory. Otherwise, create ```.bash_profile``` in your home directory, copy and paste the following contents. If you use Linux, you may need to name this file ```.bashrc``` instead of ```.bash_profile```.

```   
# Enable tab completion
source ~/git-completion.bash

# colors!
red="\[\033[0;31m\]"
green="\[\033[0;32m\]"
yellow="\[\033[0;33m\]"
blue="\[\033[0;34m\]"
purple="\[\033[0;35m\]"
cyan="\[\033[0;36m\]"
reset="\[\033[0m\]"

# Change command prompt
source ~/git-prompt.sh
export GIT_PS1_SHOWDIRTYSTATE=1
# '\u' adds the name of the current user to the prompt
# '\$(__git_ps1)' adds git-related stuff
# '\W' adds the name of the current directory
export PS1="$purple\u$green\$(__git_ps1)$yellow \W $ $reset"
```

# How to start quick

## create a new repository on the command line
echo "# HuStarx" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/idebtor/HuStarx.git
git push -u origin master

## …or push an existing repository from the command line
git remote add origin https://github.com/idebtor/HuStarx.git
git push -u origin master

