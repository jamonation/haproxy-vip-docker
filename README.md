# haproxy-vip-docker

This ansible role will build a docker image containing HAproxy and keepalived.

Either haproxy docker container can be shutdown and the other will take over.

Up to n HTTP backends can be defined in vars/main.yml.

HAproxy will expose its admin socket as a Docker volume at /var/run/haproxy/haproxy.sock on each host server. Use the socket as specified in https://cbonte.github.io/haproxy-dconv/configuration-1.5.html#9.2

# multicast / unicast

This role has been tested using multicast for VRRP without any issues.

Minimal testing has been done using unicast peer IPs, but it seems to work well enough.

Pull requests welcome!
