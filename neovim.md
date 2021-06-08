# vim 使用技巧

### 目标: 快速移动 + 快速编辑 + 快速使用命令行

- **移动(命令+插件)**
- **编辑(命令+插件)**
- **终端命令行**
- 文件管理
- 主题插件
- 编程语言相关插件

## 移动
- 0^$ hjkl fFtT; webWEB %
- HML zz (){} gg G /?n \*n
- ctrl+o, ctrl+i
- :number

- vim-easymotion
	- ss
- fzf.vim
	- [leader]f
	- ctrl+p
	- [leader]rg
	- [leader]b
	- [leader]l
	- [leader]h
- coc.vim
	- gd
- vim-bookmarks
	- [leader]mi [leader]mm [leader]ma [leader]mj [leader]mk [leader]mc
- TaskList.vim
	- [leader]td
- tagbar
	- [leader]tt
- FastFold
	- [space], zA, zR

## 编辑
- iIaAoOxXrR
- cdpyvCDPYV
- ctrl+h, ctrl+w, ctrl+u
- J, ==,  `>>, <<, :center, :left, :right`
- ~, gu, gU
- u, ctrl+r
- ctrl+v IA
- :ctrl+r
- :r, :w, :f
- :normal, `:s/{a}/{b}`, :! cmd, :!!
- qa -> q ->[number]@a

- auto-pairs
- vim-surround
	- cs ds ys vs
- vim-repeat
- ultisnips
- vim-snippets
- coc.nvim
- ale
- vim-commentary
	- gcc gc
- vim-multiple-cursors
	- ctrl+n ctrl+p ctrl+x

## 命令行
- vim-floaterm
	- [leader]tf
	- Fn+F12

## 文件管理
- vim-nerdtree
	- [lead]nf
	- [lead]nt
	- ma mm ? q
- vim-signify
	- [leader]st [leader]sd

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
- vim-interestingwords
	- [leader]k
	- [leader]K


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
