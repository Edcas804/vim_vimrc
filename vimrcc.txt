syntax on
set number
set mouse=a
set clipboard=unnamed
set showcmd
set ruler
set encoding=utf8
set showmatch
set sw=4
set relativenumber
let mapleader = " "
set laststatus=2
set backspace=2
set guioptions-=T
set guioptions-=L
set ignorecase
imap ñl <Esc>

"Mapping to reload config
nmap <leader>so :source $HOME\_vimrc<CR>
nmap <leader>w :w <CR>
nmap <leader>q :q <CR>

"Autocompletar signos...
inoremap ( ()<Esc>i
inoremap " ""<Esc>i
inoremap ' ''<Esc>i
inoremap [ []<Esc>i
inoremap { {}<Esc>i
inoremap {<CR> {}<Esc>i<CR><CR><Esc>ki<leader><leader><leader> 


"Plantilla html
nnoremap ,html :-1read $HOME/.config/.skeleton.html<CR>




" Specify a directory for plugins
" - For Neovim: stdpath('data') . '/plugged'
" - Avoid using standard Vim directory names like 'plugin'
"
"
call plug#begin('~/.vim/plugged')
" Temas
Plug 'morhetz/gruvbox'
Plug 'crusoexia/vim-monokai'
Plug 'glepnir/oceanic-material'
Plug 'vim-airline/vim-airline-themes'
Plug 'flazz/vim-colorschemes'
"Nerdtree
Plug 'preservim/nerdtree'

Plug 'christoomey/vim-tmux-navigator'
"Color
Plug 'lilydjwg/colorizer'
Plug 'KabbAmine/vCoolor.vim'

"Indentar
Plug 'yggdroot/indentline'
"Emmemattn/emmet-vimt
Plug 'mattn/emmet-vim'

"Git integration
Plug 'mhinz/vim-signify'
Plug 'tpope/vim-fugitive'
Plug 'tpope/vim-rhubarb'
Plug 'junegunn/gv.vim'

"IDE
Plug 'easymotion/vim-easymotion'
"Autocompletar
Plug 'vim-scripts/AutoComplPop'
"Formatear  
"Plug 'prettier/vim-prettier', { 'do': 'yarn install'}
Plug 'prettier/vim-prettier', {
\ 'do': 'yarn install',
\ 'branch': 'release/0.x'
\ }
call plug#end()




"colorscheme gruvbox
" 'hard' 'medium' 'soft'
"let g:gruvbx_contrast_dark = "hard"
"let g:gruvbox_bold = "0"

"temes vim-colorschemes: darkeclipse, darkdevel, darkocean, darkZ, dante,
"moria, nazca, up
"papercolor


colorscheme darkZ 
 

nmap <Leader>nt :NERDTreeFind<CR>
nmap <Leader>s <Plug>(easymotion-s2)
nmap <Leader>py <Plug>(Prettier)
map <leader><tab> :NERDTreeToggle<CR>
  
let g:prettier#config#config_precedence = 'file-override'
let g:prettier#autoformat=1
