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

### 端口查看
```
netstat -tunlp|grep 15692
```

### Git切换SSR代理
```
// 设置
git config --global https.proxy http://127.0.0.1:1081
git config --global https.proxy https://127.0.0.1:1081


//   取消
git config --global --unset http.proxy
git config --global --unset https.proxy
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