测试文件
//Git is a version control system.
//Git is free software.
$mkdir learngit在当前目录创建一个文件夹learngit
$cd learngit 进入learngit文件夹
$pwd 显示当前文件夹全路径
$git init 初始化一个git仓库
在learn下创建readme.text
$git add readme.text添加文件到仓库
$git commit -m"本次提交的说明"
可以一次添加多个文件一次说明

//Git is a distributed version control system.
//Git is free software.
修改文件后使用$git status查看状态，提示changes not staged for commit;文件修改，未提交
使用$git diff查看修改的内容
提交修改和提交新文件一样要两步
$git add提交
$git status查看状态，提示将要修改包含的文件
$git commit -m"修改说明"
$git status查看状态，没有需要提交的更改，工作目录干净

//Git is a distributed version control system.
//Git is free software distributed under the GPL.
$git log查看历史记录
$git log --pretty=oneline显示在一行,长串16进制数字是commit id（版本号）
当前版本是HEAD,上一个是HEAD^,上上一个HEAD^^,往上100,HEAD~100.

按q键退出：

$git reset --hard HEAD^回到上一个
$git reset --hard commit id (前几位即可)回到版本号（过去或未来）
Git在内部有个指向当前版本的HEAD指针，当你回退版本的时候，Git仅仅是把HEAD指向改变，顺便把工作区的文件更新。
$ git reflog 查看历史命令，查看commit id


learngit是工作区，.git是版本库，版本库下包含stage（暂存区）和自动创建的第一个分支master，以及指向master的指针HEAD。
add把文件放到暂存区，commit把暂存区的文件提交到当前分支。

git diff HEAD --readme.txt查看工作区与版本库最新版本的区别