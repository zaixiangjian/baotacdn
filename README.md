
首先SSH屏蔽域名

# 启动运行
## cdn.com修改为你安装路径一般就是域名
```bash
cd /www/wwwroot/cdn.com/edge-admin
bin/edge-admin start
```
# 可能需要手动放行端口
```bash
sudo ufw allow 7788
sudo ufw allow 8001
```

# 创建一个开机或者重启自启动cdn.com修改为实际路径
```bash
cd /www/wwwroot/cdn.com
touch GoEdge.sh
nano GoEdge.sh
```
# GoEdge.sh内容为下面内容cdn.com修改为你的实际目录
```bash
cd /www/wwwroot/cdn.com/edge-admin
bin/edge-admin start
```
## ctrl+x输入y保存

# 添加开启自启动任务
```bash
crontab -e
```
# 添加下面任务内容
```bash
@reboot /www/wwwroot/cdn.com/GoEdge.sh
```
## ctrl+x输入y保存
激活
```bash
F4BuVYEKSDWV+I13ISd5NUyBcWOlH0af4/ow9obzYBS3XvYC9IsK86k5UDyyBv9vqJWN2/FQTDbPyuAO0zxYlkLDC0c8rrShs+7PAkqM0O8wBIGknzForgidDZahky5Lo/ZWaPZ1dVFUxmV29ykb0I0b4tv7Q3OtnTylOuzf//MYrlvyw6VJQMGnsttmeHzsNL/r0yDONOEXZoGoLZsuBKnkfXt+qt6bZF+kM1ncbh+sY42BrPTWQ12sXqJS3qHlzU0FFl9lTNzLGYYhq5vi/4sJuPVE50/uLCtslTJdb9zOGR915hnM+jHYsR+jUk0QxOqtreaHpsvNuLkexXbkmA==

```








