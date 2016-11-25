FROM debian:jessie

# Add filebeat
ADD filebeat*.tar.gz /filebeat-install
#move everything to the right dir
RUN mkdir /filebeat
RUN mv /filebeat-install/filebeat*/* /filebeat
RUN rm -f /filebeat/filebeat.yml

# Add this file in the run command
#ADD filebeat-config/filebeat.yml /filebeat/filebeat.yml
#RUN ls /filebeat
ENTRYPOINT ["/filebeat/filebeat", "-e", "-v", "-c", "/filebeat/filebeat.yml"]
