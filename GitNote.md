(ssh关联自不用说)

git和github的关系：git是分布式版本控制系统可以理解为一个工具，而hub则是存放项目的仓库


git init	//将当前所在文件夹出初始化为一个仓库，主分支默认名由gitconfig文件决定，如并未配置则默认为master
					//查看默认配置指令git config --list

git config --global user.name "xxxx"
git config --global user.email xxxx@xx.com	//设置本地用户名和邮件地址，最好与github一致，尤其是邮箱

///当编写完成相应文件或者进行了修改后

git add xxx.c		//将xxx.c文件加入跟踪列表（每一次修改都必须要重新执行！！）
								//除非写入.gitignore文件（其中最重要的是!表示不被忽视）

git commit -m "xxxxx"		//将文件存档（m为message，备注信息，如果不加-m则会弹出窗口进行备注）

git push <远程主机名> <本地分支名>:<远程分支名>		//上传，如果本地和远程分支名相同则可省略远程分支名

git log		//查看目前为止的所有存档（commit以后才进入存档）
					//git一共分为三个区域：工作区--暂存区--本地仓库--（远程仓库如github、geehub）
					//存档全部保存在本地仓库，也就是控制系统仓库

git status //查看当前状态，即与之前的文档相比发生了哪些变化（也会提示下一步应该做什么）

git reset --hard xxxx  //回档，xxxx为log中的存档编号
											 //回档后，该档其后的存档会全部删除，有一定风险

git branch		//查看全部分支

git checkout xxxx		//切换分支，如果xxxx为log的编号则该分支为虚拟分支，同时可以查看当下存档的信息也可进行修改、存档并上传
										//但当切换回main或者其他分支的时候，会消失

git checkout -B xxxx  //创新新的分支，可用此方法替代上述方法。不会消失的同时，也可回溯存档


