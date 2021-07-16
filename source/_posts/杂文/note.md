---
title: 重要的笔记
tag: 笔记
category: 笔记
---

记录一些重要的笔记


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

### ngin
```
sudo yum install epel-release
sudo yum install nginx
sudo systemctl enable nginx // 设置开机启动
Created symlink from /etc/systemd/system/multi-user.target.wants/nginx.service to /usr/lib/systemd/system/nginx.service.  // 软连接
sudo systemctl start nginx  // 启动
sudo systemctl status nginx // nginx运行状态
nginx -t 
nginx -s reload
```

### 端口查看 || 内存
```
netstat -tunlp|grep 15692

```

### Git配置
```
// 保存账号密码
git config credential.helper store
// 设置切换SSR代理
git config --global https.proxy http://127.0.0.1:1081
git config --global https.proxy https://127.0.0.1:1081



//   取消
git config --global --unset http.proxy
git config --global --unset https.proxy

// 设置局部登录用户
git config user.name "A"
git config user.email "A@hotmail.com"

// 本地修改了一些文件 (并没有使用 git add 到暂存区)，想放弃修改
git checkout -- filename // 单个文件/文件夹：
git checkout .  所有文件/文件夹：

// 本地新增了一些文件 (并没有 git add 到暂存区)，想放弃修改
rm  -rf filename //单个文件/文件夹：
git clean -xdf  // 所有文件
git clean -xdff // 所有文件和文件夹

// 本地修改/新增了一些文件，已经 git add 到暂存区，想放弃修改
git reset HEAD filename //单个文件/文件夹
git reset HEAD . // 所有文件/文件夹：

// 本地通过 git add 和 git commit 后，想要撤销此次 commit

git reset commit_id  // 撤销 commit, 同时保留该 commit 修改
git reset --hard commit_id //撤销 commit, 同时本地删除该 commit 修改
【git子模块设置】https://www.jianshu.com/p/9000cd49822c

```



### v2ray 服务器配置
点击查看[https://v2raytech.com/centos-one-click-install-v2ray/]
```
 6 Nov 10:56:20 ntpdate[1435]: no server suitable for synchronization found
 v2ray安装成功！
============================================
 v2ray运行状态： 正在运行
 v2ray配置文件： /etc/v2ray/config.json

 v2ray配置信息：               
   IP(address):   1035.1002.2100.2032
   端口(port)： 23654
   id(uuid)： 7c1d74e6-63f4-4fd6-b918-a9818f8e9ed5
   额外id(alterid)：  76
   加密方式(security)：  auto
   传输协议(network)：  tcp

 vmess链接:  vmess://eyAidiI6IjIiLCAicHMiOiIiLCAiYWRkIjoiMTAzLjEwMC4yMTAuMjAzIiwgInBvcnQiOiIyMzY1NCIsICJpZCI6IjdjMWQ3NGU2LTYzZjQtNGZkNi1iOTE4LWE5ODE4ZjhlOWVkNSIsICJhaWQiOiI3NiIsICJuZXQiOiJ0Y3AiLCAidHlwZSI6Im5vbmUiLCAiaG9zdCI6IiIsICJwYXRoIjoiIiwgInRscyI6IiIgfQ==
```


### 响应试网站设计
[文章地址]https://juejin.cn/post/6844903814332432397
 

### 文件预览系统
[文件预览系统]https://kkfileview.keking.cn/zh-cn/docs/production.html


### WebSocket
[websocket]https://juejin.cn/post/6844903655221493774

### HTTPS 申请
https://juejin.cn/post/6844903957165244430


### redis 开机自动启动
Mac设置redis开机启动[https://www.jianshu.com/p/afb1b1796cc6]

### 安装rabbitmq
