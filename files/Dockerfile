FROM centos:latest


RUN dnf install -y epel-release
RUN dnf install -y transmission-daemon
RUN mkdir -p /data/vod/td

EXPOSE 9091 60198 60198/udp

ADD settings.json /var/lib/transmission/.config/transmission-daemon/

ENTRYPOINT [ "/usr/bin/transmission-daemon", "--foreground", "--log-error" , "--config-dir", "/var/lib/transmission/.config/transmission-daemon"]