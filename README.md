# Eco-Snap-Project
﻿![alt text](https://github.com/GMT-352/midterm-project---ecosnap-api-eslemsahin/blob/main/readme%20images/Ads%C4%B1z.png)

# GMT352 / GEOGRAPHIC INFORMATION SYSTEMS

## 21967756 ESLEM ŞAHİN

# MIDTERM PROJECT, SPRING 2022/23 

------

## EcoSnap API 

* EcoSnap is an application that does not aim to gather real-time citizen participation in identifying environmental and health issues during the creation of urban planning.


## INTRODUCTION 

* First of all, after downloading the eco snap application to my phone, I became a member and shared about the problems that attracted my attention and became a member.

<img src="./EcoSnap images/My_EcoSnap_Profile.jpeg" alt="alt yazı" width="400">

## MY EcoSnap POSTS

### 1) **Bad Asphalt**

<img src="./EcoSnap images/Bad_asphalt.jpeg" alt="alt yazı" width="280" >   <img src="./EcoSnap images/Bad_asphalt2.jpeg" alt="alt yazı" width="280" >

### 2) **Bad Path**

<img src="./EcoSnap images/Bad_path.jpeg" alt="alt yazı" width="280" >   <img src="./EcoSnap images/Bad_path2.jpeg" alt="alt yazı" width="280" >

### 3) **Barrier to crossing from pavement**

<img src="./EcoSnap images/Barrier_to_crossing_from_pavement.jpeg" alt="alt yazı" width="280">   <img src="./EcoSnap images/Barrier_to_crossing_from_pavement2.jpeg" alt="alt yazı" width="280">

### 4) **Chimney Carelessness**

<img src="./EcoSnap images/Chimney_carelessness.jpeg" alt="alt yazı" width="280">    <img src="./EcoSnap images/Chimney_carelessness2.jpeg" alt="alt yazı" width="280">

### 5) **Parking lot structure disorder**

<img src="./EcoSnap images/Parking_lot_structure_disorder.jpeg" alt="alt yazı" width="280">  <img src="./EcoSnap images/Parking_lot_structure_disorder2.jpeg" alt="alt yazı" width="280">

### 6) **Broken drain pipe**

<img src="./EcoSnap images/Broken_drain_pip.jpg" alt="alt yazı" width="280" >   <img src="./EcoSnap images/Broken_drain_pip2.jpg" alt="alt yazı" width="280" >

## POSTMAN 

### * User Information Request :

The POST request is used to send data to the server. This request method is used when the user fills out a web form or submits an API request (a form of request to receive or send data from the application). The POST request is processed by the server to add, update, or delete data from the specified resource. The POST request does not store the sent data in the URL and provides the ability to encrypt the data to aid security.

<img src="./readme images/Postman_User_ınf.png" alt="alt yazı" width="800" > 


### * Friends Activities Request : 

* GET request is used to get data from server. This request method retrieves data for a particular resource from the server by connecting to a URL. Since the GET request is only used to retrieve data, it does not make any changes to the server. A GET request can perform operations such as filtering, sorting, or paginating a particular dataset by adding query parameters to the URL.

<img src="./readme images/Postman_Activities.png" alt="alt yazı" width="800" >

### * Differences between POST and GET : 

* Both request methods are used for different purposes.
* GET request is used to get data from server while POST request is used to send data to server.
* It allows the POST request to move larger datasets and provides more flexibility compared to a GET request.

## MY POSTS DATA / PYTHON-JUPYTER NOTEBOOK 

* The code where I output the latitude and longitude information of my locations in the data obtained from Postman.


> 1.   Bad Asphalt                         |  2.   Bad Path

> 3.   Barrier to crossing from pavement   |  4.  Chimney Carelessness

> 5.   Parking lot structure disorder      |  6.   Broken drain pipe



* **INPUT**

** The code that provides coordinate information for a single location of the results obtained using Ecosnap data. You can review the codefile for other locations.

```
import json

x = {
        "id": "207b5166-08e3-434e-abbc-877952473ed7",
        "userName": "Eslem",
        "userSurname": "Şahin",
        "userPhotoUrl": "https://peer-review.hacettepe.edu.tr/ecosnap-photos/21f4fc8b-7354-45f7-9cae-c389d845aa0a.jpeg",
        "activityName": "Kaldırımdan Geçiş Engeli",
        "activityDescription": "Kaldırım ortasına düzensiz yerleştirilmiş olan  internet erişim kabini kaldırımın tamamının kullanımına engel oluyor.",
        "activityLatitude": 39.9668025,
        "activityLongitude": 32.5885711,
        "activityDate": "2023-04-23T14:19:25.239267+00:00",
        "activityType": "Bad Sidewalk",
        "photos": [
            "https://peer-review.hacettepe.edu.tr/ecosnap-photos/0482626d-f762-492c-85a6-e62b383d0b7d.jpg",
            "https://peer-review.hacettepe.edu.tr/ecosnap-photos/41006bfa-f295-4b2e-89cc-84942e52a466.jpeg",
            "https://peer-review.hacettepe.edu.tr/ecosnap-photos/6e8cf392-a67c-49da-b897-9d56fbb4a652.jpeg"
        ]
    }

with open('data.json', 'w') as f:
    json.dump(x, f)

with open('data.json', encoding='utf-8') as f:
    data_1 = json.load(f)

formatted_data_1 = json.dumps(data_1, indent=4, ensure_ascii=False)

print(formatted_data_1)

lat = data_1['activityLatitude']
lon = data_1['activityLongitude']

print(" ----> Bad Sidewalk Coordinates (lat/lon):", lat, lon) 


```

* **OUTPUT**

** You can see the output of the code that provides coordinate information for a single location of the results I obtained using my Ecosnap data. You can review the codefile for the output of other locations.

```
{
    "id": "207b5166-08e3-434e-abbc-877952473ed7",
    "userName": "Eslem",
    "userSurname": "Şahin",
    "userPhotoUrl": "https://peer-review.hacettepe.edu.tr/ecosnap-photos/21f4fc8b-7354-45f7-9cae-c389d845aa0a.jpeg",
    "activityName": "Kaldırımdan Geçiş Engeli",
    "activityDescription": "Kaldırım ortasına düzensiz yerleştirilmiş olan  internet erişim kabini kaldırımın tamamının kullanımına engel oluyor.",
    "activityLatitude": 39.9668025,
    "activityLongitude": 32.5885711,
    "activityDate": "2023-04-23T14:19:25.239267+00:00",
    "activityType": "Bad Sidewalk",
    "photos": [
        "https://peer-review.hacettepe.edu.tr/ecosnap-photos/0482626d-f762-492c-85a6-e62b383d0b7d.jpg",
        "https://peer-review.hacettepe.edu.tr/ecosnap-photos/41006bfa-f295-4b2e-89cc-84942e52a466.jpeg",
        "https://peer-review.hacettepe.edu.tr/ecosnap-photos/6e8cf392-a67c-49da-b897-9d56fbb4a652.jpeg"
    ]
}
 ----> Bad Sidewalk Coordinates (lat/lon): 39.9668025 32.5885711

```

## FOLIUM

** With the knowledge of the obtained data, there is a code with a folium library where points are specified on the open street map. You can use openfile for detailed inspection.

* The required libraries are imported for the code.

```
import folium
from folium.plugins import MarkerCluster
import pandas as pd

```

* Then, the lat, long information in the json files we obtained with the previous coding are drawn from the data and assigned to the variables in order.

```
a , b = data_1['activityLatitude'] , data_1['activityLongitude']
c, d =  data_2['activityLatitude'] , data_2['activityLongitude']
e, f  = data_3['activityLatitude'] , data_3['activityLongitude']
h, z =  data_4['activityLatitude'] , data_4['activityLongitude']
k ,l =  data_5['activityLatitude'] , data_5['activityLongitude']
m, n =  data_6['activityLatitude'] , data_6['activityLongitude']

```
* A broad bounded osm map covering the study area is obtained.

```

boulder_coords = [39.9670000 , 32.5880000]

my_map = folium.Map(location = boulder_coords, zoom_start = 16.5)

my_map

```

* The variables whose coordinate information is obtained are assigned as points and marked on the map with the name "activity name or type" to be descriptive on the map.

```
point_1 = [a, b]
point_2 = [c, d]
point_3 = [e, f]
point_4 = [h, z]
point_5 = [k, l]
point_6 = [m, n]

folium.Marker(point_1, popup = data_1['activityType']).add_to(my_map)
folium.Marker(point_2, popup = data_2['activityName']).add_to(my_map)
folium.Marker(point_3, popup = data_3['activityName']).add_to(my_map)
folium.Marker(point_4, popup = data_4['activityName']).add_to(my_map)
folium.Marker(point_5, popup = data_5['activityName']).add_to(my_map)
folium.Marker(point_6, popup = data_6['activityName']).add_to(my_map)


my_map

```

## MY MAP

** Locations where problems are found in my posts

<img src="./readme images/My_map.png" alt="alt yazı" >


## CONCLUSION

* As a result, with this project, I got to know the ecosnap application, used it and displayed and marked these regions on the map using a programming language with the data I shared.

### * My User Comments :

* As someone who has gained experience with the application, I think that the 1-hour limit on post sharing restricts the user from using the application actively. In addition, I think that sharing the solutions found to the problems in the environment will contribute to the problems. In the Activity type section, I would prefer the user to edit and name the other problem part. Comments can be taken into account for improvements to be made in the future use of the application.

