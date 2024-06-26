# bike-repair-stations
Work in Progress

## overpass query
```
[out:csv(::id,amenity,::lat,::lon,opening_hours,brand,fee,'service:bicycle:pump','service:bicycle:tools';true;',')];

// search for the relation named Chattanooga
area
  [place=city]
  ["wikidata"="Q186702"]
  ["name"="Chattanooga"]->.a;

nwr["amenity"="bicycle_repair_station"](area.a);

out body center;
```
