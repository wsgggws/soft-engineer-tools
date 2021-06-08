# My MacOS Tools
Some apps and command-lines, which runs on mine MacOS.
Be more faster

![wsgggws](./wsgggws.png)

## 基本配置
- macOS Big Sur Version 11.4

## 说在前面的强烈建议
- 只安装一个中英文能切换的输入法, 并使用 `PlistEdit Pro` [删除MacOS自带的英文输入法](https://www.zhihu.com/question/21459701)
- [善于使用Chrome](./chrome.md)
- [使用 `Karabiner` 自定义你的键盘映射, 熟悉盲打, 并熟悉你的快捷键](./typing.md)
- [安装并善用`Alfred`效率神器](./alfred.md)
- [配置并使用好`Term2`](./term2.md)
- [学会使用`Vim`并配置好它](./vim.md)


### Google Chrome
- 浏览器推荐指数 Google Chrome > FireFox > Safari.
- 其中有很多好用的扩展与插件, 详情与推荐见[这里](./chrome.md)
    - 如 Surfingkeys 使用vim方式管理浏览网页内容.
    - ublock origin 广告过滤等等好用插件.
    - LastPass 管理用户名与密码.
    - ...

### Karabiner
- 根据自己按键喜好, 重新映射自己的键盘.
    - 如将Esc与Caps键替换,
    - 为了对称将<-替换为Ctrl键,
    - 使用Left Command+hjkl替换为上下左右方向键等,
    - ...

### Alfred
- Alfred 是 MacOS 最好用的效率神器.
- 你可以
    - 快速打开你的App.
    - 实现快速切换App.
    - 记录你的粘贴板内容. 实现快速粘贴你复制过的很多内容,
    - 文件搜索, 浏览器搜索等功能,
    - 配合workflows(且可以自己使用语言开发)能够完成诸如
        - 快速搜索选中内容,
        - 查看IP地址,
        - 快速翻译,
        - 快速打开浏览器书签,
        - 与Github进行交互等等实用操作,
	- ...
- 绝对是效率神器, 详情见[这里](https://github.com/hjtianvip/alfred3-workflows)

### iTerm2
Term2是macOS最好用的终端工具, 推荐配置tmux + oh-my-zsh(gruvbox-light.itermcolors) + autosuggestion + autojumper, 其中tmux可以很好管理多窗口,
配置及快捷键见[这里](./term2.md), oh-my-zsh集成了很多好用的命令行插件, 解放你的双手,其配置与使用见[这里](./term2.md),
autosuggestion能够自动补全你使用过的命令行, autojumper只要使用如`j *dir*`的命令即可快速跳转到你曾去过的目录,

### KeepingYouAwake
开会或者讲演时电脑却因为设置锁屏时间到达而锁屏了, 使用KeepingYouAwake点击下它可以让它不锁屏, 就不会尴尬了.

### Moom
- Moon是MacOS最好用的窗口布局工具.
    - 如使用快捷键将当着App窗口移动到上下左右边.
    - 最大小化.
    - 多应该窗口一左一右, 上下布局等.

### Snip
- 截图工具, 腾讯QQ的截图开源MacOS平台实现.


### Postmen
- 网络请求修改与调试的工具.
- 能够记录与导入导出你的请求与参数.
- 能够转化为各种语言如Python Request, curl, Java的爬虫代码.

### Zoom
- 视频会议.
- 录制视频.
- 全平台(Andriod, ISO, Windows, MacOS, Linux, ...)支持.

### Dash
- 支持很多语言很多库的离线文档(先下载)
- 与Vim, Alfred3都有接口支持

### CheatSheet
- 不记得快捷键了, 长按Command, CheatSheet告诉你

### LICEcap
- 录制gif.

### Keycastr
- 录制时, 显示你在键盘上敲了哪些键

### Keka
- 解压如zip, rar, ...各种压缩文件

### Docker-CE
- Docker当然是要装的.

### AppCleaner
- 以托动的形式干净地卸载MacOS上的App.

### Dictionary
- MacOS原生应用, 需要额外安装中英字典进行翻译, 配合触摸板使用效果很佳(三手指点下), 当然也有快捷键(Ctrl+Command+D).

### IINA
- 看视频用的, 多窗口, 大小布局, 快进...不在话下.

### NeteaseMusit
- 互联网开发人员听音乐有不使用网易云音乐的?
- 每日有推荐, 评论很精彩.

### Offices
- 微软的Word, Excel, PPT无处不在.

### NetWorker
- 你想知道你当前的网速吗? 它来实时告诉你.


---

### HomeBrew
- MacOS下安装APP的命令, 如`brew install git`

### git
- git命令你得会使用, 如`git commit -m"SOME COMMIT"`

### Neovim
- 文本编辑器.
- 各服务器等终端里无处不在. 
- 我非常钟意, 各开发语言(Java除外)均配置使用Nvim.
- 配置与使用见[这里](https://github.com/wsgggws/my-neovim-configurations)

### thefuck
- 敲错命令行怎么办, fuck下, 大概率会给你想要的命令.

### fzf
- [文件名模糊搜索](https://github.com/junegunn/fzf)
