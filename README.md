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
set belloff=all
set hidden
set nocp
set grepprg=rg\ --vimgrep\ --smart-case\ --follow

filetype plugin on

call plug#begin()
Plug 'junegunn/fzf.vim'
Plug 'junegunn/fzf', { 'do': { -> fzf#install() } }
call plug#end()

nnoremap <silent> <C-f> :Files<CR>
nnoremap <silent> <Leader>f :Rg<CR>

nnoremap <C-y> "+y
vnoremap <C-y> "+y
nnoremap <C-p> "+p
vnoremap <C-p> "+p
inoremap <C-p> <C-r>+
```
