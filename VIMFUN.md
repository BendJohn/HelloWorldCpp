# Cool Vim / Terminal Fun

These are based on the [Dracula](https://draculatheme.com/) theme.

## Part 1: Get Vim-plug
Download a minimilist, light-weight Vim plugin manager [here](https://github.com/junegunn/vim-plug/blob/master/README.md) <br/>

Copy [plug.vim](https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim) and put it in the `~/.vim/autoload` directory.
```sh
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

## Part 2: Get Dracula theme
This part is easy! Just copy and paste the following into your .vimrc. The comments tell what each line does.
```sh
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
