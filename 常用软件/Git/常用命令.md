# 常用命令

- `git merge test` 将test分支合并到当前分支。注意应先检出到你想合并入的分支，然后运行 `git merge` 命令

## 分支相关

- `git checkout -b test` 从当前分支新建test分支，并切换到该test分支

上述命名等价于先新建test分支，再切换到test分支，即：

```bash
git branch test
git checkout test
```
- - `git checkout -b test master` 从指代分支创建新分支，并切换到新分支

- `git branch` 查看本地所有分支

- `git branch -a` 查看本地和远程所有分支

- `git branch -d test` 删除test分支。注意这是删除已经被合并的分支

- `git branch -D test` 强制删除test分支。注意这是删除未被合并的分支

- `git merge test` 将test分支合并到当前分支。注意应先检出到你想合并入的分支，然后运行 `git merge` 命令

- `git remote update origin --prune` 当远程分支发生改动（如新增、删除）时，本地并不能自动的获知这些改动，可以执行该命令更新下分支信息

