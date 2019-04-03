FROM openjdk:8
ADD .mvn .mvn
ADD src src
ADD pom.xml pom.xml
ADD mvnw mvnw
RUN ./mvnw clean install
RUN cp target/docker-spring-boot-0.0.1-SNAPSHOT.jar docker-spring-boot.jar
EXPOSE 8085
ENTRYPOINT ["java", "-jar", "docker-spring-boot.jar"]