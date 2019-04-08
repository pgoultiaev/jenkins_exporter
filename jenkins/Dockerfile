FROM jenkins/jenkins:lts
USER root
USER jenkins

ARG JENKINS_USER
ENV JENKINS_USER ${JENKINS_USER:-admin}
ARG JENKINS_PASS
ENV JENKINS_PASS ${JENKINS_PASS:-admin}

COPY security.groovy /var/jenkins_home/init.groovy.d/security.groovy
# COPY jenkins.yaml /var/jenkins_home/jenkins.yaml
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt

ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"