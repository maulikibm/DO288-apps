# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
EXPOSE 8080

LABEL io.k8s.description="A basic APache HTTPD Child image"\
      io.k8s.display-name="Apache HTTP Hola Server"\
      io.openshift.expose-services="8080"\
      io.openshift.tags="apache,httpd"

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf

run chgrp -R 0 /var/log/httpd /var/run/httpd &&\
    chgrp -R g=u /var/log/httpd /var/run/httpd

USER 1001

