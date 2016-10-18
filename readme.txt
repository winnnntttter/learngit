测试文件
//Git is a version control system.
//Git is free software.
$mkdir learngit在当前目录创建一个文件夹learngit
$cd learngit 进入learngit文件夹
$pwd 显示当前文件夹quanlujing
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