https://docs.google.com/document/d/1NnJmcAoHscxGSyFzhYd5AbU9JoZMBwG6/edit?usp=sharing&ouid=115821798289915649231&rtpof=true&sd=true

Weird things with data:
Floor: NAN -> 0
Rooms: NAN -> 1
Ceiling: NAN -> Average, Median
Bathrooms: if bathroom_shared is 1 bathroom_private NAN -> 0 and vice versa from corr map
Research window laws in Russia
Condition: NAN -> 3
Phones: NAN -> 1, maybe 0
New: NAN -> 0
Constructed: Newer is more expensive
Material: NAN->2
Elevator_without: NAN -> 0
Elevator_passenger: NAN -> 1
Elevator_service: NAN -> 0
Parking: NAN -> 1
Garbage_chute: NAN ->1
Heating: NAN -> 0
Seller: NAN -> 3




Features:
Combinations of area_total, area_kitchen, area_living
Floor/Stories, the ratio is what matters
Combine latitude/longitude

drop: "id","area_total","floor", "rooms", "building_id", "street", "address", "stories"
drop: "id","area_total", "building_id",
"street", "address", "stories", 'bathrooms_shared', 'bathrooms_private',
'constructed', 'windows_street', 'windows_court', 'layout', 'area_kitchen', 'area_living'


        #('rooms', 1), no nans
        ('ceiling', data['ceiling'].mean()),
        #('bathrooms_shared',),
        #('bathrooms_private',),
        ('condition', 3),
        ('phones', 1),
        ('new', 0),
        #('contructed',),
        ('material', 2),
        ('elevator_without', 0),
        ('elevator_passenger', 1),
        ('elevator_service', 0),
        ('parking', 1),
        ('garbage_chute', 0),
        ('heating', 0),
        ('balconies', 0),
        ('loggias', 0),
        ('seller', 2)

seller	price	area_total	area_kitchen	area_living	floor	rooms	
layout	ceiling	bathrooms_shared	bathrooms_private	windows_court	
windows_street	balconies	loggias	condition	phones	building_id
new	 latitude	longitude	district.	street	address	constructed	
material	stories	elevator_without	elevator_passenger	elevator_service	
parking	garbage_chute	heating