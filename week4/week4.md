# Week 4 – Network Configuration and Routing

## Overview

In this week, I worked on two tasks.  
Task 1 was about setting up static IP addresses.  
Task 2 was about configuring OSPF routing so different networks can communicate.

---

# Task 1 – Static IP Configuration

## Topology

![Task1 Topology](task1-topology.png)

This diagram shows the network with three hosts connected to a switch and a router.

---

## Host Configurations

![Host1](task1-host1.png)

Host1 was given a static IP address and a default gateway so it can communicate with other networks.

![Host2](task1-host2.png)

Host2 was also configured with a static IP in the same network as Host1.

![Host3](task1-host3.png)

Host3 is in a different network and uses the router as its gateway to communicate.

---

## Router Configuration

![Router eth0](task1-router-eth0.png)

This interface connects to the network where Host1 and Host2 are located.

![Router eth1](task1-router-eth1.png)

This interface connects to the network where Host3 is located, allowing communication between both networks.

---

## Connectivity Test

![Ping](task1-ping.png)

Ping was used to check if the devices can communicate. The replies confirm that the connection is working.

---

## Result

All hosts were able to communicate successfully, which means the static IP setup was done correctly.

---

# Task 2 – OSPF Routing

## Topology

![Task2 Topology](task2-topology.png)

This diagram shows multiple routers connected together using OSPF.

---

## FRR Configuration

![FRR](task2-frr-config.png)

FRR was configured on the routers to enable OSPF routing.

---

## Routing Table

![Routing Table](task2-routing-table.png)

The routing table shows both directly connected networks and routes learned through OSPF.

---

## OSPF Routes

![OSPF Routes](task2-ospf-routes.png)

This output shows the routes that were shared between routers using OSPF.

---

## Traceroute

![Traceroute](task2-traceroute.png)

Traceroute shows the path packets take across the network, confirming that routing is working properly.

---

## Result

OSPF routing worked successfully and allowed communication between different networks.
