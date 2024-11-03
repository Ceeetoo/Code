# Git 使用指南

本文档用于记录 Git 的使用方法和常用命令。

## .gitignore 文件

`.gitignore` 文件用于记录不需要被 Git 管理的文件，这些文件不会被提交到远程仓库。

使用方法：
1. 在 Git 仓库的根目录下创建 `.gitignore` 文件
2. 在文件中添加需要忽略的文件路径，每行一个路径
   例如：`/CODE/Readme.md`

## 基础命令

- `git init`：初始化一个 Git 仓库
- `git clone <url>`：克隆远程仓库到本地
- `git add <file>`：添加文件到暂存区（命令只是保存，并没有提交到远程仓库）
- `git commit -m "message"`：提交更改到本地仓库
  > 注：这会打开 Vim 编辑器，按 `i` 进入编辑状态，编辑完成后按 `Esc` 退出编辑状态，然后输入 `:wq` 保存并退出
- `git status`：查看仓库当前状态
- `git log`：查看提交历史

## 版本控制与提交信息

- `git log`：查看所有提交历史，每个提交都有唯一的 commit ID
- `git show <commit-id>`：查看某个提交的具体修改内容
- `git commit -m "type: message"`：提交时添加备注信息，type 可以是：
  - `feat`：新功能
  - `fix`：修复 bug
  - `docs`：文档更新
  - `style`：代码格式修改
  - `refactor`：代码重构
  - `test`：测试用例修改
  - `chore`：其他修改
- `git commit`：打开编辑器编写详细的提交信息
- `git checkout <commit-id>`：回到指定的历史版本
- `git checkout master`：返回到最新版本
- `git revert <commit-id>`：创建一个新的提交来撤销指定提交的修改

## 分支操作

- `git branch`：查看分支列表
- `git branch <name>`：创建新分支
- `git checkout <branch>`：切换分支
- `git merge <branch>`：合并指定分支到当前分支

## 远程仓库操作

- `git remote add origin <url>`：添加远程仓库
- `git push`：推送本地更改到远程仓库
- `git pull`：拉取远程更改到本地
- `git fetch`：获取远程仓库信息

## 其他常用命令

- `git diff`：查看文件变化
- `git reset`：重置当前 HEAD 到指定状态
- `git stash`：暂存当前修改
- `git tag`：标签管理