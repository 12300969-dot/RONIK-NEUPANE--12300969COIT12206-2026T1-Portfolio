# Week 4 – Network Configuration and Routing

## Overview

In this week, I worked on two tasks.  
Task 1 was about setting up static IP addresses.  
Task 2 was about configuring OSPF routing so different networks can communicate.

---

# Task 1 – Static IP Configuration

## Topology

![Task1 Topology](task1_topology.png)

This diagram shows the network with three hosts connected to a switch and a router.

---

## Host Configurations

![Host1](task1_host1_config.png)

Host1 was given a static IP address and a default gateway so it can communicate with other networks.

![Host2](task1_host2_config.png)

Host2 was also configured with a static IP in the same network as Host1.

![Host3](task1_host3_config.png)

Host3 is in a different network and uses the router as its gateway to communicate.

---

## Router Configuration

![Router eth0](task1_router_eth0_config.png)

This interface connects to the network where Host1 and Host2 are located.

![Router eth1](task1_router_eth1_config.png)

This interface connects to the network where Host3 is located, allowing communication between both networks.

---

## Connectivity Test

![Ping](task1_ping_result.png)

Ping was used to check if the devices can communicate. The replies confirm that the connection is working.

---

## Result

All hosts were able to communicate successfully, which means the static IP setup was done correctly.

---

# Task 2 – OSPF Routing

## Topology

![Task2 Topology](task2_topology.png)

This diagram shows multiple routers connected together using OSPF.

---

## FRR Configuration

![FRR](task2_frr_config.png)

FRR was configured on the routers to enable OSPF routing.

---

## Routing Table

![Routing Table](task2_routing_table.png)

The routing table shows both directly connected networks and routes learned through OSPF.

---

## OSPF Routes

![OSPF Routes](task2_ospf_routes.png)

This output shows the routes that were shared between routers using OSPF.

---

## Traceroute 1

![Traceroute 1](task2_traceoute_1.png)

This traceroute shows the path taken by packets through the network.

---

## Traceroute 2

![Traceroute 2](task2_traceoute_2.png)

This traceroute also confirms that communication between networks is working properly.

---

## Result

OSPF routing worked successfully and allowed communication between different networks.
