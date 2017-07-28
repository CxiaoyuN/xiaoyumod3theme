# xiaoyumod3theme
打开目录cd /www/wwwroot/default/public
git clone https://github.com/mmmwhy/ss_panel_theme.git tmp && mv tmp/.git . && rm -rf tmp && git reset --hard
使用lnmp
使用的是vhost，那么目录应该在cd /usr/local/nginx/conf/vhost/
有一个 域名.conf 文件
- 如果使用默认配置cd /usr/local/nginx/conf/
有一个nginx.conf文件
修改顺序为：
server
    {
        listen 80 default_server;
        #listen [::]:80 default_server ipv6only=on;
        server_name _;
        index index.html index.htm index.php;
        root  /home/wwwroot/default/public;
