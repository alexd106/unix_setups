#**setting up a mac to use various GNU software rather than BSD**

**install homebrew from [homebrew](http://brew.sh)**

    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

A couple of usefull homebrew commands

    update homebrew
    brew update

update homebrew packages

    brew upgrade

**install git**

    brew install git

**install GNU unix utilities**

    brew install coreutils

**install gawk**

    brew install gawk

**Installation pathogen.vim to manage vim plugins**

from <https://github.com/tpope/vim-pathogen>

Install to `~/.vim/autoload/pathogen.vim` or copy and paste:

    mkdir -p ~/.vim/autoload ~/.vim/bundle && \
    curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim

Runtime Path Manipulation

Add this to your vimrc:

    execute pathogen#infect()

Now any plugins you wish to install can be extracted to a subdirectory under `~/.vim/bundle` and they willbe added to the 'runtimepath'. Observe to install vim-sensible:

    cd ~/.vim/bundle && \
    git clone git://github.com/tpope/vim-sensible.git

**install eunuch.vim to add more functionality to vim**

from <https://github.com/tpope/vim-eunuch>

    cd ~/.vim/bundle
    git clone git://github.com/tpope/vim-eunuch.git

**install vim-markdown**

from <https://github.com/plasticboy/vim-markdown>

    cd ~/.vim/bundle
    git clone https://github.com/plasticboy/vim-markdown.git

**install monokai.vim colour scheme**

from <https://github.com/sickill/vim-monokai>

    cd ~/.vim/colors
    git clone git://github.com/sickill/vim-monokai.git
    cp -i ./vim-monokai/colors/monokai.vim .

then in `~/.vimrc` add the following

    set colorscheme monokai

**Misc Terminal preferences**

Change the default startup theme to homebrew, change the font to Lucida console pt 14 and opacity to 100%
