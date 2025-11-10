#### 添加用户
```sh
ssh-keygen -t rsa -C 'admin@qq.com'
```
#### 第二步：找到公钥文件
```sh
.ssh/id_rsa.pub
```
#### 初始化仓库命令
```sh
git init
```
#### git 全局配置
```sh
git config --global user.name "admin" git config --global user.email "admin@example.com"
```
