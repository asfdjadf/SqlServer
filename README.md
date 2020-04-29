# 安装 SQL Server
`wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -`

`sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/18.04/mssql-server-2019.list)" `

`sudo apt-get update`

`sudo apt-get install -y mssql-server`

`sudo /opt/mssql/bin/mssql-conf setup`

`systemctl status mssql-server --no-pager`

#  安装 SQL Server 命令行工具

`curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -`

` curl https://packages.microsoft.com/config/ubuntu/18.04/prod.list | sudo tee /etc/apt/sources.list.d/msprod.list `

`sudo apt-get update `
`sudo apt-get install mssql-tools unixodbc-dev`
## 将工具更新
`sudo apt-get update` 
`sudo apt-get install mssql-tools`
## 添加环境变量
`/opt/mssql-tools/bin/`

`echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bash_profile`

`echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bashrc`

`source ~/.bashrc`

## 使用 SQL Server 名称 (-S)，用户名 (-U) 和密码 (-P) 的参数运行 sqlcmd 。 在本教程中，用户进行本地连接，因此服务器名称为 localhost。 用户名为 SA，密码是在安装过程中为 SA 帐户提供的密码。

`sqlcmd -S localhost -U SA -P '<YourPassword>`

`如果成功，应会显示 sqlcmd 命令提示符：1>`
