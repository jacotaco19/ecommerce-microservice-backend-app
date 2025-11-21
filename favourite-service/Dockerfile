FROM eclipse-temurin:11-jre AS runtime

ARG SPRING_PROFILES_ACTIVE=dev
ENV SPRING_PROFILES_ACTIVE=${SPRING_PROFILES_ACTIVE}

WORKDIR /app

COPY target/favourite-service-v0.1.0.jar favourite-service.jar

EXPOSE 8800

ENTRYPOINT ["java", "-Dspring.profiles.active=${SPRING_PROFILES_ACTIVE}", "-jar", "favourite-service.jar"]
