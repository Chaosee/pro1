## git 基本操作

> 1. 增删改查 
>
>    ```
>    $ git config --global user.name fany
>    $ git config --global user.email 2539625765@qq.com
>    ```
>
> 2. 配置文件级别 ` --local `  >  ` --global `  >  ` --system `
>
> 3. 增加
>
>    ```
>    $ git config --global --add user.name chaosee
>    ```
>
> 4. 删除
>
>    ```
>    $ git config --global --unset user.name chaosee
>    ```
>
> 5. 改
>
>    ```
>    $ git config --global user.name chaosee
>    ```
>
> 6. 查看
>
>    ```
>    $ git config user.name
>    $ git config --get user.name
>    ```
>
> 7. 查看所有配置
>
>    ```
>    $ git config --list --global
>    ```



## 创建git仓库

> 1.  使用` git init` 创建裸仓库
>
>    ```
>    $ git init 目录(git_non-bare_repo)
>    目录$ git init
>    $ git init -bare 目录(git_bare_repo)
>    ```
>
> 2. 使用` git clone` 将远程的仓库克隆到本地
>
>    ```
>    $ git clone 目录
>    ```



## 文件操作流程

> 工作区、暂存区、历史区` work`>` cache` >	` history` 
>
> 1. 将工作区文件添加到暂存区
>
>    ```\
>    $ touch a
>    $ git add a
>    // 所有
>    $ git add -A
>    $ git add .
>    ```
>
> 2. 查看暂存区
>
>    ```
>    $ git status
>    ```
>
> 3. 将缓存区文件添加到历史区
>
>    ```
>    $ git commit -m '提交信息'
>    ```
>
> 4. 删除工作区、暂存区文件
>
>    ```
>    // 删除工作区、暂存区文件
>    $ git rm 文件
>    // 只删除暂存区文件
>    $ git rm --cached 文件
>    ```
>
> 5. 操作工作区文件, ` rename` ` move`
>
>    ```
>    $ git mv 源文件 目标文件
>    ```
>
> 6. 不将指定文件添加到历史区
>
>    ```
>    $ vim .gitignore
>    // 添加文件筛选
>    *.[da]  文件后缀
>    *`
>    *.pyc   
>    !test.pyc 需要注意的不筛选这个文件
>    foo/      一个foo目录
>    **/res	  所有的res目录，连带子目录
>    
>    ```
>
> 7. 还原
>
>    ```
>    $ git reset HEAD 文件
>    ```
>
> 8. 将历史区文件检出
>
>    ```
>    $ git checkout 文件
>    ```
>
>    ```
>    echo "# pro1" >> README.md
>    git init
>    git add README.md
>    git commit -m "first commit"
>    git remote add origin https://github.com/Chaosee/pro1.git
>    git push -u origin master
>    ```
>
> 9. 查看历史清单
>
>    ```
>    $ git log
>    ```
>
## 远程git操作
> 1. 建立远程仓库
>   ```
>   git remote add origin(自定义远程库名) url
>   ```
>
> 2. 更改文件,将更新上传到远程origin库的master的分支中
>
>    ```
>    git push origin master
>    ```
>
> 3. 下载文件
>
>    ```
>    git pull 
>    ```
>
>

