### ssl 一键生成证书脚本：

##### 第一步：安装脚本

```sh
wget -O -  https://get.acme.sh | sh -s email=vx91586x@qq.com
```
#### 第二步：生成证书80端口验证方式（保证80未被占用）

```sh
~/.acme.sh/acme.sh  --issue -d www.baidu.com   --standalone
```

#### 第三步：将证书移动，指定的文件中（nginx中）

```sh
~/.acme.sh/acme.sh --installcert -d www.baidu.com --key-file /root/ssl/private.key --fullchain-file /root/ssl/cert.crt

```

### 第二种生成方式：（http验证）后面的目录要是网站的根目录，同样需要把移动到指定的文件夹目录

```sh
~/.acme.sh/acme.sh  --issue  -d mydomain.com -d www.mydomain.com  --webroot  /home/wwwroot/mydomain.com/
```

