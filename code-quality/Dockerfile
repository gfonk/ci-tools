FROM sonarqube:5.6.3

# assumptions
# - plugins.tgz is the latest plugins download from current production instance

EXPOSE 9000

ENV SONARQUBE_HOME /opt/sonarqube
ENV SONARQUBE_JDBC_USERNAME sonar
ENV SONARQUBE_JDBC_PASSWORD sonar
ENV SONARQUBE_JDBC_URL jdbc:h2:tcp://localhost:9092/sonar

RUN mv /opt/sonarqube/extensions/plugins /opt/sonarqube/extensions/plugins-orig
RUN rm -rf /opt/sonarqube/extensions/plugins && mkdir /opt/sonarqube/extensions/plugins
ADD plugins-download/* /opt/sonarqube/extensions/plugins/
#RUN curl -O https://github.com/SonarQubeCommunity/sonar-sonargraph/releases/download/sonar-sonargraph-plugin-3.5/sonar-sonargraph-plugin-3.5.jar \
#  --output /opt/sonarqube/extensions/plugins/
# ADD plugins.tgz /opt/sonarqube/extensions/
