## git 的使用

### 关系
```html
  本地工作区 -> git add -> 本地缓存区 -> git commit ->本地仓库 -> git push -> 远程仓库 -> git pull -> 本地工作区
```


### 本地仓库操作
```html
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


```
