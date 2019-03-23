FROM hotswapagent/hotswap-vm
LABEL maintainer="hotswapagent.org" description="Thorntail hollow"
ENV HOLLOWTHORNTAIL_ARCHIVE microprofile-2.4.0.Final-hollow-thorntail.jar
ENV INSTALL_DIR /opt
RUN curl -o ${INSTALL_DIR}/${HOLLOWTHORNTAIL_ARCHIVE}.jar -L http://repo2.maven.org/maven2/io/thorntail/servers/microprofile/2.4.0.Final/microprofile-2.4.0.Final-hollow-thorntail.jar
ENV HOLLOWTHORNTAIL_HOME ${INSTALL_DIR}
ENV DEPLOYMENT_DIR ${HOLLOWTHORNTAIL_HOME}
ENTRYPOINT java ${JAVA_OPTS} -jar ${HOLLOWTHORNTAIL_ARCHIVE}.jar ${ARCHIVE_NAME} -b=0.0.0.0
WORKDIR ${INSTALL_DIR}
EXPOSE 8080 9990
