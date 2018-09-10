1）开启mysql的远程登录

默认情况下mysql为安全起见，不支持远程登录mysql，所以需要设置开启     远程登录mysql的权限

登录mysql后输入如下命令：

[grant all privileges on *.* to 'root' @'%'identified by 'root';](undefined)

[flush privileges;](undefined)

 

2）开放Linux的[对外访问的端口3306](undefined)

[/sbin/iptables -I INPUT -p tcp --dport 3306-j ACCEPT](undefined)

[/etc/rc.d/init.d/iptables save](undefined) ---将修改永久保存到防火墙中