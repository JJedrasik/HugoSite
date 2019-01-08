---
title: "Port Scanning"
date: 2019-01-02T15:19:10-05:00
draft: true
---

In the realm of cybersecurity, port scanning is probably one of the first things you want to do, regardless of which colour your metaphorical hacking hat is.

At Ryerson, security guards usually begin prowling around after hours, going door to door and giving them a tug to see if they're unlocked or not. In essence, this is what a port scan is.

Any kind of web-connected device will be running multiple ports for the  services it has going. For example, ssh runs on port 22, ftp runs port 20, and sql server runs on port 1433. As such, when I ssh into a server, my computer has an open port - 22.

What a port scan does is send a signal to each port sequentially (1,2,3...etc), checking to see if it is open or not. While this seems fairly trivial, it can usually be the first noticeable sign that something foul is afoot.

It's worth noting that scanning specific ports (My scan will only check a small subset of ports), is less likely to trigger any kind of alerts than if I was scan every single port in sequence.

Essentially, your port scanner will send packets to ports, and the ports will reply with either of the 3:

Open: Well, it means the service is running and accepting connections

Closed: Quite the opposite, this service is disabled and no connections can be established

Filtered: We send a packet, however something (perhaps a firewall), filtered it out
