#**Git setup and basic usage on Mac OSX**

**configure the global settings**

    git config --global user.name "Alex Douglas"
    git config --global user.email "alexd106@gmail.com"
    git config --global color.ui true
    git config --global core.editor vim
    git config --global core.excludesfile ~/.gitignore_global

The global ignore file has been created `~/.gitignore_global` and contains files that
git will ignore

Check what has been configured with:

    git config --list

**Setup ssh key and copy to clipboard. Add a new SSH key on github webpage**

Need to do this for all devices

    ssh-keygen -t rsa -C "alexd106@gmail.com"
    pbcopy < ~/.ssh/id_rsa.pub

Then paste a new SSH key on github webpage <https://github.com/settings/ssh>

Test the SSH using

    ssh -T git@github.com

Should receive the following:

     Hi alexd106! You've successfully authenticated, but GitHub does not provide shell access.

**Connecting to Git remotes**

In the directory which contains the files you wish to add

    git remote add origin git@github.com:alexd106/unix_setups.git

Now we can use the following to check that our local Git repository knows about the remote repository:

    git remote -v

We can add additional repositories in the same ways but using different names.

To delete unused remote repositories: 

    git remote rm <repository name>

**Simple Git workflow ouline**

This assumes you have already used `git remote add` 

To initialise a Git repository navigate to directory and use:

    git init

To check the status:

    git status

To track files:

    git add <file name>

To commit files:

    git commit -m "add an informative note"

or to stage all tracked files and commit all in one command:

    git commit -a -m "add informative note"

Note if files have been changed they are not automatically staged and will not be included when using `git commit`.
You need to use `git add` first and then then commit them (unless using the `commit -a option`).

To push changes to GitHub:

    git push origin master

To pull changes from GitHub:

    git pull origin master

To get a summary of past commits:

    git log --pretty=oneline --abbrev-commit

Note: You need to add the remote in each directory where you want to use git. Follow the instructions after you have created the new repository on github.com. 
