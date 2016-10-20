#based off the jenkins image at https://hub.docker.com/_/jenkins/
#but added the plugins needed for the presales team
FROM jenkins

USER root
USER jenkins

#ENV JAVA_OPTS="-Xmx4096m"

COPY plugins.txt /usr/shar/jenkins/plugins.txt

#plugins not found as part of the base installed as part of jenkins 2.19.1
#these not found on Jenkins site
# ali-jenkins-git-plugin:2.32-495 \
ADD http://flynnshome.com/downloads/ALI29/agents/build-integration/jenkins/ali-jenkins-git-plugin.hpi /var/jenkins_home/plugins
RUN /usr/local/bin/install-plugins.sh \
        async-http-client:1.7.24.1 \
        cvs:2.12 \
        depgraph-view:0.11 \
        hp-application-automation-tools-plugin:4.5.0 \
        git-tag-message:1.5 \
        github-oauth:0.24 \
        github-pullrequest:0.1.0-rc9 \
        gitlab-oauth:1.0.9 \
        gradle:1.25 \
        greenballs:1.15 \
        jenkins-multijob-plugin:1.23 \
        jquery:1.11.2-0 \
        jquery-ui:1.0.2 \
        maven-release-cascade:1.3.2 \
        maven-deployment-linker:1.5.1 \
        maven-plugin:2.14 \
        m2release:0.14.0 \
        nunit:0.18 \
        repository:1.3
