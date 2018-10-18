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

（作为测试git checkout -- file 存在 当改变并且添加到暂存区 需要先回退版本  只是回退添加到暂存区的 直接 git reset HEAD --readme.txt 即可，然后本地文件再使用 git checkout -- readme.txt）


1,当改乱了工作区文件的内容，想直接丢弃工作区的修改时，用命令 git checkout -- file
2,当改乱了工作区文件的内容并且添加到了暂存区的时候，先使用命令 git reset HEAD file，然后再使用命令 git checkout -- 文件名


删除文件 rm file

1，误删除 使用 git checkout -- file  (从版本库里拉取文件)
2，确实想删除  git rm file 然后  git commit -m "";


cd ~  进入用户的主目录文件


让本地的git仓库和github上面的git仓库远程同步  -在github上创建一个仓库，然后在本地仓库执行命令
1，让本地仓库和github上面的仓库关联  git remote add origin git@github.com:YUECHUNYING/learngit.git
2,  把本地的内容推送到远程github库上  git push -u origin master



生成秘钥：ssh-keygen -t rsa -C "你自己的邮箱" (shell 或者是 git bash下面)


在github上新建一个仓库，在本地执行 git clone 建成仓库后的地址


git branch dev  (git命令创建一个分支)
git dev(分支的名称) （切换到dev这个分支）
git checkout -b dev (创建dev分支并且切换到dev分支上)

git branch （查看分支列表）
