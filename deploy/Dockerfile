FROM ubuntu
MAINTAINER vishnuk@google.com

# NOTE: Run build.sh before building this Docker image.

ADD heapster /usr/bin/heapster
ADD run.sh /run.sh
RUN chmod +x /run.sh

# cAdvisor discovery via external files.
RUN mkdir -p /var/run/heapster
RUN touch /var/run/heapster/hosts

ENTRYPOINT ["/run.sh"]