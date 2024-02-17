# 自用的jira和confluence的docker镜像构建项目(带破解)


## docker镜像构建命令
```shell
cd jira
docker build .
docker tag [镜像id] [镜像名称]:[版本号] # docker tag [ImageId] registry.cn-hongkong.aliyuncs.com/suhang-me/jira:9.4.2

docker login --username=[阿里云用户名] registry.cn-hongkong.aliyuncs.com # 登录阿里云香港
docker push [镜像名称]:[镜像版本号] # docker push registry.cn-hongkong.aliyuncs.com/suhang-me/jira:9.4.2

```

## docker拉取镜像
```shell
docker login --username=[阿里云用户名] registry.cn-hongkong.aliyuncs.com # 登录阿里云香港
docker pull [镜像名称]:[镜像版本号] # docker pull registry.cn-hongkong.aliyuncs.com/suhang-me/jira:9.4.2
```