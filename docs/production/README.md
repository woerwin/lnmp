# 配置

假设我们在 `开发环境` 中已经将 PHP 项目测试完毕，并推送到了 `GitHub`，准备在生产环境部署。

## 单机

单机环境中通过 `数据卷` 将 `项目文件` 挂载到容器中。

将 GitHub 上的 PHP 项目克隆到 `./app` 目录下，之后安装依赖 `./lnmp-docker.sh composer` 交互式填入路径。

在 `./config/nginx/*.conf` 增加 nginx 配置。

执行 `./lnmp-docker.sh production`。

## 集群

直接将 PHP 项目打入镜像，以容器方式 (`Dockerfile`) 交付。

## PHP

* 生产环境不启用 `xdebug` 扩展

## Docker 私有仓库

Docker 镜像分发可以使用 Docker 私有仓库。

>注意这里为了表述方便将 git 统一称为 GitHub，实际项目可能不开源，会推送到私有 git 仓库中，请读者知悉。