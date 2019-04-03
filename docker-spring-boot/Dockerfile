FROM openjdk:8
ADD ../docker-spring-boot
RUN ./docker-spring-boot/mvnw clean install
#copy from target to root
RUN cp /docker-spring-boot/target/docker-spring-boot.jar docker-spring-boot.jar
EXPOSE 8085
ENTRYPOINT ["java", "-jar", "docker-spring-boot.jar"]