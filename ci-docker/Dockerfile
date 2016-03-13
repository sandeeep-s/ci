FROM anapsix/alpine-java:jdk7
ADD liferay-portal-6.2-ce-ga2 /usr/local/liferay-portal-6.2-ce-ga2
EXPOSE 8080
CMD /usr/local/liferay-portal-6.2-ce-ga2/tomcat-7.0.42/bin/startup.sh && tail -f /usr/local/liferay-portal-6.2-ce-ga2/tomcat-7.0.42/logs/catalina.out
