# git-note
Try to record the usage of git

### Q1: 如何修改某次提交commit message?

1. `git log   //查看历史提交记录`

2. `复制你需要修改历史记录的commit id`

3. `git rebase -i "commit id"^`

4. `将需要修改的那条记录前缀改为 r,修改完成后 :wq 保存退出`

5. `修改message,修改完成后保存退出`

6. `git push origin branch-name -f  提交修改记录`

### Q2: 如何删除远程branch or tag?

1. `git push origin --delete branch-name`

2. `git push origin :refs/tags/<tagname>`

3. `git push origin --delete $(git tag -l) 删除所有`

### Q3: 如何拉取远程分支代码?

1. `git pull origin branch:branch`

### Q4: 如何合并分支代码(在dev分支上开发,master分支合并dev上线)?

1. `从master 切出分支  git checkout -b dev`

2. `在dev分支开发完成,保存代码后 git checkout master`

3. `git rebase dev -i 合并分支,提交记录`

4. `if 冲突 then  解决冲突,提交冲突 git add 修改的文件`

5. `git rebase --continue 继续合并`

### Q5: 如何查找,添加,删除,重命名远程地址?

1. `添加远程 git remote add 远程名字 远程地址`

2. `删除远程 git remote remove 远程名字`

3. `重命名 git remote 旧名字 新名字`

4. `查询远程 git remote -a`

### Q6: 如何在不提交当前修改的情况下切换分支?

1. `git stash`

### Waiting for updating.......
