Apparently, there are territories that are not served by Google Map Geocoding API, eventhough they looks to have addresses on Google Map. For example, if I query the following coordinates:
lat:42.6475  lon:21.1795 (Kosovo)
lat:42.6575  lon:20.2895 (Kosovo)
lat:44.6705  lon:34.3985 (Sevastopol, Russia)

Google Geocoding API returns none.

However, OpenStreetMap Nominatim returns the address correctly. Of course, I can't conclude that OSM is better than Google just by observing three samples.
