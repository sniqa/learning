# git 的使用

## git

### 关系

```shell
  本地工作区 -> git add -> 本地缓存区 -> git commit ->本地仓库 -> git push -> 远程仓库 -> git pull -> 本地工作区
```

### 本地仓库操作

```shell

git init       //初始化本地仓库

//与GitHub账号无关
git config --global? user.name [username] //当前项目或全局
git config --global? user.email [useremail] //当前项目或全局

git status  //查看本地库状态

git add [filename | .] //将文件增加到本地缓存区

git commit  -m "commit message" [filename?]    //提交到本地仓库

git log   //查看日志
git log --pretty=oneline  /一行显示
git log --oneline  //一行简略显示，只能
git reflog //带索引的一行显示 部分hash值


git reset [--hard | --soft | --mixid]
git reset --hard HEAD^ 代表回退一个版本
git reset --hard HEAD~[number] 代表回退number个版本

git diff [filename]  //查看修改未add
git diff HEAD [filename]   //查看修改已add


git branch -v //查看所有分支
git branch [branch_name] //新建分支
git checkout [branch_name] //切换分支

//合并分支
  git checkout [branch_name] //接受合并的分支
  git merge [branch_name] //被合并的分支

//冲突解决
  编辑冲突文件，删除特殊符号，保存退出
  git add [filename]
  git commit -m "commit message"

```

### git 远程仓库

```shell
//远程仓库操作
git remote -v //查看远程仓库地址
git remote add [origin] [github地址] //添加一个远程仓库，origin为后面地址的别名

//推送到远程仓库
git push [project_address] [branch_name]

//复制到本地
git clone [project_address]



//开放其他人对项目的push
git_project => collaborators => add collabrator
//上述操作会生成一个链接，当被邀请人确定时，被邀请人即拥有该远程仓库的修改权限

//拉取远程仓库
  pull = fetch + merge
  //获取远程仓库的数据，不对本地仓库进行修改合并
  git fetch [origin] [branch_name]  //下载的远程仓库数据在 [origin]/[branch_name]

  //合并git fetch数据
  git merge [origin]/[branch_name]

  //拉取远程仓库并合并本地仓库
  git pull [origin] [branch_name]


//fork 流程
  A的项目里fork一个到B -> B: {git clone frok_project -> 修改 ->
  git push -> pull request } -> A:{merge}

```
