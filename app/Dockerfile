FROM openjdk:11 AS BUILD_IMAGE
RUN apt update && apt install maven -y
RUN git clone https://github.com/abcd0000abcd/SimpleProject.git
RUN cd 

FROM tomcat:9-jre11
LABEL "Project"="VK_Project"
LABEL "Author"="Vishal"
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILD_IMAGE

EXPOSE : 8080
CMD ["cataline.sh"."run"]
