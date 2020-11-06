FROM openjdk:8-jdk-alpine

COPY . /var/www/java

WORKDIR /var/www/java

RUN ./gradlew build

RUN ls ./build/libs

ARG JAR_FILE=/var/www/java/build/libs/*.jar

RUN ls ${JAR_FILE}

#COPY ${JAR_FILE} ${WORKDIR}/app.jar

ENTRYPOINT ["java","-jar","/var/www/java/build/libs/gs-spring-boot-docker-0.1.0.jar"]

