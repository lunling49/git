git使用：
本地：
1、mkdir <file>，创建一个空目录
2、git init，将这个目录变成 git 可管理的本地仓库
3、vi/vim <file>，在文件夹下编写（或新增）文件
4、git add <file>，实际上就是把要提交的所有修改放到暂存区（Stage）
5、git commit -m "改动说明"，把暂存区的所有修改提交到分支

版本回退：
git log -- 查看改动日志，即提交历史，以便确定要回退到哪个版本
git reflog -- 查看命令历史，以便确定要回到未来的哪个版本
HEAD -- 指向的版本就是当前版本
git reset --hard commid_id(版本号) -- 回退或回到未来的版本
上一个版本HEAD^，上上一个版本HEAD^^，上很多版本时，可写成~数字，比如20，HEAD~20

管理修改：
git diff HEAD -- <file>  查看工作区和版本库里最新版的区别
git checkout -- <file> -- 把文件在工作区的修改全部撤销
如果修改后的内容添加到了暂存区，想丢弃修改
	1、git reset HEAD <file>，回到工作区
	2、git checkout -- <file>，工作区丢弃修改
如果commit了，想丢弃修改
	git reset --hare HEAD^ 或者 git reset --hard +版本号

删除文件：
1、rm <file>，相当于只删除了工作区的文件，如果想要恢复，直接用git checkout -- <file>
2、git rm <file>，相当于不仅删除了文件，而且还添加到了暂存区，需要先git reset HEAD <file>，然后再git checkout -- <file>
3、如果要彻底把版本库删掉，先git rm，再git commit