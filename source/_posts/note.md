---
title: 重要的笔记
tag: 笔记
category: 笔记
---
## 服务器node相关服务

### 安装node环境

``` bash
1.  curl --silent --location https://rpm.nodesource.com/setup_12.x | sudo bash -
2.sudo yum -y install nodejs
3.node -v
```

### 拷贝代码

``` bash
0.git config credential.helper store
1.cd  /alidata1/taopiao;  git clone https://github.com/kukeblue/vote_frontend.git
2.cd vote_frontend; -> npm install yarn -g; -> yarn
```

### 安装pm2

``` bash
npm install -g pm2
```