FROM openjdk:8-jre-alpine


ADD *.war app.war

RUN sh -c 'touch /app.war'

RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone

EXPOSE 8761 8861  5701/udp

CMD ["java","-Djava.security.egd=file:/dev/./urandom -Xms512m -Xmx512m -Xss256k","-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=8861","-jar","/app.war"]
