# A Simple Bind9 Recursive Server deployment for home Lab Environment

This Ansible Playbook will just deploly a bind9 server inside a REHL 8 Based OS (Such as Almalinux 8)

Yes, Bind9 and Bind are mostly same!

You can run this script by running the following command
```
time ansible-playbook main.yml
```
Some credits goes to: https://mangolassi.it/topic/12877/set-up-bind-server-with-ansible/2
###### Note: You have to have the valid hostnames added in your /etc/ansible/hosts file


### You can check live dns queries on your server by
```
tcpdump -i enp1s0 udp port 53
```

Or see the cached dns queries on
```
rndc dumpdb -cache
grep google.com /var/named/data/cache_dump.db
```