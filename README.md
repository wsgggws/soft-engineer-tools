# My MacOS Tools
Some apps and command-lines, which run on my MacOS

![wsgggws](./wsgggws.png)

## 基本配置
- macOS High Sierra Version 10.13.6

## 说在前面的强烈建议
- 只安装一个中英文能切换的输入法, 并使用 `PlistEdit Pro` [删除MacOS自带的英文输入法](https://www.zhihu.com/question/21459701)
- [使用 `Karabiner` 自定义你的键盘映射, 熟悉盲打, 并熟悉你的快捷键](./typing.md)
- [安装并善用`Alfred`效率神器](https://github.com/wsgggws/alfred3-workflows)
- [配置并使用好`Term2`](./term2.md)
- [学会使用`Vim`并配置好它](https://github.com/wsgggws/my-neovim-configurations)

## 说在前面的可选建议
- Finder太难用了, 那试用下[ranger](https://www.howtoing.com/ranger-console-file-manager-with-vi-key-bindings)这个命令行工具吧
- 文件搜索`find`太慢了, 那试试`fzf`这个命令行工具吧, [这里](https://github.com/junegunn/fzf)
- 想实时清楚自己的网速, 那安装`NetWorker`

## MacOS Apps
- iTerm2
- Alfred3
- Google Chrome
- NeteaseMusit
- Karabiner
- Moom
- Snip
- ShortCat
- Fork
- Postmen
- Zoom
- Dash
- NetWorker
- KeepingYouAwake
- Usage
- Noizio
- TeamViewer
- Typore
- CheatSheet
- IINA
- LICEcap
- Keycastr
- The Unarchiver
- Bitbar
- Docker-CE
- AppCleaner
- Dictionary
- Outline, ShadowsocksX, Doutai
- Outlook
- Xmind
- Offices

## MacOS Command Lines
- brew
- git
- Neovim
- thefuck
- fzf
- ranger
- Hexo + Next


### iTerm2
Term2是macOS最好用的终端工具, 推荐配置tmux + oh-my-zsh(gruvbox-light.itermcolors) + autosuggestion + autojumper, 其中tmux可以很好管理多窗口,
配置及快捷键见[这里](./term2.md), oh-my-zsh集成了很多好用的命令行插件, 解放你的双手,其配置与使用见[这里](./term2.md),
autosuggestion能够自动补全你使用过的命令行, autojumper只要使用如`j *dir*`的命令即可快速跳转到你曾去过的目录,
不要使用相对或者绝对路径了.

### Alfred3
Alfred3是macOS最好用的效率神器, 你可以快速打开你的App, 实现快速切换App, 记录你的粘贴板内容, 实现快速粘贴你复制过的很多内容,
文件搜索, 浏览器搜索等功能, 配合workflows(且可以自己使用语言开发)能够完成诸如快速搜索选中内容, 查看IP地址, 快速翻译,
快速打开浏览器书签, 与Github进行交互等等实用操作, 绝对是效率神器, 详情见[这里](https://github.com/hjtianvip/alfred3-workflows)

### Google Chrome
推荐Google Chrome > FireFox > Safari, 其中有很多好用的扩展与插件, 如Surfingkeys使用vim方式管理浏览网页内容, LastPass管理用户名与密码, 与ublock origin广告过滤等等好用插件. 详情与推荐见[这里](./chrome.md)

### NeteaseMusit
因为手机上也是装的网易云音乐, 且使用时间长后, 推荐的音乐也较符合自己的口味, 就推荐了(互联网开发人员听音乐有不使用网易云音乐的?)

### Karabiner
重新映射自己的键盘, 如将Esc与Caps键替换, 为了对称将<-替换为Ctrl键, 使用Left Command+hjkl替换为上下左右方向键等,
根据自己的方式来配置, 很爽

### Moom
App窗口布局管理, 如使用快捷键将当着App窗口移动到左边, 最大小化, 多App窗口一左一右布局等

### Snip
截图工具, 腾讯QQ的截图开源实现

### ShortCat
如果你想尝试完全脱离鼠标, 那这个工具可以尝试下

### Fork
MacOS下Git的图形化提交工具, 还可以只提交修改后的小部分代码, 与Sourcetree为竞争产品, 但Fork颜值更高

### Postmen
网络请求修改与调试的工具, 能够记录与导入导出你的请求与参数, 并且能够转化为各种语言的爬虫代码, 如Python Request, curl, Java代码

### Zoom
视频会议, 自己录制视频都可以使用这工具

### Dash
离线文档, 支持很多语言很多库的文档

### NetWorker
你想知道你当前的网速吗? 它在bar上实时告诉你

### KeepingYouAwake
开会或者讲演时电脑却因为设置锁屏时间到达而锁屏了, 使用KeepingYouAwake点击下它可以让它不锁屏, 就不会尴尬了.

### Usage
显示自己时间花费在哪些应用软件上

### Noizio
有很多种自然界的杂音，包括电闪雷鸣，动物，火车鸣叫...可以组合

### TeamViewer
MacOS下的QQ是没有远程支持的, TeamViewer能够支持各种系统

### Typore
MacOS下写Markdown很爽

### CheatSheet
不记得快捷键了, 长按Command, CheatSheet告诉你

### IINA
看视频用的

### LICEcap
录制gif使用的

### Keycastr
录制时, 显示你在键盘上敲了哪些键

### The Unarchiver
解压如zip, rar, ...各种压缩文件

### Bitbar
我就只使用这工具在Bar上动态显示"Hand washing is not active, code issues!", 当然你可以显示当前股份,
或者其它你通过程序输出的各种信息

### Docker-CE
Docker当然是要装的

### AppCleaner
以托动的形式卸载MacOS上的App

### Dictionary
MacOS原生应用, 安装字典进行翻译, 配合触摸板使用效果很佳(三手指点下), 当然也有快捷键(Ctrl+Command+S)

### Outline, ShadowsocksX, Doutai
科学上网用的

### Outlook
微软集邮件日历管理等的工具, 适合跟公司使用. 可视化根据同事的时间安排, 在合适的时间地点安排会议, 还可以与Zoom一起使用

### Xmind
思维导图工具

### Offices
Word, Excel, PPT无处不在

---

### brew
MacOS下安装APP的命令

### git
git命令你得会使用

### Neovim
文本编辑器, 在服务器等无处不在, 我非常钟意, 配置与使用见[这里](https://github.com/wsgggws/my-neovim-configurations)

### thefuck
敲错命令行怎么办, fuck下, 大概率会给你想要的命令

### fzf
[文件名模糊搜索](https://github.com/junegunn/fzf)

### ranger
命令行下使用vim的方式管理你的文件,替换难使用的Finder

### Hexo + Next
如果你写博客, 可以利用Github Home Page配合Hexo + Next非常愉快的写静态博客
