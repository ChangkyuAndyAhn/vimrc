# HOW TO SETUP VIM

## clone vimrc repo and make symbolic link
    cd ~  
    git clone git@github.com:positoy/vimrc  
    ln -s ~/vimrc/.vim ~/.vim  
    ln -s ~/vimrc/.vimrc ~/.vimrc  
* cscope path could be changed depending on OS  
* MacOS path : /usr/local/bin/cscope  

## install ctags
    brew install ctags  

## install cscope
    brew install cscope  
    ln -s ~/vimrc/mkcscope.sh /usr/local/bin/mkcscope.sh  
    ln -s ~/vimrc/rmcscope.sh /usr/local/bin/rmcscope.sh  

## install vim plugins
    git clone git@github.com:VundleVim/Vundle.vim.git
    on the vim commandline  
    :VundleInstall  

## display git branch name on terinal prompt
    git_branch() {
        git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
    }
    export PS1="\u@\[\033[32m\]\w\[\033[33m\]\$(git_branch)\[\033[00m\]\$ " 
* put following at the end of the .bash_profile

## git config
git config --global core.editor vim
git config --global core.autocrlf true
git config --global core.eol lf

### reference
https://ysoh.wordpress.com/2012/04/09/%EB%A6%AC%EB%88%85%EC%8A%A4-%EC%BB%A4%EB%84%90-%EA%B0%9C%EB%B0%9C%EC%9D%84-%EC%9C%84%ED%95%9C-vim-%EC%84%A4%EC%A0%95-vimrc/  

### Yes I can
to JH
