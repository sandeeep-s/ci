FROM anapsix/alpine-java:jdk7

RUN apk update && apk add --update curl

ENV LIFERAY_PARENT_DIR=/usr/local

#RUN curl -O -s -k -L -C - http://downloads.sourceforge.net/project/lportal/Liferay%20Portal/6.2.5%20GA6/liferay-portal-tomcat-6.2-ce-ga6-20160112152609836.zip \
#	&& unzip liferay-portal-tomcat-6.2-ce-ga6-20160112152609836.zip -d /usr/local \
#	&& rm liferay-portal-tomcat-6.2-ce-ga6-20160112152609836.zip

COPY liferay-portal-tomcat-6.2-ce-ga6-20160112152609836.zip ${LIFERAY_PARENT_DIR}
RUN unzip ${LIFERAY_PARENT_DIR}/liferay-portal-tomcat-6.2-ce-ga6-20160112152609836.zip -d ${LIFERAY_PARENT_DIR} \
	&& rm ${LIFERAY_PARENT_DIR}/liferay-portal-tomcat-6.2-ce-ga6-20160112152609836.zip
	
EXPOSE 8080

CMD ${LIFERAY_PARENT_DIR}/liferay-portal-6.2-ce-ga6/tomcat-7.0.62/bin/startup.sh && tail -f ${LIFERAY_PARENT_DIR}/liferay-portal-6.2-ce-ga6/tomcat-7.0.62/logs/catalina.out
