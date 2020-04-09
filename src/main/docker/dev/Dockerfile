FROM openjdk:8-jre-alpine


ADD *.war app.war

RUN sh -c 'touch /app.war'

RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone

EXPOSE 8761


ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom ","-jar","/app.war"]
