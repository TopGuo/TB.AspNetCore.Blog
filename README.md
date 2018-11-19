# TB.AspNetCore.Blog
这个仓库主要用做我再工作学习中，关于aspnetcore上的一下记录--by top

# EF Core

## dbfrist
//该命令用于在cli执行
1. dotnet ef dbcontext scaffold "Server=localhost;Database=ef;User=root;Password=123456;" "Pomelo.EntityFrameworkCore.MySql"

## codefrist
//该命令用于在cli执行
1. dotnet ef migrations add InitialCreate //运行 dotnet ef migrations add InitialCreate 以为迁移搭建基架，并为模型创建一组初始表
2. dotnet ef database update //运行 dotnet ef database update 以将新迁移应用到数据库。 在应用迁移之前，此命令可创建数据库。
//该命令用于在PM中执行迁移
1. Add-Migration Xxx //生成迁移的类
2. Script-Migration //生成迁移的sql脚本--这步可省略
3. Update-Database -Verbose //迁移到书库
## 在执行3的时候，可能出现mysql 1045 access defined 拒绝远程连接的问题
1. 登录你的服务器，进入mysql 授权，命令如下：
``` GRANT ALL PRIVILEGES ON *.* TO'root'@'%' IDENTIFIED BY '允许远程连接的password' WITH GRANT OPTION; TION; ```

## db frist
//for sqlserver
1. Scaffold-DbContext "Server=(localdb)\mssqllocaldb;Database=Blogging;Trusted_Connection=True;" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models

//for mysql
2.Scaffold-DbContext "Server=xx;Database=db_naem;User=root;Password=xx;" "Pomelo.EntityFrameworkCore.MySql" -OutputDir dir

