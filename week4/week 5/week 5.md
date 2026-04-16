## Task 1 – Setup VLANs on Switch

### Network Topology
![Task 1 Topology](task1_topology.png)

This screenshot shows the network for Task 1.  
Host1 and Host2 are in one VLAN.  
Host3 and Host4 are in another VLAN.

---

### Host Configurations

![Host1 Config](task1_host1_config.png)

Host1 was configured with a static IP address.

![Host2 Config](task1_host2_config.png)

Host2 was configured in the same subnet.

![Host3 Config](task1_host3_config.png)

Host3 was also configured with a static IP.

---

### Ping Test

![Ping Result](task1_ping_result.png)

Ping works between hosts in the same VLAN and fails between different VLANs.

---

### Router Configuration (if included in Task 1)

![Router eth0](task1_router_eth0_config.png)

![Router eth1](task1_router_eth1_config.png)

Router interfaces were configured for communication.

---

## Task 2 – Routing and OSPF

### Network Topology

![Task 2 Topology](task2_topology.png)

This shows the full network with routing enabled.

---

### FRR Configuration

![FRR Config](task2_frr_config.png)

FRR was configured to enable routing.

---

### Routing Table

![Routing Table](task2_routing_table.png)

This shows the routing table after configuration.

---

### OSPF Routes

![OSPF Routes](task2_ospf_routes.png)

OSPF routes are visible and working.

---

### Traceroute Test

![Traceroute 1](task2_traceroute_1.png)

![Traceroute 2](task2_traceroute_2.png)

Traceroute confirms packets are travelling correctly across the network.
