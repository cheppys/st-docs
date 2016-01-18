January 13, 2016
5:39 PM


-----

# ST Developer API & DB

-----

1. [**Introduction**](#introduction)
2. [**Rest-API**](#rest-api)
2. Authentication
3. Realtime Event
4. Errors
5. Streaming API


## [Introduction](id:introduction)
______________________

Satutrack API untuk interaksi dengan device OBD

1. **REST - API** Application data request dari satutrack
2. **REALTIME EVENT API** 




## [Rest-API](id:rest-api)

---------------------

### Device

Device information/identifier seperti OBD/GPS 

* id

> device identifier,

* Imei

> device Imei

* type

> type of OBD/GPS

* brand

> type of brand/merk of vehicle

* simcard

> number simcard provider

* Version

> Device Version



### Trip

**Trip** ter-create ketika kendaraan memiliki satu cycle yaitu **ignition:on to ignition:off** (1 trip) 

**Trip** harus memiliki jarak minimum dari 10 meters jika kurang tidak akan di anggap Trip 

* Trip
	* start_time 
	* end_time
	* Start_address
	* End_address
	* Distance
	* Duration
	* Fuel Consume
	* Speed avg
	* Overspeed
		* Time
		* Duration
	* Lat/Lon
	* Tag


**Output Example**

```
{
  
  "id": "idxxxx",
  "user": "url",
  "started_at": "",
  "ended_at": "",
  "distance_km": ,
  "duration_s": ,
  "vehicle": "",
  "start_location": {
    "lat": ,
    "lon": ,
    "accuracy_m": 
  },
  "start_address": {
    "name": "Jl. Margaguna Raya Kby.Baru Kota Jakarta Selatan, Daerah Khusus Ibukota Jakarta 12420",
    "display_name": "Jl. Margaguna Raya, Kby.Baru,Jakarta Selatan, Jakarta",
    "pos_code": "12420",
    "street_name": "Jl. Margaguna Raya",
    "city": "Jakarta Selatan",
    "state": "Jakarta",
    "country": "ID"
  },
  "end_location": {
    "lat": ,
    "lon": ,
    "accuracy_m": 9
  },
  "end_address": {
    "name": "Jl. Margaguna Raya Kby.Baru Kota Jakarta Selatan, Daerah Khusus Ibukota Jakarta 12420",
    "display_name": "Jl. Margaguna Raya, Kby.Baru,Jakarta Selatan, Jakarta",
    "pos_code": "12420",
    "street_name": "Jl. Margaguna Raya",
    "city": "Jakarta Selatan",
    "state": "Jakarta",
    "country": "ID"
  },
  "path": ,
  "fuel_cost_idr": ,
  "fuel_volume_l": ,
  "fuel_consume": ,
  "average_from_epa_kmpl": 9.4,
  "score_events": 47.7,
  "score_speeding": 50,
  "hard_brakes": 0,
  "hard_accels": 1,
  "duration_over_70_s": 0,
  "duration_over_75_s": 0,
  "duration_over_80_s": 0,
  "vehicle_events": [
    {
      "type": "hard_accel",
      "lat": 33.97642,
      "lon": -118.37013,
      "created_at": "",
      "g_force": 0.3
    }
  ],
  "start_timezone": "",
  "end_timezone": "",
  "night_driving_fraction": 0,
  "idling_time_s": ,
  "group":,
  "tags": [
    "business"
  ]
}

```


	



### User



### Vehicle


