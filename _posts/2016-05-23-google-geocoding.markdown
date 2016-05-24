---
layout: post
title:  "Blank Spot in Google Geocoding API"
date:   2016-05-23 21:21:45 +0200
categories: 
---
Apparently, there are territories that are not served by Google Map Geocoding API, eventhough they looks to have addresses on Google Map. For example, if I query the following coordinates:
* lat:42.6475  lon:21.1795 (Kosovo)
* lat:42.6575  lon:20.2895 (Kosovo)
* lat:44.6705  lon:34.3985 (Sevastopol, Russia)

Google Geocoding API returns none.

However, OpenStreetMap Nominatim returns the address correctly. 
* lat:42.6475  lon:21.1795 ==> Shaqir Ingrishta, Bregu i Diellit, Prishtinë, Komuna e Prishtinës, 10000, Kosovë 
* lat:42.6575  lon:20.2895 ==> Bulevardi, Pejë, Komuna e Pejës, 39000, Србија (Serbia)
* lat:44.6705  lon:34.3985 ==> 53, Октябрьская улица, Мирный, Алушта, Алуштинский городской совет, КФО, 98500, Україна

Well, it doesn't mean that Google Geocoding is less accurate. Those three coordinates located in disputed areas. From quick googling, Google seems to give serious consideration of their services on such region. Maybe including my problem above. On the other hand, OSM seems doesn't care at all (I haven't searched about it yet).
