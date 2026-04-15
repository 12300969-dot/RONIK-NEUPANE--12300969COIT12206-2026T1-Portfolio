# Week 2 Assignment

**Name:** Ronik Neupane  
**Student ID:** 12300969  

## Task 1: Setting Static IP Addresses

A project was created in GNS3 with four Linux Host nodes and one Ethernet switch connected in a LAN topology. A private IPv4 network was used to assign static addresses to each host.

For Host1 and Host2, the static IP addresses were configured using the GNS3 **Configure** option by editing the `/etc/network/interfaces` file before starting the nodes. This method applies the configuration when the node starts.

For Host3, the IP address was configured manually in the console by editing the `/etc/network/interfaces` file using `nano`. After saving the changes, the network interface configuration was reloaded using `ifdown eth0` and `ifup eth0`.

For Host4, the IP address was assigned directly from the console using the `ip address add` command. This method applies the IP address immediately, although it is not permanent after reboot.

The following IP addresses were used in the LAN:

- Host1: 10.10.2.1/24
- Host2: 10.10.2.2/24
- Host3: 10.10.2.3/24
- Host4: 10.10.2.4/24

### Network Topology

![Week 2 Network Topology](week2_network.png)

### Host1 IP Verification

![Host1 IP Address](week2_host1.png)

### Host2 IP Verification

![Host2 IP Address](week2_host2.png)

### Host3 IP Verification

![Host3 IP Address](week2_host3.png)

### Host4 IP Verification

![Host4 IP Address](week2_host4.png)

## Task 2: Testing Network Connectivity and Delay with Ping

Ping was used to test connectivity between hosts and to observe round-trip time (RTT). A successful ping from one host to another showed that the destination was reachable on the network.

A basic ping test was performed from one host to another host in the same LAN. The output showed replies being received successfully, with 0% packet loss. The average RTT was very low, which is expected because all hosts are connected through the same switch in a local network.

A second ping test was performed to a non-existent IP address, 10.10.2.5. In this case, the output showed **Destination Host Unreachable** and 100% packet loss. This indicates that no host with that IP address exists in the network.

A third ping test was performed using options to set the count, interval and packet size. The command used was:

`ping -c 5 -i 2 -s 60 10.10.2.2`

This command sent 5 packets, waited 2 seconds between packets, and used a data size of 60 bytes. The destination replied successfully, confirming connectivity. The options changed how ping operated, but the RTT remained low because the devices were still on the same local network.

### Simple Ping

![Simple Ping](week2_ping_simple.png)

### Ping to Wrong IP Address

![Ping Error](week2_ping_error.png)

### Ping with Options

![Ping Options](week2_ping_options.png)

## Conclusion

This week’s tutorial demonstrated three different ways of setting static IP addresses on Linux hosts in GNS3: by editing the configuration before startup, by editing the configuration file from the console and reloading the interface, and by using the `ip address add` command directly. After configuring the IP addresses, ping was used to verify connectivity and measure delay between hosts. The results confirmed that the hosts were correctly configured and able to communicate across the LAN.
