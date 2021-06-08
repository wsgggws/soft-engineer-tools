# vim 使用技巧

- **移动(命令+插件)**
- **编辑(命令+插件)**
- **终端命令行**
- 文件管理
- 主题插件
- 编程语言相关插件

## 移动
- ^$ hjkl webWEB HML ft (){}% gg G / ctrl+o, ctrl+i, ctrl+l
- vim-easymotion
	- ss
- fzf.vim
	- [leader]f
	- ctrl+p
	- [leader]rg
	- [leader]b
	- [leader]l
	- [leader]h
- vim-bookmarks
	- [leader]mm
	- [leader]mi
	- [leader]mj, mk
- tagbar
	- [leader]tt
- FastFold
	- [space], zA, zR
- TaskList.vim
	- [leader]td
- vim-interestingwords
	- [leader]k
	- [leader]K

## 编辑
- iIaAoOxXrR xp ddp yyp p ydcv + 文本对象(aw,as,ap,ab,at,iw,is,ip,ib,it)
- `>>,<< :center, :left, :right`
- u ctrl+r :r :w :normal `:s/{a}/{b}`
- qa -> q ->[number]@a
- auto-pairs
- vim-surround
	- cs
	- ds
	- ys
- vim-repeat
- ultisnips
- vim-snippets
- coc.nvim
	- CocUpdate
	- CocInstall
- ale
- vim-commentary
	- gcc
	- gc
- vim-multiple-cursors
	- ctrl+n
	- ctrl+p
	- ctrl+x

## 命令行
- vim-floaterm
	- [leader]tf
	- Fn+F12

## 文件管理
- vim-nerdtree
	- [lead]nf
	- [lead]nt
	- q m a ?
- vim-signify
	- [leader]se
	- [leader]sd
	- [leader]st

## 主题插件
- vim-airline
- vim-airline-themes
- indentLine
- vim-startify
- vim-cursorword
- vim-lastplace
- vim-cool
- gruvbox
- vim-hybrid
- onedark.vim


## 编程语言
- dash
	- [leader]ds
- python-mode
	- [leader]r
- rust.vim
- webapi-vim
- vim-cargo
- vim-racer
- mathjax-support-for-mkdp
	- :MarkdownPreview
