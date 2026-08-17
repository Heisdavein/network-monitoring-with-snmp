# Network Monitoring with SNMP
Documentation Attached as PDF

A hands-on Cisco Packet Tracer network monitoring project focused on configuring SNMP Version 2 on a Cisco router and switch, establishing centralized monitoring, and retrieving network information through the MIB Browser.

---

## Project Overview

This project is a practical **SNMP Version 2 network monitoring lab** completed in Cisco Packet Tracer.

The purpose of the lab was to understand how network administrators can monitor multiple network devices from one central location without having to log into each router or switch individually.

The lab consisted of:

- A Cisco router
- A Cisco switch
- A monitoring server
- Application servers
- End-user PCs

The router and switch were configured as **SNMP agents**, while the monitoring server acted as the **SNMP manager**.

The monitoring server used the **MIB Browser** to communicate with the SNMP agents and retrieve information about the devices.

This project provided practical experience with SNMP configuration, MIBs, OIDs, community strings, Read-Only access, device monitoring, verification, and the limitations of network simulation.

---

# The Problem SNMP Solves

Imagine a company with 80 network switches.

If a network administrator wanted to check whether a network port had stopped working, logging into all 80 switches individually would take a significant amount of time.

SNMP helps solve this problem by allowing one central computer to monitor many network devices from a single location.

Each network device runs an **SNMP agent**.

The agent can collect information about the device, such as:

- CPU usage
- Memory usage
- Interface status
- Device uptime
- IP addresses
- Interface information
- MAC addresses

A central computer called the **SNMP manager** sends requests to these agents and receives the requested information.

This makes it much easier to monitor a large network.

---

# Real-World Example

I think of SNMP in a similar way to smart electricity meters.

Instead of sending someone to every house to manually check the electricity meter, each house can have a smart meter that automatically provides its readings to the electricity company.

The same concept applies to SNMP:

- The **SNMP manager** is like the electricity company collecting the readings.
- The **SNMP agents** are like the smart meters installed in each house.
- The information collected from each device is similar to the meter readings.

This allows administrators to monitor many network devices quickly without physically visiting each device.

---

# Project Objectives

The main objectives of this lab were to:

- Understand the purpose of SNMP
- Understand how centralized network monitoring works
- Understand the role of an SNMP manager
- Understand the role of an SNMP agent
- Understand Management Information Bases (MIBs)
- Understand Object Identifiers (OIDs)
- Understand SNMP community strings
- Configure SNMP Version 2 on a Cisco router
- Configure SNMP Version 2 on a Cisco switch
- Configure Read-Only SNMP access
- Verify the SNMP configuration
- Use the MIB Browser to query network devices
- Retrieve information from a Cisco router
- Retrieve information from a Cisco switch
- Understand the security limitations of SNMP Version 2
- Understand the limitations of SNMP simulation in Cisco Packet Tracer
- Understand how SNMP is used in real enterprise environments

---

# SNMP Architecture

SNMP uses a manager-and-agent architecture.

The main components involved in this project were:

```text
                 SNMP Manager
                Monitor Server
                      |
          +-----------+-----------+
          |                       |
          | SNMP Requests         | SNMP Requests
          ↓                       ↓
     Cisco Router           Cisco Switch
      SNMP Agent             SNMP Agent
