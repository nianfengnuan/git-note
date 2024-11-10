# 本笔记用于介绍git的常用命令
在官网可以直接安装Git
安装完成后，还需要最后一步设置,在命令行输入：

`$ git config --global user.name "Your Name"`
`$ git config --global user.email "email@example.com"`

由于Git是分布式版本控制系统，所以每台机器都需要自报家门：你的名字和Email地址。

注意`git config`命令的`--global`参数，使用此参数，表示此机器上所有的Git仓库都会使用该配置，当然也可以对某个仓库指定不同的用户名和Email

## Git创建仓库
* **git init** :初始化一个git仓库（若后面加仓库名，则新建一个目录，并在新建目录下创建仓库）

* **git clone**:clone一个git仓库：
 ` git clone <url> [directory]`

**注意要确保目录中不包含中文**

1. 用`git add`命令告诉Git,将文件添加到仓库中
   例如：git add readme.txt
2. 用`git commit`命令告诉Git,将文件提交到仓库 `git commit -m`后面输入本次改动的记录
   例如成功提交readme.txt文件后，会提示：`1 file changed`:一个文件被改动（新添加的readme.txt文件）`2 insertions`:插入了两行内容（readme.txt有两行内容）
3. 用`git status`命令可以查看关于工作目录和暂存区状态的信息
