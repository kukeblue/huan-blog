---
title: Docker
tag: Docker
category: Docker
---
[入门到放弃](https://yeasy.gitbook.io/docker_practice/container/daemon)

```
    docker run -d -it -v /home/dock/file:/opt/kkFileView-2.2.1/file -p 8012:8012 keking/kkfileview
    docker run -it -p 8012:8012 -v /opt/paper:/opt/kkFileView-3.3.1/file keking/kkfileview
```