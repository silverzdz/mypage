# mypage

## hugo
```shell
# hugo new site mypage
hugo server
hugo
```

## 内容修改
* 主页标题：`config.toml`
* 内容：`content/`，注意删除drart项

## 主题
例：
```shell
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
echo "theme = 'PaperMod'" >> config.toml
```

## 部署
* nginx文件参考`nginx.conf`
* 证书：
    ```shell
    sudo apt install nginx
    sudo apt install snap
    sudo snap install core
    sudo snap refresh core
    sudo snap install --classic certbot
    sudo ln -s /snap/bin/certbot /usr/bin/certbot
    sudo certbot --nginx
    ```
* 注意防火墙放行80端口：
    ```shell
    firewall-cmd --zone=public --add-port=80/tcp --permanent
    firewall-cmd --reload
    firewall-cmd --list-ports
    ```