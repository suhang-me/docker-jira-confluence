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

## jira破解
```shell
docker exec jira-service java -jar /var/agent/atlassian-agent.jar \
    -d \
    -p jira \
    -m suhang@abuse.com \
    -n suhang@abuse.com \
    -o SUHANG \
    -s B5PB-W0H5-2O87-0IIA
```

## jira插件破解
```shell
docker exec jira-service java -jar /var/agent/atlassian-agent.jar \
    -d \
    -p eu.softwareplant.biggantt \
    -m Hello@world.com \
    -n Hello@world.com \
    -o your-org \
    -s you-server-id-xxxx
```

## confluence破解
```shell
docker exec confluence-service java -jar /var/agent/atlassian-agent.jar \
    -d \
    -p conf \
    -m suhang@abuse.com \
    -n suhang@abuse.com \
    -o SUHANG \
    -s B6Z2-DF5X-VLUM-OAGQ
```

## confluence插件破解
```shell
docker exec confluence-service java -jar /var/agent/atlassian-agent.jar \
    -d \
    -p csdn.confluence.languagepatch.zh_CN \
    -m suhang@abuse.com \
    -n suhang@abuse.com \
    -o SUHANG \
    -s B6Z2-DF5X-VLUM-OAGQ
```