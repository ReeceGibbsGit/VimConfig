# VIM CONFIG

## .vimrc

```
set belloff=all
set backspace=2
set hidden
set nocp
set relativenumber

let &t_SI = "\e[5 q"  " Insert mode - blinking vertical bar
let &t_EI = "\e[1 q"  " Normal mode - blinking block

nnoremap <C-y> "+y
vnoremap <C-y> "+y
nnoremap <C-p> "+p
vnoremap <C-p> "+p
inoremap <C-p> <C-r>+

nnoremap <C-d> "+d
vnoremap <C-d> "+d

nnoremap J gj
vnoremap J gj

nnoremap K gk
vnoremap K gk

nnoremap B ge
vnoremap B ge

vnoremap $ g_
```
