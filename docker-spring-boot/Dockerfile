FROM openjdk:8
RUN ./mvnw clean install
ADD target/docker-spring-boot-0.0.1-SNAPSHOT.jar docker-spring-boot.jar
EXPOSE 8085
ENTRYPOINT ["java", "-jar", "docker-spring-boot.jar"]