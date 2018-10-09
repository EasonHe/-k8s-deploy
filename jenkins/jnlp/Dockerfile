FROM cnych/jenkins:jnlp
ENV MAVEN_VERSION 3.5.4
ENV JAVA_HOME /usr/java/jdk1.8.0_181
ENV MAVEN_HOME /opt/apache-maven-${MAVEN_VERSION}
ENV CLASSPATH .:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar

# build java
COPY ./jdk1.8.0_181 ${JAVA_HOME}


# build maven
COPY apache-maven-${MAVEN_VERSION} /tmp/apache-maven-${MAVEN_VERSION}
USER root:root
RUN mkdir -p /opt/ \
    && /bin/mv /tmp/apache-maven-${MAVEN_VERSION} /opt/

ENV PATH ${MAVEN_HOME}/bin:${PATH} 
