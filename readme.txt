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

$ git diff HEAD --readme.txt查看工作区与版本库最新版本的区别

$ git checkout -- readme.txt把工作区的修改全部撤销，如果暂存区有readme.txt,则将工作区的恢复到暂存区状态，否则，恢复到版本库状态。

$ git reset HEAD readme.txt 把暂存区的文件放回到工作区（覆盖工作区）。然后使用$ git checkout -- readme.txt 把工作区恢复到版本库状态。

工作区新添加了文件使用add和commit添加到版本库，$rm test.txt效果等同于在文件夹中直接删除。如果要恢复，使用$git checkout -- test.txt将版本库中的替换工作区中的版本。要删除版本库中的，使用$git rm test.txt.


远程仓库 github充当git服务器 本地git仓库和github仓库之间通过SSH加密，
$ ssh-keygen -t rsa -C "1013222027@qq.com" 创建SSH Key
主目录下.ssh下id_rsa和id_rsa.pub后者为公钥。复制到github的account的ssh keys下。只要每天电脑的key都添加到github，就可以在每台电脑往github推送了