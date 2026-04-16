sh /etc/openvswitch/init.sh

ovs-vsctl set port eth1 tag=491
ovs-vsctl set port eth2 tag=491
ovs-vsctl set port eth3 tag=492
ovs-vsctl set port eth4 tag=492
ovs-vsctl set port eth0 trunks=491,492

ovs-vsctl show

ip addr add 10.10.1.101/24 dev eth0
ip link set eth0 up

ip addr add 10.10.1.102/24 dev eth0
ip link set eth0 up

ip addr add 10.10.2.103/24 dev eth0
ip link set eth0 up

ip addr add 10.10.2.104/24 dev eth0
ip link set eth0 up

ip route add default via 10.10.1.1
ip route add default via 10.10.1.1
ip route add default via 10.10.2.1
ip route add default via 10.10.2.1

ip link add link eth0 name eth0.491 type vlan id 491
ip link add link eth0 name eth0.492 type vlan id 492
ip address add 10.10.1.1/24 dev eth0.491
ip address add 10.10.2.1/24 dev eth0.492
ip link set dev eth0.491 up
ip link set dev eth0.492 up

ip addr show

ping 10.10.1.102
ping 10.10.2.104

ip neigh show
