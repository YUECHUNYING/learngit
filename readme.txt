学习git；
git是一个版本控制系统。
git是开源的。

1.pwd命令 用于显示当前目录
2.windows系统 确保目录名包括父目录  不包含中文

3.git init 把目录变成git可以管理的仓库 （会生成.git目录，跟踪管理版本库）
.git 目录默认是隐藏的 可以用 ls -ah 命令显示

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
git checkout dev(分支的名称) （切换到dev这个分支）
git checkout -b dev (创建dev分支并且切换到dev分支上)

git branch （查看分支列表）


git merge dev  (合并指定的分支到当前分支下，)

git branch -d dev （删除dev分支）

解决冲突 把git合并失败的文件手动编辑为希望的内容


git merge --no-ff -m "合并并且提交文件" dev  
（合并分支时加上 --no-ff 参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并,而fast-forward合并就看不出来曾经做过合并）

git stash 工作区储藏功能
git stash list 查看工作现场

恢复 工作区内容：1，git stash apply 恢复后stash的内容并不删除，需要使用 git stash drop来删除
                           2，git stash pop 恢复的同时把stash的内容也删除了
1，git stash  2,去做别的事情比如修复个bug  3，git stash pop 恢复工作现场



新建的一个分支，还没有合并 如果删除，就会丢失掉修改 ，如果要强行删除，需要一个参数 -D。
git branch -D dev （强行删除）


查看远程库的信息  git remote  --> origin
                            git remote -v 更详细的信息

推送分支  就是把该分支上的所有本地提交推送到远程库，推送时，要指定本地分支。
这样，git就把该分支推送到远程库对应的远程分支上。

创建远程origin的dev分支到本地   git checkout -b dev origin/dev
然后把 本地的 dev分支 push 到远程  git push origin dev

推送失败：先使用git pull 把最新的提交从远程仓库分支 dev上抓下来，然后，在本地合并，解决冲突，再推送

如果没有指定本地dev分支和远程origin/dev分支的链接，设置dev和origin/dev的链接
git branch --set-upstream-to=origin/dev dev

再次执行 git pull 合并有冲突 需要手动解决，然后再提交，再git push origin dev

git tag v1.0 用于新建一个标签 默认是HEAD 也可以指定一个commit id   （git tag v0.9  f52c633）
git tag -a v1.1 -m "打标签"  指定标签信息
git tag 可以查看所有标签
