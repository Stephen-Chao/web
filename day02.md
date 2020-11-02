##1. 关于HEAD

    就是一个存盘点,实现版本的控制git将每次的提交串成一条时间线,这条时间线
    就是一条分支,默认只有一条分支,master分支,也叫主分支,而HEAD指向的就是
    当前分支  

##2.分支

####    2.1创建分支
    git branch 分支名
    将当前分支复制一条新的分支
    
#### 2.2 查看当前有哪些分支
    git branch
    显示当前仓库中有哪些分支
    注: 前面有*的表示当前所在分支(HEAD指向的分支)
####2.3切换分支
    git checkout 文件名
    将当前分支切换到指定分支名上
    将HEAD的指向写换到指定分支上
    注: 在一条分支上的修改不会影响到其他分支上的内容
        将master分支复制一条新的分支version1
        然后切换到version1,将version1分支的内容修改,并提交
        在切换回master分支,测试,master分支的内容没有改变
#### 2.4分支的合并
    git merge 分支名称
    将指定名称的分支合并到当前分支
    在master分支上使用git merge version1
    则是将version1的修改全部合并给master
    version1的内容不变
    
#### 2.5删除分支
    git branch -d 分支名
    删除指定名称的分支
    强制删除
    git branch -D 分支名
##3.github社区
https://github.com/
####3.1登录注册
####3.2 创建远程仓库
    登陆后,点击右上角的+,选择new repository
    在repository name中填写远程仓库的名字
    点击create repository
    注: description   是用于描述仓库,可以不写
        public        表示仓库内容公开,private表示私有不公开
        initialize    下的几个多选一个都不勾
####3.3 将远程仓库和本地仓库关联到一起
    打开命令窗口,切换到本地仓库的路径
    git remote add origin 远程仓库的url地址    
    git remote: 固定用法
    add 添加远程仓库
    origin 是一个带名词,表示远程仓库的url    
####3.4 将本地仓库的内容推送到远程仓库中
    git push -u origin master
    git push: 固定用法
    -u: 只在第一次推送时使用,以后就再也不需要添加了
    origin: 代名词,只带上一步关联时的远程仓库的url
