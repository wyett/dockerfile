6ASU9_oracle.repo是oracle 6.9版本的yum源信息，可自行配置；



在本容器中，仅与tar命令有关，所以也可以将

```shell
RUN \
  rm -r -f /etc/yum.repos.d/*

COPY ./6ASU9_oracle.repo /etc/yum.repos.d/
```



改成

```shell
COPY tar.x86_64.rpm /opt/
RUN rpm -ivh tar.x86_64.rpm
```

