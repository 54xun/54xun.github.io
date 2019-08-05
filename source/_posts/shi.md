---
title: 搭建LAMP环境
---
LAMP=LINUX+APACHE+MYSQL+PHP，这是Linux下最常见的提供web服务的组合之一
> 浏览器-->提交账户密码-->传输给服务器-->服务器接受处理
Apache是中间件 后端和前端的软件（中间件特性：识别请求。根据客户端请求的内容，判断，是将请求装发给后端还是自己处理，只有请求的文件后缀是PHP、JSP、ASP..可执行的的，才会将请求装发给后端）
Post提交用户名，密码-->apache转交给PHP-->php查询后向数据库中进行查询-->查询成功，就登录成功


### 搭建命令

``` bash
$   yum install httpd
    systemctl enable httpd
    
    systemctl start httpd
    
    firewallcmd --add-pot 80/ tcp --zone=public --permanen:

      yum install mariadb-server

      systemctl enable mar iadb ?systemctl start ma riadb

      mysql_ secure_ init...

      yum install php php-gd php-mysql php-pdo php-*

      systemctl restart httpd

      chown R apache : apache /var/www/html
```
