## 日常（add → commit → push → pull）

1. `git add <文件>` / `.` / `-A`/ `-u`  — 暂存
2. `git add -p <文件>` — 分块选择暂存，逐个确认
3. `git commit -m "信息"` / `--amend` — 提交 / 修改上次提交
4. `git push [-u origin main]` — 推送到远程
5. `git pull [--rebase]` — 拉取远程更新

## 查看

1. `git status [-s]` — 工作区状态
2. `git log [--oneline] [--graph] [--all] [-5]` — 提交历史
3. `git diff [--staged]` — 比较差异
4. `git reflog` — 查看 HEAD 移动记录
5. `git blame <文件>` — 每行最后修改者
6. `git show <哈希>` — 显示一次提交的完整信息
7. `git show --stat <哈希>` — 只看该提交改了哪些文件
8. git log HEAD..origin/main  — 看有哪些新提交

## 撤销

1. `git restore <文件>` — 丢弃工作区修改
2. `git restore --staged <文件>` — 取消暂存
3. `git reset --soft/mixed/hard HEAD~1` — 回退提交
4. `git revert <哈希>` — 反向提交（安全回退远程）
5. `git stash [pop/list/apply/drop]` — 暂存/恢复工作区
6. `git clean -fdxn` — 删除所有未跟踪文件和目录
7. `--abort` — 放弃本次合并

## 分支

1. `git branch [-a] [-v] [-vv]` — 查看分支
2. `git switch [-c] <分支>` — 切换 / 创建并切换
3. `git merge <分支>` — 合并到当前分支
4. `git branch -d/-D <分支>` — 删除本地分支
5. `git push origin --delete <分支>` — 删除远程分支

## 远程

1. `git remote [-v]` — 查看远程仓库
2. `git remote add origin <地址>` — 添加远程
3. `git remote set-url origin <地址>` — 修改远程地址
4. `git fetch [origin main]` — 拉取远程信息（不合并）
5. `git push --force-with-lease` — 更安全的强制推送
6. `closes #1` — 自动关闭 #1 号 Issue

## 创建 / 获取

1. `git init` — 初始化仓库
2. `git clone <地址> [目录]` — 克隆远程仓库

## 配置

1. `git config --global user.name "名字"` — 设置用户名
2. `git config --global user.email "邮箱"` — 设置邮箱
3. `git config --list` — 查看所有配置

## 其他

1. `git tag [-a v1.0 -m "信息"]` / `git push origin --tags` — 标签
2. `git rebase [main / -i HEAD~3]` — 变基
3. `git cherry-pick <哈希>` — 挑选提交
4. `.gitignore` — 忽略文件：`*.o  build/  .vscode/`

## 提交前缀

1. `feat:` — 新功能
2. `fix:` — 修 bug
3. `docs:` — 文档
4. `style:` — 格式
5. `refactor:` — 重构
6. `perf:` — 性能
7. `test:` — 测试
8. `chore:` — 杂项
