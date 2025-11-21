FROM eclipse-temurin:11-jre AS runtime

ARG SPRING_PROFILES_ACTIVE=dev
ENV SPRING_PROFILES_ACTIVE=${SPRING_PROFILES_ACTIVE}

WORKDIR /app

COPY target/service-discovery-v0.1.0.jar service-discovery.jar

EXPOSE 8761

ENTRYPOINT ["java", "-Dspring.profiles.active=${SPRING_PROFILES_ACTIVE}", "-jar", "service-discovery.jar"]
