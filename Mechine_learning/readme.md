# 项目说明
该项目用于记录台大李宏毅老师的2020年的机器学习课程，主要是上课笔记和课后作业的内容。

课后作业是给予python3.6.8进行的，使用Pyenv进行Python版本管理。

## 课前准备
______________________________________
1.第一步在ubuntu桌面环境下，安装和配置pyenv：
```
$ git clone https://github.com/pyenv/pyenv.git ~/.pyenv
$ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
$ echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
$ echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bashrc
$ exec "$SHELL"
```
______________________________________
2.常用的pyenv指令
- pyenv versions
列出目前系统中所有的Python
- pyenv version
显示当前预设的Python版本,*表示当前环境下所使用的python版本
- pyenv install <python_version>
安装特定版本的Python

【注】由于这种方式安装太慢，一般采用手动下载Python的方式进行安装，以安装3.6.8为例
```
1.下载3.6.8版本的Python安装包，浏览器访问下方网址，下载安装包：
https://www.python.org/ftp/python/3.6.8/Python-3.6.8.tar.xz
2.将安装包文件放到～/.pyenv/cache路径下，如果.pyenv文件夹下没有cache文件夹，手动创建
3.对～/.pyenv/plugins/python-build/share/python-build/3.6.8文件进行修改
首行添加“cat ~/.pyenv/plugins/python-build/share/python-build/3.6.8”，用于输出安装信息
4.由于安装编译python需要一些依赖项，所以需要提前安装
$ sudo apt-get install make build-essential libssl-dev zlib1g-dev
$ sudo apt-get install libbz2-dev libreadline-dev libsqlite3-dev wget curl
$ sudo apt-get install llvm libncurses5-dev libncursesw5-dev
$ sudo apt-get update
5.终端运行pyenv install 3.6.8
```
- pyenv uninstall <python_version>
移除特定版本的Python
- pyenv global 3.x.x
切换工作环境下的Python版本

如果此时在终端安装python相关的包时，会将相关包安装在当前的星号版本下的python环境下，卸载时会将所有的外带的包也一起删除
______________________________________
3.常用的git指令
- git init
初始化当前文件夹
- git clone <url>
将网络上的资料克隆到本地端
- git add <files>
```
git add a.txt
git add a.txt b.sh c.cpp
git add --all
```
将文件加入到版本管理记录缓存中，
- git rm --cached <file>
将文件从版本管理记录缓存中取消
- git status
查看当前工作环境的状态
- git commit -m <description>
对新的修改记录添加一个commit
- git remote add origin <url>
将本地端对应到远端网络
- git push -u origin <branch>
将提交记录同步到Github