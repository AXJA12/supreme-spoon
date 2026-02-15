# supreme-spoon
我已经学会Github啦！真简单！！实在是太简单了！
你需要一份纯 Markdown 格式的 Git 常用命令速查表，方便直接复制、保存或打印，我按使用场景分类整理，结构清晰且保留所有核心命令：
---------------------------------------------这是在线编辑内容
```markdown
# Git 常用命令速查表
## 一、基础配置与初始化
| 命令 | 作用 | 示例 |
|------|------|------|
| `git config --global user.name "你的名字"` | 配置全局用户名 | `git config --global user.name "ZhangSan"` |
| `git config --global user.email "你的邮箱"` | 配置全局邮箱 | `git config --global user.email "zhangsan@xxx.com"` |
| `git config --list` | 查看所有 Git 配置信息 | - |
| `git init` | 在当前目录初始化本地 Git 仓库 | - |
| `git clone <仓库地址>` | 克隆远程仓库到本地 | `git clone https://github.com/xxx/xxx.git` |

## 二、日常工作核心操作
| 命令 | 作用 | 示例 |
|------|------|------|
| `git status` | 查看工作区文件状态（未跟踪/已修改/暂存） | - |
| `git add <文件名>` | 将指定文件添加到暂存区 | `git add index.html` |
| `git add .` | 将当前目录所有修改文件添加到暂存区 | - |
| `git commit -m "提交说明"` | 提交暂存区文件到本地仓库（必须带说明） | `git commit -m "修复登录按钮样式问题"` |
| `git commit --amend` | 修改最后一次提交的说明（未推远程时使用） | - |
| `git log` | 查看完整提交历史（按 q 退出） | - |
| `git log --oneline` | 简洁版提交历史（每行一个提交记录） | - |
| `git diff` | 查看工作区与暂存区的文件差异 | - |
| `git diff --staged` | 查看暂存区与上一次提交的文件差异 | - |

## 三、分支管理
| 命令 | 作用 | 示例 |
|------|------|------|
| `git branch` | 查看本地所有分支（* 标记当前分支） | - |
| `git branch -a` | 查看本地 + 远程所有分支 | - |
| `git branch <分支名>` | 创建新分支（不切换） | `git branch feature/login` |
| `git checkout <分支名>` | 切换到指定分支 | `git checkout feature/login` |
| `git checkout -b <分支名>` | 创建并切换到新分支（常用） | `git checkout -b feature/login` |
| `git merge <分支名>` | 将指定分支合并到当前分支 | `git merge feature/login` |
| `git branch -d <分支名>` | 删除本地已合并的分支 | `git branch -d feature/login` |
| `git branch -D <分支名>` | 强制删除本地未合并的分支 | `git branch -D feature/login` |

## 四、远程仓库操作
| 命令 | 作用 | 示例 |
|------|------|------|
| `git remote -v` | 查看远程仓库地址（fetch/push） | - |
| `git remote add origin <仓库地址>` | 关联本地仓库与远程仓库 | `git remote add origin https://github.com/xxx/xxx.git` |
| `git pull origin <分支名>` | 拉取远程分支代码并合并到本地 | `git pull origin main` |
| `git push origin <分支名>` | 推送本地分支代码到远程仓库 | `git push origin main` |
| `git push -u origin <分支名>` | 推送并关联远程分支（首次推送新分支用） | `git push -u origin feature/login` |
| `git fetch origin` | 拉取远程仓库最新信息（不自动合并） | - |

## 五、撤销与回滚
| 命令 | 作用 | 适用场景 |
|------|------|----------|
| `git checkout -- <文件名>` | 丢弃工作区该文件的修改 | 未暂存的修改 |
| `git reset HEAD <文件名>` | 撤销暂存区的修改，放回工作区 | 已暂存但未提交 |
| `git reset --hard HEAD^` | 回退到上一个版本，丢弃所有未提交修改 | 提交后想撤销 |
| `git reset --hard <commit-id>` | 回退到指定提交版本（commit-id 可从 log 查） | 精确回滚历史版本 |
| `git revert <commit-id>` | 生成新提交，撤销指定版本的修改（保留历史） | 已推远程的提交回滚 |

## 六、其他实用命令
| 命令 | 作用 |
|------|------|
| `git stash` | 暂存当前未提交的修改（切换分支时用） |
| `git stash pop` | 恢复最近一次暂存的修改 |
| `git stash list` | 查看所有暂存记录 |
| `git tag <标签名>` | 给当前提交打标签（如版本号） |
| `git tag -d <标签名>` | 删除本地标签 |
| `git show <commit-id/tag>` | 查看提交/标签的详细信息 |
```

### 总结
1. 这份 Markdown 速查表按「配置→日常操作→分支→远程→撤销→其他」分类，覆盖新手 90% 以上的使用场景；
2. 命令示例贴近实际开发，关键参数（如 `commit-id`、分支名）标注清晰，便于替换使用；
3. 可直接复制到 Markdown 编辑器、笔记软件（如 Typora、Obsidian）中，也可导出为 PDF/图片格式打印。
