# Git基本操作

## 获取与创建项目命令
### git init

![enter description here][1]
这样就可以在当前文件夹创建一个仓库

![enter description here][2]

可以看到git在这里创建了一个 ==.git== 文件夹

### git clone
使用git clone拷贝一个git仓库到本地
```
git clone [url]
```
默认情况下，Git 会按照你提供的 URL 所指示的项目的名称创建你的本地项目目录。 通常就是该 URL 最后一个 / 之后的项目名称。如果你想要一个不一样的名字， 你可以在该命令后加上你想要的名称。

## 基本快照
![enter description here][3]
### git add命令
可以把该文件添加到缓存（即添加到仓库的管理中
"AM" 状态的意思是，这个文件在我们将它添加到缓存之后又有改动。改动后我们在执行 git add 命令将其添加到缓存中：
![enter description here][4]


### git status -s命令
用来将查看当前项目的状态，没有加-s参数就会输出其他内容
### git diff
用来查看执行git diff结果的详细信息
git diff命令显示写入缓存和未写入缓存的改动的区别
git diff --cached #显示已缓存的改动
![enter description here][5]
### git commit
使用 git add 命令将想要快照的内容写入缓存区， 而执行 git commit 将缓存区内容添加到仓库中。
![enter description here][6]

### git reset HEAD
用于取消已经缓存的内容
例如同时修改README,hello.php
然后用git add提交到缓存区
执行
` git reset HEAD -- hello.php `
取消hello.php的缓存
之后用git commit -m则只会上传README的缓存
简而言之，执行 git reset HEAD 以取消之前 git add 添加，但不希望包含在下一提交快照中的缓存。

### git rm
会从本地磁盘中删除该文件
如果你要在工作目录中留着该文件，可以使用 git rm --cached

### git mv
用于移动，重命名








  [1]: ./images/1.png "1"
  [2]: ./images/2.png "2"
  [3]: ./images/3.png "3"
  [4]: ./images/5.png "5"
  [5]: ./images/4.png "4"
  [6]: ./images/6.png "6"