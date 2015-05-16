---
layout: post
title: VIM常用命令
comments: true
---

## 对标点内的内容进行操作 

>   ci'、ci"、ci(、ci[、ci{、ci< - 分别更改这些配对标点符号中的文本内容
>
>   di'、di"、di(或dib、di[、di{或diB、di< - 分别删除这些配对标点符号中的文本内容
>
>   yi'、yi"、yi(、yi[、yi{、yi< - 分别复制这些配对标点符号中的文本内容
>
>   vi'、vi"、vi(、vi[、vi{、vi< - 分别选中这些配对标点符号中的文本内容}])}])}])}])"

## 复制或移动内容到指定位置

>   行号9 ，行号15 copy 行号16                                        将行号9到行号15的内容复制到行号16所在行的后面。

>   行号9 ，行号15 move 行号16                                       将行号9到行号15的文本内容移动到行号16所在行的后面。

## 复制到系统剪切板

在普通模式下按v进入可视模式，选中要复制的内容后按

    " + y 

三个键就可以把内容复制到系统粘贴板，下面在终端那里按Ctrl+Shift+v就可以粘贴了

## VIM格式化代码

>   按两下小写g，即gg，定位光标到第一行。

>   按住Shift+v，即大写V，进入可视化编辑的列编辑模式。

>   Shift+g，即大写G，选中整个代码。

>   按下等号=，格式化所有代码。"

## 参考资料
