FROM maven:3.9.9-eclipse-temurin-21-jammy as builder
RUN git clone https://github.com/hkhcoder/vprofile-project.git
RUN cd /vprofile-project && git checkout containers && mvn clean package -DskipTests


FROM tomcat:10-jdk21
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=builder /vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war