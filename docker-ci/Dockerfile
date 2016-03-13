FROM liferay-portal:tomcat-6.2-ce-ga6

ENV RELEASE_VERSION=0.00.06 LIFERAY_HOME=/usr/local/liferay-portal-6.2-ce-ga6
ENV TOMCAT_HOME=${LIFERAY_HOME}/tomcat-7.0.62
	
ADD	["http://192.168.99.100:8081/service/local/repositories/liferay-releases/content/com/example/plugins/ci-portlet/2.0.0/ci-portlet-2.0.0.war", "${LIFERAY_HOME}/deploy/"]

EXPOSE 8080

CMD ${TOMCAT_HOME}/bin/startup.sh && tail -f ${TOMCAT_HOME}/logs/catalina.out


