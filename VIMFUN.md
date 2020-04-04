# Cool Vim / Terminal Fun

These are based on the [Dracula](https://draculatheme.com/) theme.

## Part 1: Get Vim-plug
Download a minimilist, light-weight Vim plugin manager [here](https://github.com/junegunn/vim-plug/blob/master/README.md) <br/>

Copy [plug.vim](https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim) and put it in the `~/.vim/autoload` directory.
```sh
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

## Part 2: Get Dracula theme for Vim
This part is easy! Just copy and paste the following into your .vimrc. The comments tell what each line does.
```vim
" activates filetype detection
filetype plugin on

" activates syntax highlighting among other things
syntax on

" allows you to deal with multiple unsaved
" buffers simultaneously without resorting
" to misusing tabs
set hidden

" delete over line breaks, indents, or
" start of insert mode
set backspace=indent,eol,start

" Set tabs to only 4 spaces
set vb t_vb=
set tabstop=4

" Add plug ins use vim plug
" Stored in plugged directory
call plug#begin('~/.vim/plugged')

" Plugin for Dracula theme
Plug 'dracula/vim', { 'as': 'dracula' }

call plug#end()

" use Dracula theme as default
colorscheme dracula
```

## Part 3: Get Dracula theme for cmd
The information for this was taken from [Dracula's Powershell Github](https://github.com/dracula/powershell) <br/>
We can get the dracula-style theme for Vim by changing the cmd.exe environment variable `prompt`:
```sh
setx prompt "$E[1;32;40m→ $E[1;36;40m$p$E[1;35;40m› $E[1;37;40m"
```

## Part 4: Finding more Dracula themes
You can get more at the [Dracula website](https://draculatheme.com/). They are all free and reasonably light-weight!
