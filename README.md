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

