#**git set up on Mac OSX**

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

Then add a new SSH key on github webpage <https://github.com/settings/ssh>

Test the SSH using

    ssh -T git@github.com

Should receive the following:

Hi alexd106! You've successfully authenticated, but GitHub does not provide shell access.


