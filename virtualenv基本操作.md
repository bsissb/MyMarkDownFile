---
title: virtualenv基本操作
tags: virtualenv,python
grammar_cjkRuby: true
---

## 安装
easy_install方式安装
```CentOS
[root@localhost ~]# yum install python-setuptools python-devel
[root@localhost ~]# easy_install virtualenv
```
## 创建virtualenv环境
使用virtualenv命令创建python虚拟环境：virtualenv [虚拟环境名称]。
(需要root权限)
```
[root@localhost ~]# virtualenv env1
New python executable in env1/bin/python
Installing setuptools, pip...done.
```
执行后，在本地会生成一个与虚拟环境同名的文件夹。

如果你的系统里安装有不同版本的python，可以使用--python参数指定虚拟环境的python版本：
```
virtualenv --python=/usr/local/python-2.7.8/bin/python2.7 env1
```

## 启动虚拟环境
 进入虚拟环境目录，启动虚拟环境，如下：
```
[root@localhost ~]# cd env1/
[root@localhost env1]# source bin/activate
(env1)[root@localhost env1]# python -V
Python 2.7.8
```
## 退出
deactivate

## 使用virtualenvwrapper

 virtualenvwrapper是virtualenv的扩展工具，可以方便的创建、删除、复制、切换不同的虚拟环境。
  1.安装virtualenvwrapper
  ```
  easy_install virtualenvwrapper
  ```
  创建一个文件夹，用于存放所有的虚拟环境：
  `mkdir ~/workspaces`
  设置环境变量，把下面两行添加到~/.bashrc里。
  ```
  export WORKON_HOME=~/workspaces
  source /usr/bin/virtualenvwrapper.sh
  ```
  2.创建虚拟环境：mkvirtualenv [虚拟环境名称]