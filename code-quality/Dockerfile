FROM sonarqube:5.6.3

EXPOSE 9000
EXPOSE 9092

ENV SONARQUBE_HOME /opt/sonarqube
#ENV SONARQUBE_JDBC_USERNAME sonar
#ENV SONARQUBE_JDBC_PASSWORD sonar
#ENV SONARQUBE_JDBC_URL jdbc:h2:tcp://localhost:9092/sonar

RUN mv /opt/sonarqube/extensions/plugins /opt/sonarqube/extensions/plugins-orig
RUN rm -rf /opt/sonarqube/extensions/plugins && mkdir /opt/sonarqube/extensions/plugins
ADD plugins-download/* /opt/sonarqube/extensions/plugins/
