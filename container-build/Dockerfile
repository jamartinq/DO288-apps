# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

LABEL io.openshift.expose-services="8080:http" \
      io.k8s.display-name="Apache HTTP server" \
      io.k8s.description="A basic Apache HTTP Server child image, uses ONBUILD" \
      io.openshfit.tags="apache,httpd"

RUN sed -i 's/Listen 80/Listen 8080/g' /etc/httpd/conf/httpd.conf && \
    chgrp -R 0 /var/run/httpd /var/log/httpd && \
    chmod -R g=u /var/run/httpd /var/log/httpd

EXPOSE 8080

USER 1001

