#Base image of java runtime
FROM openjdk:21-jdk-slim
LABEL authors="Aadit"

#Who maintains the image
#MAINTAINER <name of the maintainer>

#Add the jar to image
COPY target/accounts-0.0.1-SNAPSHOT.jar accounts-0.0.1-SNAPSHOT

#Execute the image
ENTRYPOINT ["java", "-jar", "accounts-0.0.1-SNAPSHOT"]