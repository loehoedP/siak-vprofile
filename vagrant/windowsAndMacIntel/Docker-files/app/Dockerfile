        #Build Image Stage
        FROM maven:3.9.9-eclipse-temurin-21-jammy AS build_image
        RUN git clone --branch containers https://github.com/hkhcoder/vprofile-project.git
        RUN cd vprofile-project && mvn install

        #Service Image Stage
        FROM tomcat:10-jdk21
        LABEL project="chelsea" 
        LABEL app="vprofile"
        LABEL author="loehoedp"
        RUN rm -rf /usr/local/tomcat/webapps/*
        COPY --from=build_image vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

        EXPOSE 8080
        CMD ["catalina.sh", "run"]

