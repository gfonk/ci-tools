FROM sonarqube:5.1.2

# assumptions
# - plugins.tgz is the latest plugins download from current production instance

EXPOSE 9000

ENV SONARQUBE_HOME /opt/sonarqube
ENV SONARQUBE_JDBC_USERNAME sonar
ENV SONARQUBE_JDBC_PASSWORD sonar
ENV SONARQUBE_JDBC_URL jdbc:h2:tcp://localhost:9092/sonar

RUN rm -rf /opt/sonarqube/extensions/plugins
ADD plugins.tgz /opt/sonarqube/extensions/
