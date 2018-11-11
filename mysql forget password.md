# mysql 忘记登录密码，跳过重置的方法
1. 
#编辑mysql配置文件
vim /etc/my.cnf
2.
#添加
skip-grant-tables
3.
#重启mysql
service mysql restart
#新的mysql执行这个命令
systemctl restart mysqld.service
4.
#连接mysql，直接回车即可，不需要输入密码
mysql -u root -p
5.
#更新root用户密码
update mysql.user set authentication_string=password('123') where user='root' and Host = 'localhost';
6.
#刷新权限
flush privileges;
7.
#去掉/etc/my.cnf文件中的
skip-grant-tables

