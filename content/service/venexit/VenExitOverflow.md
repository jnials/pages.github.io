---
date: '2025-01-23T15:29:42-06:00'
draft: false
title: 'VenExitOverflow'
---

### VenExit Overflow
A VEN Exit overflow occurs when an Exit is unable to receive network traffic
from an Entrance due to its queue being full.  While the packet is returned to
the pool for future processing, and is not dropped, this signifies slower
network traffic via the Exit which can lead to connection timeouts for the VEN
Entrance clients.

### Alerts
**VenExitOverflowWarning:** The total number of overflow packets is greater than 5% of total packets for an Exit during a 5 minute window.
**VenExitOverflowCritical:** The total number of overflow packets is greater than 10% of total packets for an Exit during a 5 minute window.

### Causes
There is insufficient CPU allocation on an Exit to handle incoming network
traffic from its associated Entrances causing overflows to occur.

### Solutions:
* The number of CPU's assigned to the VEN Exit may be too low. Increase the number of CPU's on that VEN Exit.
* If increasing the number of CPU's does not prevent the alert or there are already enough CPU's, then spin up a new VEN Exit and put it into service.