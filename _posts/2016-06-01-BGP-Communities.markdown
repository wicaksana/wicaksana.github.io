BGP communities attribute is typically used for three purposes:
1. Inbound
It refers to communities added or used when a route is received by a router on an eBGP session. It is categorized into two: LocalPref and Route tagging. LocalPref is used to set the LOCAL\_PREF attribute in the AS receiving the route. Route tagging is used by an AS to indicate the location where the route was received from an external peer.

A route might be tagged in the following cases:
a.) IXP. This type of communities indicates the interconnection point where a route was learned. 
b.) Type of peer. An AS might define a community value for describing the relationship, e.g., peer, customer, provider, or transit. This simplifies the configuration of filters on BGP routers.
c.) Geographic. An AS might need to indicate the geographic location where the route was received.
d.) AS. This community indicates the AS from which a route was learned.

Most inbound communities values in use today have been defined independently by different operators, eventhough RFC 4384 proposed recommended encodings for most of these values.

2. Outbound
Outbound communities are used by a router to filter BGP announcements for traffic engineering purposes. A community is inserted by the originator of the route in order to influence its redistribution by downstream routers. The routes redistribution may be categorized into two: announcement and AS\_PATH prepending. 

3. Blackhole 
One can distinguish three types of blackholing by their scope:
a.) Global blackholing, packets are blocked everywhere in the ISP networks
b.) Border blackholing, packets are blocked at the ISP border routers
c.) Upstream blackholing, packets are blocked by the ISP's transit provider before they enter its own network
These communities are used only inside ISPs and should not be distributed on the global Internet

Based on [1], BGP communities are mainly used by network operators of Traffic Engineering purposes.

References:
[1] On BGP Communities
