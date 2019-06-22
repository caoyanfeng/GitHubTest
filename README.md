# GitHub Guide
**本文记录了GitHub的常用操作**
对于团队协作来讲，好的GitHub使用指南将极大的提高效率。
本文的MarkDown编写基于在线网站：[mdeditor](https://www.mdeditor.com/)。
## 一、GitHub创建仓库
### 1.1注册
### 1.2添加ssh
根目录执行

    ssh-keygen -t rsa -C "18817801185@163.com"
查询ssh

    cyf@cyf-pad:~/.ssh$ cat id_rsa.pub
将内容贴到下图位置
![image](https://github.com/caoyanfeng/GitHubTest/blob/master/images/add_ssh.png)
### 1.3创建仓库
## 二、分支操作
### 2.1创建仓库
    cyf@cyf-pad:~/github/GitHubTest$ git checkout -b dev
切换到一个新分支 'dev'

    cyf@cyf-pad:~/github/GitHubTest$ touch dev_branch.log
    cyf@cyf-pad:~/github/GitHubTest$ git status
位于分支 dev
未跟踪的文件:
  （使用 "git add <文件>..." 以包含要提交的内容）

　　dev_branch.log

提交为空，但是存在尚未跟踪的文件（使用 "git add" 建立跟踪）

    cyf@cyf-pad:~/github/GitHubTest$ git add .
    cyf@cyf-pad:~/github/GitHubTest$ git commit . -m "add log for dev branch"
[dev a4e7f3d] add log for dev branch
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 dev_branch.log

    cyf@cyf-pad:~/github/GitHubTest$ git push -u origin dev
对象计数中: 3, 完成.
Delta compression using up to 4 threads.
压缩对象中: 100% (2/2), 完成.
写入对象中: 100% (3/3), 322 bytes | 322.00 KiB/s, 完成.
Total 3 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/caoyanfeng/GitHubTest/pull/new/dev
remote: 
To github.com:caoyanfeng/GitHubTest.git
 * [new branch]      dev -> dev
分支 'dev' 设置为跟踪来自 'origin' 的远程分支 'dev'。

### 2.2分支推送

    cyf@cyf-pad:~/github/GitHubTest$ git push origin master
对象计数中: 3, 完成.
Delta compression using up to 4 threads.
压缩对象中: 100% (3/3), 完成.
写入对象中: 100% (3/3), 1.24 KiB | 1.24 MiB/s, 完成.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:caoyanfeng/GitHubTest.git
   2328701..c65c540  master -> master
   
    cyf@cyf-pad:~/github/GitHubTest$ git push origin dev
Everything up-to-date
