第一个github测试
测试添加分支
git add 文件名
git commit -m "你提交的描述"
git log //查看你的日志
git reset --hard HEAD^//版本回退，一个^表示回退一次 两个^^ 多个N^即可
git reset --hard commitID//指定回退到提交的那个id，这个id之需要前面几个字符即可
git status //查看当前的状态，哪些需要add 需要提交
git diff HEAD -- 文件//这里是查看文件和最新版本的区别
git checkout -- 文件//将修改了的没有被提交到暂存区的文件恢复到最近的版本的工作区间或者已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态
git reset HEAD 文件//将暂存区的内容撤销到工作区
删除文件
1.rm 文件--》git rm 文件-->git commit -m ""//通过这样的步骤就可以撤销如果你删除失误的话
这个时候（也就是说这个时候只执行了rm test.txt）有两种情况

第一种情况:的确要把test.txt删掉，那么可以执行
                   git rm test.txt
                   git commit -m "remove test.txt"
                   然后文件就被删掉了

第二种情况:删错文件了，不应该删test.txt，注意这时只执行了rm test.txt，还没  
有提交，所以可以执行git checkout test.txt将文件恢复。

git remote add origin git@github.com:michaelliao/learngit.git
//这里是远程库与其本地库相关联 这里的@github.com:michaelliao/learngit.git是你GitHub创建的仓库的地址4
git push -u origin master 把本地内容推送到远程 我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支

git push origin master

克隆远程库：
git clone git @github...你的远程库的地址
创建分支：
git ckeckout -b 分支名 快速创建分支并且切换

git branch 查看当前分支*表示当前HEAD指向的分支
查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>

修改master时





测试dev分支和master分支出现冲突，就是当两个分支都更改
git merge --no-ff -m "" dev//合并分支禁用fast and forward
git stash可以把当前工作现场存储起来等以后恢复现场后继续工作
feature-vulcan分支还没有被合并，如果删除，将丢失掉修改，如果要强行删除，需要使用大写的-D参数。
git branch -D feature-vulcan
修复bug
推送失败的时候
git pull也失败了，原因是没有指定本地dev分支与远程origin/dev分支的链接，根据提示，设置dev和origin/dev的链接：

$ git branch --set-upstream-to=origin/dev dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
再pull：

$ git pull
然后解决冲突后
$ git push origin dev
命令git tag <tagname>用于新建一个标签，默认为HEAD，也可以指定一个commit id；

命令git tag -a <tagname> -m "blablabla..."可以指定标签信息；

命令git tag可以查看所有标签。

命令git push origin <tagname>可以推送一个本地标签；

命令git push origin --tags可以推送全部未推送过的本地标签；

命令git tag -d <tagname>可以删除一个本地标签；

命令git push origin :refs/tags/<tagname>可以删除一个远程标签。




