# 使用 Git 将本地代码上传到 GitHub 仓库的指南

## 1. 创建 GitHub 仓库

1. 登录到您的 GitHub 账户。
2. 在右上角，点击加号（+）并选择“New repository”。
3. 输入仓库名称，选择公开或私有，然后点击“Create repository”。

## 2. 设置本地 Git 仓库

### 2.1 安装 Git

首先，确保您已经安装了 Git。您可以从 [Git 官方网站](https://git-scm.com/) 下载并安装。

### 2.2 初始化本地 Git 仓库

在您的项目文件夹中打开终端（或命令提示符）并运行以下命令：

```bash
git init
```

## 3. 将本地仓库与 GitHub 仓库关联

在您的终端中，将本地仓库与 GitHub 仓库关联：

```bash
git remote add origin <GitHub 仓库的 URL>
```

请将 `<GitHub 仓库的 URL>` 替换为您在 GitHub 上创建的仓库的 URL。例如：

```bash
git remote add origin https://github.com/yourusername/your-repo-name.git
```

## 4. 添加文件并提交更改

将文件添加到本地仓库并提交更改：

```bash
git add .
git commit -m "Initial commit"
```

## 5. 将本地代码推送到 GitHub 仓库

将代码推送到 GitHub 仓库的 `master` 分支：

```bash
git push -u origin master
```

如果您使用的是 GitHub 的默认分支（通常是 `main`），请将 `master` 替换为 `main`：

```bash
git push -u origin main
```

# 常用 Git 指令

## 配置 Git

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## 创建和克隆仓库

```bash
git init                   # 初始化新的 Git 仓库
git clone <repository>     # 克隆远程仓库
```

## 记录变更

```bash
git add <file>             # 添加指定文件到暂存区
git add .                  # 添加当前目录下的所有文件到暂存区
git commit -m "Message"    # 提交暂存区中的文件
```

## 查看状态和历史

```bash
git status                 # 查看工作目录状态
git log                    # 查看提交历史
```

## 分支操作

```bash
git branch                 # 列出所有分支
git branch <branch>        # 创建新分支
git checkout <branch>      # 切换到指定分支
git merge <branch>         # 合并指定分支到当前分支
```

## 远程仓库操作

```bash
git remote -v              # 查看所有远程仓库
git remote add <name> <url> # 添加远程仓库
git fetch <name>           # 从远程仓库获取最新版本
git pull                   # 拉取远程仓库的更改并合并
git push                   # 推送本地更改到远程仓库
```

## 撤销操作

```bash
git reset <file>           # 取消对文件的暂存
git checkout -- <file>     # 撤销对文件的修改
git revert <commit>        # 撤销指定的提交
```

## 删除操作

```bash
git rm <file>              # 删除指定文件
git rm -r <directory>      # 删除指定目录
```

## 其他常用操作

```bash
git stash                  # 暂存当前工作目录的修改
git stash pop              # 恢复最近一次的 stash 并删除它
```
