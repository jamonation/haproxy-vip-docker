FROM centos:7

RUN yum -y install haproxy keepalived psmisc && yum clean all

RUN mkdir /opt/haproxy-vip-docker
COPY haproxy.cfg /opt/haproxy-vip-docker/
COPY keepalived-haproxy.cfg /opt/haproxy-vip-docker/

CMD rm -f /var/run/haproxy/haproxy.sock& haproxy -f /opt/haproxy-vip-docker/haproxy.cfg& keepalived -P -l -n -f /opt/haproxy-vip-docker/keepalived-haproxy.cfg
