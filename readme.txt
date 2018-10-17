学习git；
git是一个版本控制系统。
git是开源的。

学习git status

git diff  

git log 查看提交日志

git log --pretty=oneline 使得输出日志信息简洁

HEAD^ 上一版本
HEAD^^ 上两个版本
HEAD~100  往上100版本

版本回退  git reset --hard HEAD^

（版本回退之后想要再改回来  根据git log 提供的commit id 可以再次回退  git reset --hard  19sa23---- 指定要回退的版本的commit id）
( Git 在内部有一个指向当前版本的HEAD 指针，当你回退版本的时候，仅仅是改变HEAD的指向)


cat readme.txt  (该命令用于查看readme.txt文件的内容)

git reflog (记录每一次的命令)
git log (提交历史)


git diff (工作区和暂存区的比较 ，可以看开发过程中修改了那些内容)

尝试看git add 但是不进行 git commit

沒有提交，返回最后一次提交后的状态  git checkout -- readme.txt