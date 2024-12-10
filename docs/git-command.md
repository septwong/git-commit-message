以下是常用的 **Git 指令**，分为不同类别整理，方便查阅和学习。

---

### **基础操作**

| 指令                     | 功能                                     |
| ------------------------ | ---------------------------------------- |
| `git init`               | 初始化一个新的 Git 仓库                  |
| `git clone [url]`        | 克隆一个远程仓库到本地                   |
| `git status`             | 查看当前分支的状态                       |
| `git add [file/dir]`     | 添加文件到暂存区（可以是单个文件或目录） |
| `git add .`              | 添加当前目录下所有更改到暂存区           |
| `git commit -m "msg"`    | 提交暂存区的更改，并附加提交说明         |
| `git log`                | 查看提交历史                             |
| `git log --oneline`      | 查看简洁的提交历史                       |
| `git diff`               | 查看工作区与暂存区之间的差异             |
| `git diff [branch/file]` | 查看指定分支或文件的差异                 |

---

### **分支管理**

| 指令                            | 功能                           |
| ------------------------------- | ------------------------------ |
| `git branch`                    | 查看本地分支                   |
| `git branch [branch-name]`      | 创建新分支                     |
| `git branch -d [branch-name]`   | 删除本地分支                   |
| `git branch -D [branch-name]`   | 强制删除本地分支               |
| `git checkout [branch-name]`    | 切换到指定分支                 |
| `git checkout -b [branch-name]` | 创建并切换到新分支             |
| `git merge [branch-name]`       | 将指定分支合并到当前分支       |
| `git rebase [branch-name]`      | 将指定分支的提交变基到当前分支 |

---

### **远程仓库**

| 指令                               | 功能                                 |
| ---------------------------------- | ------------------------------------ |
| `git remote add origin [url]`      | 添加远程仓库                         |
| `git remote -v`                    | 查看远程仓库地址                     |
| `git push origin [branch-name]`    | 推送本地分支到远程仓库               |
| `git push -u origin [branch-name]` | 推送本地分支到远程仓库并设置跟踪关系 |
| `git fetch origin`                 | 拉取远程仓库的更新但不合并           |
| `git pull`                         | 拉取远程仓库更新并合并到当前分支     |
| `git pull origin [branch-name]`    | 拉取指定分支的更新并合并             |
| `git clone [url]`                  | 克隆远程仓库到本地                   |

---

### **标签管理**

| 指令                                    | 功能                   |
| --------------------------------------- | ---------------------- |
| `git tag`                               | 查看所有标签           |
| `git tag [tag-name]`                    | 创建一个轻量标签       |
| `git tag -a [tag-name] -m "msg"`        | 创建一个附带说明的标签 |
| `git push origin [tag-name]`            | 推送标签到远程仓库     |
| `git push origin --tags`                | 推送所有标签到远程仓库 |
| `git tag -d [tag-name]`                 | 删除本地标签           |
| `git push origin :refs/tags/[tag-name]` | 删除远程仓库的标签     |

---

### **回滚与撤销**

| 指令                           | 功能                                     |
| ------------------------------ | ---------------------------------------- |
| `git restore [file]`           | 撤销工作区对文件的更改（未添加到暂存区） |
| `git restore --staged [file]`  | 从暂存区撤销文件                         |
| `git reset [commit-id]`        | 将分支重置到指定提交                     |
| `git reset --hard [commit-id]` | 将分支重置到指定提交，并清空工作区的更改 |
| `git revert [commit-id]`       | 反转指定提交，生成一个新的提交           |
| `git stash`                    | 保存当前工作区的修改为一个栈             |
| `git stash apply`              | 恢复最近一次 `stash` 的更改              |
| `git stash list`               | 查看所有 `stash`                         |
| `git stash drop`               | 删除最近一次 `stash`                     |

---

### **常用配置**

| 指令                                          | 功能                       |
| --------------------------------------------- | -------------------------- |
| `git config --global user.name "Your Name"`   | 配置全局用户名             |
| `git config --global user.email "Your Email"` | 配置全局邮箱               |
| `git config --list`                           | 查看当前的 Git 配置        |
| `git config --global alias.[alias] [command]` | 设置 Git 指令别名          |
| `git config --global core.editor [editor]`    | 设置默认编辑器，比如 `vim` |

---

### **查看和调试**

| 指令                   | 功能                                         |
| ---------------------- | -------------------------------------------- |
| `git show [commit-id]` | 查看某次提交的详细信息                       |
| `git blame [file]`     | 查看每行代码的提交历史                       |
| `git log --graph`      | 以图形化方式显示提交历史                     |
| `git reflog`           | 查看所有的操作历史（包括被删除的分支或提交） |

---

### **清理**

| 指令            | 功能                   |
| --------------- | ---------------------- |
| `git clean -f`  | 删除未跟踪的文件       |
| `git clean -fd` | 删除未跟踪的文件和目录 |

---

### **总结**

Git 提供了强大的版本控制功能，上述命令覆盖了日常开发中最常用的操作。从入门到精通，你可以根据实际需求逐步学习和掌握。
