FROM debian:latest
MAINTAINER Max Schaefer <max@excloo.com>
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y ca-certificates inotify-tools nano pwgen supervisor tmux unzip wget
RUN mkdir -p /config/data /config/init /data /var/log/supervisor
ADD loop /config/loop
RUN chmod +x /config/loop
CMD /config/loop
