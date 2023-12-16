# kfz_neukölln.csv

* Description: This dataset is created from the others datasets which are mentioned above and also from the datasets which were published in the Berlin Datathon 2021. This well organized dataset, contains data of the district Friedrichshain-Kreuzberg and Neukölln. 

* A street contains one or more parking areas and each parking area contains one or more parking spots. Each parking spot has a fixed orientation.

* Each row is mimicked 'n' times for specific parking area of a specific street. Here 'n' means the capacity of that specific parking area. The only difference among rows is the values of one column which name is "geometry" that represents the coordinates of each parking spots. 

|Variable Name | Data Type | Description |
|---|---|---|
highway | string | street type, for example: secondary, residential, tertiary |
name | string | street name, for example: Köpenicker Straße, Hildegard-Jadamowitz-Straße, Methfesselstraße |
parking | string | type of parking area, for example: lane, street_side |
orientation | string | direction of parking vehicles in the parking spots, for example: parallel, diagonal, perpendicular |
position | string | the places where the parking areas are located, for example: on_street, street_side, on_kerb, shoulder |
capacity | integer | the capacity of parking area for each parking type, each represents the parking spot, for example: 'secondary' type street 'Köpenicker Straße' has a 'on_street' parking 'lane' where 12 vehicles can be parked in the 'parallel' direction. So the number of parking spots is 12. |
source_orientation | string | the source of orientation  |
source_position | string | the source of parking area's position. |
source_capacity | string | the source of parking area's capacity. |
geometry | geometry object | the geometry which contains the coordinates of real world's map. This geometry explains the location of a parking spots. |
district | string | the name of the district where the lor exists. |
lor | string | the name of the small block in a district, that means, a district consists of a collection of lors. for example: the district Friedrichshain-Kreuzberg consists of 26 lors. |
Bezirksregion | string | ... |
Prognoseraum | string | ... |
lor size in m² | float64 | the size of each lor in square meter. |
inhabitants_total | int64 | the number of people who are living in the specific lor. |
of_those_inhabitants_18+ | int64 | the number of people who are over 18 years old and also are living in the specific lor. |
vehicles_overall | int64 | the total number of registered vehicles in the specific lor. |
cars_only | int64 | the total number of registered cars in the specific lor. |
vehicles_per_1000_inhabitants | int64 | the registered vehicles per 1000 inhabitants of the specific lor. |
cars_per_1000_inhabitants | int64 | the registered vehicles per 1000 inhabitants of the specific lor. |
lor_geometry | geometry object | the geometry which contains the coordinates of real world's map. This geometry explains the location of a lor. |

# kfz_neukölln_02.csv
* Description: This dataset is created from the above dataset which name is 'kfz_neukölln.csv'. This is more purified and compact version of the 'kfz_neukölln.csv' dataset. This dataset contains some columns(for example: lor geometry but not the parking spot geometry) from 'kfz_neukölln.csv' dataset and the total parking capacity of each parking area. For this, the mimicked rows are droped in this dataset.
