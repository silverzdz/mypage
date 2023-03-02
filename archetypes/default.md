---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
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
description: " "
canonicalURL: "http://silverxb.xyz/{{ replace .Name "-" " " | title }}"
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