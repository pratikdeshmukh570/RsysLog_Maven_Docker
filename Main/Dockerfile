# lightweight base image 
FROM maven:3.6-jdk-11-slim

# Creating a directory
WORKDIR /app

# copying files
COPY .. /app

# install rsyslog
RUN apt update &&  apt-get install rsyslog -y

# Edit and move the config file inside the directory within the image
RUN mv -f /app/rsyslog.conf /etc/rsyslog.conf

EXPOSE 7000
# IF WANT TO SEE RSYSLOGS IMMEDIATELY AFTER THE CONTAINER RUNS
#CMD ["rsyslogd", "-n"]

# If want to check or edit log files
CMD ["/bin/bash"]
