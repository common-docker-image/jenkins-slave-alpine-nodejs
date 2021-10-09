# 构建前端镜像

支持jenkins master节点通过SSH证书方式连接slave容器。

## Running

本地测试：

```bash
$ docker run prong/jenkins-slave-alpine:1.0 "<public key>"
```



## 配合jenkins Docker Plugin使用

进入jenkins master节点管理控制台->系统管理->系统配置，配置Docker参数：

- Docker Image：prong/jenkins-slave-alpine:1.0
- Remote File System Root：/home/jenkins
- Connect method：Connect with SSH
- SSH key：Inject SSH key
- User：jenkins

