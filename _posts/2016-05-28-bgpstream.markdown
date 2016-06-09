---
layout: post
title:  "BGPStream"
date:   2016-05-28 21:21:45 +0200
categories: BGPStream BGP
---
A few things about BGPStream:

It uses data from RIPE RIS and RouteViews. It should be noted that those two projects dump their data (RIB and BGP update) periodically. In particular, RIPE and RouteViews dump every 8 and 2 hours, respectively. For update, 5 minutes is the interval. Here, I will focus on RIB data, since the dump period is much longer.

So, when specifying the time interval, it should fall around the dump time. Otherwise, BGPStream will results nothing.


