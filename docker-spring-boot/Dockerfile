FROM openjdk:8
ADD .mvn .mvn
ADD src src
ADD pom.xml pom.xml
ADD mvnw mvnw
RUN ./mvnw clean install
#copy form target to root
RUN cp /target/docker-spring-boot.jar docker-spring-boot.jar
EXPOSE 8085
ENTRYPOINT ["java", "-jar", "docker-spring-boot.jar"]
RUN rm -rf src
RUN rm -rf .mvn
RUN rm -f pom.xml
RUN rm -f mvnw