# VIM CONFIG

## Plugin Manager

vim plug
```
iwr -useb https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim |`
    ni $HOME/vimfiles/autoload/plug.vim -Force
```

## Plugins
- [fzf](https://github.com/junegunn/fzf) 
- [ripgrep](https://github.com/BurntSushi/ripgrep)

## .vimrc

```
set belloff=all " annoying windows notification off
set hidden
set nocp
set grepprg=rg\ --vimgrep\ --smart-case\ --follow
set relativenumber 

filetype plugin on

call plug#begin()
Plug 'junegunn/fzf.vim'
Plug 'junegunn/fzf', { 'do': { -> fzf#install() } }
call plug#end()

" Copy and Paste to system register
nnoremap <C-y> "+y
vnoremap <C-y> "+y
nnoremap <C-p> "+p
vnoremap <C-p> "+p
inoremap <C-p> <C-r>+

" Soft line navigation
nnoremap J gj
vnoremap J gj
nnoremap K gk
vnoremap K gk
```
