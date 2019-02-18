---
title: deepin第四篇博客
date: 2019-02-18 13:43:19
tags:
---


使用 Hexo + GitHub 可以轻松搞出一个好看的博客
以下是步骤。

进入一个安全的目录，比如 cd ~/Desktop 或者 cd ~/Documents，别在根目录 / 瞎搞。以后所有的教程第一步都是「进入一个安全的目录，别在根目录瞎搞」，只有 ~ 里面的目录是你能碰的！
在 GitHub 上新建一个空 repo，repo 名称是「你的用户名.github.io」（注意个用户名是你的GitHub用户名，不是你的电脑用户名）
npm install -g hexo-cli，安装 Hexo
hexo init myBlog
cd myBlog
npm i
hexo new 开博大吉，你会看到一个 md 文件的路径
Windows 的路径中的 \ 需要变成 / 才行哦
Windows 的路径中的 \ 需要变成 / 才行哦

Windows 的路径中的 \ 需要变成 / 才行哦
Windows 的路径中的 \ 需要变成 / 才行哦
Windows 的路径中的 \ 需要变成 / 才行哦
运行 start source/_post/开博大吉.md 来编辑这个 md 文件，内容自己想（Ubuntu 系统用 xdg-open xxxxxxxxxxxxxxxxxxx.md 命令）

举例：如果 Windows 提示的是 INFO created: ~\Desktop\myBlog\source_posts\开博大吉.md
那么你的命令就应该是 start "~/Desktop/myBlog/source/_posts/开博大吉.md" 注意引号和斜杠，如果路径里没有空格，就不需要引号。
内容示例

  ---
  title: 开博大吉
  ---

  # 哈哈
  我的博客开通啦
start _config.yml，编辑网站配置
把第 6 行的 title 改成你想要的名字
把第 9 行的 author 改成你的大名
把最后一行的 type 改成 type: git
在最后一行后面新增一行，左边与 type 平齐，加上一行 repo: 仓库地址 （请将仓库地址改为「你的用户名.github.io」对应的仓库地址，仓库地址以 git@github.com: 开头你知道吧？不知道？不知道的话现在你知道了）
第 4 步的 repo: 后面有个空格，不要眼瞎。
npm install hexo-deployer-git --save，安装 git 部署插件
hexo deploy
进入「你的用户名.github.io」对应的 repo，打开 GitHub Pages 功能，如果已经打开了，你应该会看到一个预览链接
用浏览器访问「预览链接/index.html」就应该看到了你的博客！（GitHub Pages 存在延迟，如果没看到，过三分钟再刷新看看）
第二篇博客
hexo new 第二篇博客
复制显示的路径，使用 start 路径 来编辑它
hexo generate
hexo deploy
去看你的博客，应该能看到第二篇博客了
换主题
https://github.com/hexojs/hexo/wiki/Themes 上面有主题合集
随便找一个主题，进入主题的 GitHub 首页，比如我找的是 https://github.com/iissnan/hexo-theme-next
复制它的 SSH 地址或 HTTPS 地址，假设地址为 git@github.com:iissnan/hexo-theme-next.git
cd themes
git clone git@github.com:iissnan/hexo-theme-next.git
cd ..
将 _config.yml 的第 75 行改为 theme: hexo-theme-next，保存
hexo generate
hexo deploy
等一分钟，然后刷新你的博客页面，你会看到一个新的外观。如果不喜欢这个主题，就回到第 1 步，重选一个主题。