---
title: Linux
---
只有root可以添加用户，用户有一个主组，多个所属组

## 基础命令

### 命令格式

``` bash
$ 命令名+空格+参数  如ls -al / tmp 列出所有文件及权限
```
### 开关机

``` bash
$ 重启reboot=init 6=shutdown -r
        关机init 0=shutdown -h now=shutdown half poweroff 
        退出 logout exit=exit
```

### linux用户/用户组权限

``` bash
> useradd wu 新建用户
> passwd 123 修改用户密码
> su root 切换用户
> userdel wu 删除用户
> usermod 修改用户信息
> userdel -r -f 用户名 强制删除用户
> Groupadd 选项 用户组  添加新的用户组
> Groupdel 用户组     删除用户组
> Passwd -l 锁定账号，禁用口令
> Passwd -u 解锁     
> passwd -d  删除密码   
> passwd -f   强制执行  
> passwd -S  显示密码信息
```
### 文件/文件夹权限
``` bash
$ chmod修改当前文件或文件夹的权限
> 例：chmod +x 文件/文件夹
$ chown修改当前文件或文件夹的所属用户
> 例：chown root:root /tmp/tmp1
> chown -R root:root /tmp/tmp1
```
#### 权限命令
``` bash
$ rwx在系统中对应一个个的值
> r-4,w-2,x-1
> r可以读取显示显示文件内容，w可以向文件内写入删除内容，x可以运行这个文件
```

### 常用命令
``` bash
> whoami 查看当前用户
> tar 压缩和解压文件
> netstat 查看网络状态
> nslookup 查看dns信息
> ps 查看运行的程序
> top 实时查看运行的程序
> service 使用service控制服务启动关闭
> curl 来获取网页，可以使用输出重定向来下载文件
> wget 下载文件