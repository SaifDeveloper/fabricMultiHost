# FabricMultiHostDeployment

sudo chown -R root:ubuntu ./crypto-config/

sudo chown -R $USER ./crypto-config

docker swarm init --advertise-addr 3.238.246.168

docker swarm join-token manager

docker swarm join --token SWMTKN-1-0elhq6rqfdguwxc7p4v64sdgizslufu538huuiln8di7949u5y-8vlsunf3q8z4gye9uaojyqdee 3.238.246.168:2377 --advertise-addr 3.238.202.149

docker swarm join --token SWMTKN-1-0elhq6rqfdguwxc7p4v64sdgizslufu538huuiln8di7949u5y-8vlsunf3q8z4gye9uaojyqdee 3.238.246.168:2377 --advertise-addr 35.172.150.31

docker swarm join --token SWMTKN-1-0elhq6rqfdguwxc7p4v64sdgizslufu538huuiln8di7949u5y-8vlsunf3q8z4gye9uaojyqdee 3.238.246.168:2377 --advertise-addr 18.204.220.139



docker network create --attachable --driver overlay artifacts_test


# WARNING: The Docker Engine you're using is running in swarm mode. Compose does not use swarm mode to deploy services to multiple nodes in a swarm. All containers will be scheduled on the current node.

swarm leave and init again will fix the above