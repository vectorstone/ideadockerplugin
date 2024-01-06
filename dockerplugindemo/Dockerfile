# 基础镜像,必须存在
FROM openjdk:8u312-jdk-oracle

# 作者信息
MAINTAINER gavin

#系统编码
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8

# 解决时区的问题
RUN ln -snf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo "Asia/Shanghai" > /etc/timezone

EXPOSE 8111

# 要添加到镜像中的文件
ADD target/dockerplugindemo-0.0.1-SNAPSHOT.jar /dockerplugindemo-0.0.1-SNAPSHOT.jar

# 指定容器内的工作路径为根路径
WORKDIR /

ENTRYPOINT ["java" , "-jar" , "/dockerplugindemo-0.0.1-SNAPSHOT.jar"]