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





测试dev分支和master分支出现冲突，就是当两个分支都更改了的时候
git merge --no-ff -m "" dev//合并分支禁用fast forward


