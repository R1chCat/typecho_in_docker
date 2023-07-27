# typecho_in_docker
使用Docker一键部署Typecho,之前搜了一些项目现在都运行不起来了，然后重新写了这个项目

# 使用方法
```bash
git clone https://github.com/R1chCat/typecho_in_docker.git ## 克隆本项目
cd typecho_in_docker
git clone https://github.com/typecho/typecho.git ## 克隆typecho
```

修改nginx配置`conf/nginx/blog.conf`中的`server_name`为你的域名
然后运行容器
```bash
docker-compose up -d
```

如果遇到文件不可写时请进入两个容器执行
```bash
chown -R www-data:www-data /data/wwwroot/typecho
```