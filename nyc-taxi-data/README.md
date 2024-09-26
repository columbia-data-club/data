# NYC Taxi Data

Data Club loves NYC Taxi Data. These data come from the [TLC Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page) site provided by the NYC Taxi and Limousine Commission (TLC). This README provides some data definitions.

As of May 2022, the TLC data is provided in [parquet](https://parquet.apache.org/) format.

## Documentation

TLC provides data dictionaries and guides. Unfortunately, these are available only as pdfs.

* [TLC Trip Record User Guide](https://www.nyc.gov/assets/tlc/downloads/pdf/trip_record_user_guide.pdf)
* [Yellow Taxi Data Dictionary](https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf)
* [Green Taxi Data Dictionary](https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_green.pdf)
* [FHV Data Dictionary](https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_fhv.pdf)
* [High Volume FHV (Uber, Lyft) Data Dictionary](https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_hvfhs.pdf)
## Definitions

Some important definitions:

* **Yellow Taxis** are street- or app-hailed yellow taxis. They can operate in all five boroughs.
* **Green Taxis** are street- or app-hailed taxis. They cannot pick up fares in Manhattan south of Harlem, more or less. These taxis were introduced in 2013.
* **FHV** are “for-hire vehicles,” like limousines or black cars or community cabs. The high-volume FHV data is for companies dispatching more than 10,000 trips a day, like Uber or Lyft.

### Payment Types

Payment types are given a numerical code in the yellow and green taxi data sets. Those payment types are: 

1. Credit card
2. Cash
3. No charge
4. Dispute
5. Unknown
6. Voided trip

### Rate Categories

The final rate applied at the end of the trip is given a numerical value in the yellow and green taxi data sets. Those rate categories are:

1. Standard rate
2. JFK
3. Newark
4. Nassau or Westchester
5. Negotiated fare
6. Group ride

### Locations

The pickup and dropoff locations are indicated by Taxi Zones.
In the `maps/` folder of this section of the repository one can see the zones across the five boroughs.
The file `taxi_zone_lookup.csv` associates the numerical zones with neighborhood names.
The file `nyc-taxi-zones.geojson` is a GeoJSON file that encodes the zones for geospatial analysis of the taxi data.

