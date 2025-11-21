FROM eclipse-temurin:11-jre AS runtime

ARG SPRING_PROFILES_ACTIVE=dev
ENV SPRING_PROFILES_ACTIVE=${SPRING_PROFILES_ACTIVE}

WORKDIR /app

COPY target/proxy-client-v0.1.0.jar proxy-client.jar

EXPOSE 8900

ENTRYPOINT ["java", "-Dspring.profiles.active=${SPRING_PROFILES_ACTIVE}", "-jar", "proxy-client.jar"]
