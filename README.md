# Introduce(English)
<img src="./images/1.gif"></img>

> this is a software to translate English letter to Chinese letter -- I don't want it to be a plugin.
>
> you can hacking it to translate everything.(I only give Byte Code,You can reComplier it--such as online website?..)
>
> It is simple & use java(jdk1.8)
>
> the map I confirm in vim is `<LEADER>n`

# Start to use

> I use neovim,so my example is for neovim.

## 1

> add this to your vim(or neovim) config file
>
> (in vim,`~/.vim/vimrc` or `~/.vimrc`)
>
> (in neovim,`~/.config/nvim/initvim`)

```
"I think it's to difficult to press `\`,so I chang it!whatever?
let mapleader=" "

"you can type :help XXX to know what it meanings...
noremap <LEADER>n :let a=expand("<cword>")<Bar>exec'!java -jar ~/.config/nvim/plugged/youdaosearch.jar ' .a<CR>
```

## 2

> download youdaosearch.jar to above path
>
> such like `~/config/nvim/plugged`
>
> or you know how to do,what ever you want.

> anyway,it's simple.you can hack it use java.

# 介绍

> 因为我做的这个开箱即用的软件本来就是为了我能阅读英文。
>
> 适用那些小白用户。
>
> 原理:我做了个小软件叫做youdaosearch.jar,这个软件可以接受命令行参数`单词`，然后拼接到有道的API上。
>
> 利用dom4j来进行解析返回值。`java -jar youdaosearch.jar apple`
>
> 在vim普通模式下，通过`<cword>`来获取你光标所在的那个单词，
>
> (不知道`<cword>`的意思可以用`:help <cword>`来查找官方解释。)
>
> 然后通过一些键位匹配来完成。
>

