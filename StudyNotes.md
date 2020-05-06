# Git 基本用法



如果你要参与到某个项目中，你可以克隆（clone）该项目的 Git 仓库，然后就像这个项目只有你本地一个版本一样对项目进行修改。全部人都是在本地进行开发，然后向共同的目标推送或者拉取更新。



## 读取操作

你也许注意到了，在某些服务平台上，会同时提供 SSH 和 HTTPS 链接。只有当你拥有仓库的写权限时，你才可以使用 SSH。否则的话，你必须使用 HTTPS URL。

### 克隆仓库 git clone

```bash
git clone https://github.com/USER/project.git  [$HOME/my_dir]
```



### 检查更新 git pull

使用 git pull 命令来查看项目有没有更新

```bash
cd $HOME/my_dir
git pull
```



## 写操作

### 新建仓库

```bash
mkdir ~/jupiter  # 创建目录
cd ~/jupiter     # 进入目录
git init .       # 初始化你的新 Git 工作区
```

在本地的 Git 仓库中，一个文件可以有以下这三种状态：

- 未跟踪文件（Untracked）：你在仓库里新建了一个文件，但是你没有把文件加入到 Git 的管理之中。
- 已跟踪文件（Tracked）：已经加入到 Git 管理的文件。
- 暂存区文件（Staged）：被修改了的已跟踪文件，并加入到 Git 的提交队列中。

使用`git status`查看当前目录文件的状态



### 作业管理

```bash
# 标记文件为‘已跟踪’并保存当前内日到暂存区(stage)
git add FILE_NAME从

# 从暂存区撤回作业
git rm --cached FILE_NAME

# 从暂存区提交至仓库  
git commit FILE_NAME

# 修改后再次提交至stage 
git add FILE_NAME

# 再次提交
git commit -m "COMMENTS" FILE_NAME
```

