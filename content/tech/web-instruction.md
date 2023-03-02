---
title: "网站搭建指南"
date: 2023-03-01T15:42:55+08:00
# weight: 1
# aliases: ["/first"]
tags: ["web"]
author: "silverxb"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "搭建过程中的注意事项"
canonicalURL: "http://silverxb.xyz/tech/web-instruction"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    # image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/silverzdz/mypage/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

## hugo
```shell
# hugo new site mypage
hugo server
hugo
```

## 内容修改
* 主页标题：`config.yaml`
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

## 文档头范例
```yaml
---
title: "Test Post"
date: 2023-03-02
# weight: 1
# aliases: ["/first"]
tags: ["test"]
author: "silverxb"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "content test"
canonicalURL: "http://silverxb.xyz/others/test-post"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
ShowCodeCopyButtons: true
cover:
    # image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/silverzdz/mypage/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---
```