# macbook 中使用命令

#### 如果你删除了很多文件，并且想删除所有状态为 '!' (missing) 的文件：
```sh
svn status | grep '^!' | sed 's/^! *//' | xargs svn delete
```
#### 添加新增的文件
```sh
svn status | grep '^?' | sed 's/^? *//' | xargs svn add
```
