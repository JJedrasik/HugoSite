---
title: "Port Scanning"
date: 2019-01-02T15:19:10-05:00
draft: false
---
Ok so lets talk about port scanning. While a fairy simple concept, it's a super essential skill to understand.

Let's pretend we have a home invader, prowling around in the darkness. After he finds a house he hopes to...well...invade, he goes up to it and begins tugging and trying all the doors and windows, to see what is open, and if it is a viable way to begin his attack. In essence, this is what a port scan is, except instead of some doors and windows, there is thousands of doors, some who only accept TCP, and others only UDP.

Ports are functionally like a door, except theres, like, literally thousands. Their purpose is to have a channel of transmission for a specific service (i.e. SSH runs on  TCP/22).

So, we have a port scanner, (which, if you need, I have one on my [github](https://github.com/JJedrasik/ScriptsnScraps/blob/master/portscanner.py)), and what it's going to do is send a signal to each port on a machine in succession. Remember, ports up to 1024 are standardized, while ports after 1024 can be used by other services.

We send a signal to a server port, and it responds with one of the three responses:

Open: Ok, the service is running, and can take requests

Closed: The opposite, this port is closed and will not accept any connections.

Filtered: Something has kicked out your packet. Maybe a firewall, maybe a filter of other sorts, either way, this server port is too busy for your shenanigans.

Once we know that, we can start thinking of some kind of attack vector based on our open ports. Now, best practice is to always keep closed unused ports, for obvious reasons. We can't attack something that isn't opened. If a port is closed, well, there is no way we can send anything kind of packets into it.

Port scans are also fairly noticeable. A server is probably going to realize if something is pinging it in each port in succession, and while port scans may have 0 malicious intent, they are still used as a metaphorical scouting party before the actual horde arrives.

If you have a server at home you can poke and prod, go ahead and play around with port scanning. Most Operating Systems come preinstalled with port scanners as it is (N-Map is standardized on Windows system, and is quite robust), and of course the internet has a plethora of knowledge.

As such, as technology and security evolves, so do methods of attack. There are plenty of ways to stealth your scan, which I'll be talking about in a further article. In the meantime, give port scanning a try, as it sets up the basis for network security monitoring. 
