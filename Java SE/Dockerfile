# I used the path "/usr/src/app" as it is a commonly used path within the container

FROM openjdk:11-jre-slim

WORKDIR /usr/src/app

COPY javase-app.jar .

# Assuming there is a file called "run-tests.sh" on the path "/usr/src/test-scripts/" that we want to run
RUN /usr/src/test-scripts/run-tests.sh

CMD ["java", "-jar", "javase.jar"]