FROM eclipse-temurin:11-jre AS runtime

ARG SPRING_PROFILES_ACTIVE=dev
ENV SPRING_PROFILES_ACTIVE=${SPRING_PROFILES_ACTIVE}

WORKDIR /app

COPY target/shipping-service-v0.1.0.jar shipping-service.jar

EXPOSE 8600

ENTRYPOINT ["java", "-Dspring.profiles.active=${SPRING_PROFILES_ACTIVE}", "-jar", "shipping-service.jar"]
