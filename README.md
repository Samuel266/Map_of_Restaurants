<!DOCTYPE html>
<html lang="en">

 <head>
    <title>CUISINE WebMap </title>
    <meta charset="UTF-8">
    <title> CUISINE</title>

    <!--inport leaflet styling-->
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.0.3/dist/leaflet.css">
    <!--Import jquery library-->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script> 

</head>
<body>
    <h3 style="text-align: center; font-family: sans-serif; "><u>MAP</u> <u>OF</u> <u>RESTAURANTS</u></h3>
  <!--map  element-->
    <div id="map" style="width: 100%; height:500px;position:absolute;top:10%"></div>

    </div>
    <!--import leaflet library-->
    <script src="https://unpkg.com/leaflet@1.0.3/dist/leaflet.js"></script>


     
     

    <!--javascript-->
    <script>
        //map object
        var map1 = document.getElementById("map");
        var map = L.map(map1, {
            center: [0.000, 38.000],
            zoom: 6,
            scrollWheelZoom: true,

        });
        //base map
        L.tileLayer("http://{s}.tile.osm.org/{z}/{x}/{y}.png", {
            attribution: ""
        }).addTo(map);

        //data
        var data = [{
            "address": {
                "building": "1",
                "coord": [39.666667, -4.05],
                "street": "Park Ave",
                "postcode": "10462"
            },
            "cuisine": "Bakery",
            "grades": [{
                "date": {
                    "$date": 1393804800000
                },
                "grade": "A",
                "score": 2
            }, {
                "date": {
                    "$date": 1378857600000
                },
                "grade": "A",
                "score": 6
            }, {
                "date": {
                    "$date": 1358985600000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1322006400000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1299715200000
                },
                "grade": "B",
                "score": 14
            }],
            "name": "Bake Shop",
            "restaurant_id": "30075445"
        }, {
            "address": {
                "building": "2",
                "coord": [39.460278, -4.174444],
                "street": "Flat Avenue",
                "postcode": "11225"
            },
            "cuisine": "Hamburgers",
            "grades": [{
                "date": {
                    "$date": 1419897600000
                },
                "grade": "A",
                "score": 8
            }, {
                "date": {
                    "$date": 1404172800000
                },
                "grade": "B",
                "score": 23
            }, {
                "date": {
                    "$date": 1367280000000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1336435200000
                },
                "grade": "A",
                "score": 12
            }],
            "name": "Wendy'S",
            "restaurant_id": "30112340"
        }, {
            "address": {
                "building": "3",
                "coord": [39.85, -3.633333],
                "street": "West 57 Street",
                "postcode": "10019"
            },
            "cuisine": "Irish",
            "grades": [{
                "date": {
                    "$date": 1409961600000
                },
                "grade": "A",
                "score": 2
            }, {
                "date": {
                    "$date": 1374451200000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1343692800000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1325116800000
                },
                "grade": "A",
                "score": 12
            }],
            "name": "Dj Restaurant",
            "restaurant_id": "30191841"
        }, {
            "address": {
                "building": "4",
                "coord": [40.033333, -1.5],
                "street": "Stillwell Avenue",
                "postcode": "11224"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1402358400000
                },
                "grade": "A",
                "score": 5
            }, {
                "date": {
                    "$date": 1370390400000
                },
                "grade": "A",
                "score": 7
            }, {
                "date": {
                    "$date": 1334275200000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1318377600000
                },
                "grade": "A",
                "score": 12
            }],
            "name": "Riviera Caterer",
            "restaurant_id": "40356018"
        }, {
            "address": {
                "building": "5",
                "coord": [40.902222, -2.269444],
                "street": "63 Road",
                "postcode": "11374"
            },
            "cuisine": "Jewish/Kosher",
            "grades": [{
                "date": {
                    "$date": 1416787200000
                },
                "grade": "Z",
                "score": 20
            }, {
                "date": {
                    "$date": 1358380800000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1343865600000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1323907200000
                },
                "grade": "B",
                "score": 25
            }],
            "name": "Tov Kosher Kitchen",
            "restaurant_id": "40356068"
        }, {
            "address": {
                "building": "6",
                "coord": [38.377778, -3.504722],
                "street": "Astoria",
                "postcode": "11369"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1416009600000
                },
                "grade": "Z",
                "score": 38
            }, {
                "date": {
                    "$date": 1398988800000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1362182400000
                },
                "grade": "A",
                "score": 7
            }, {
                "date": {
                    "$date": 1328832000000
                },
                "grade": "A",
                "score": 13
            }],
            "name": "Brunos On The Boulevard",
            "restaurant_id": "40356151"
        }, {
            "address": {
                "building": "7",
                "coord": [39.658333, -0.456944],
                "street": "Victory",
                "postcode": "10314"
            },
            "cuisine": "Jewish/Kosher",
            "grades": [{
                "date": {
                    "$date": 1412553600000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1400544000000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1365033600000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1327363200000
                },
                "grade": "A",
                "score": 9
            }],
            "name": "Kosher Island",
            "restaurant_id": "40356442"
        }, {
            "address": {
                "building": "8",
                "coord": [40.05, 1.75],
                "street": "Avenue U",
                "postcode": "11234"
            },
            "cuisine": "Delicatessen",
            "grades": [{
                "date": {
                    "$date": 1401321600000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1389657600000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1375488000000
                },
                "grade": "A",
                "score": 8
            }, {
                "date": {
                    "$date": 1342569600000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1331251200000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1318550400000
                },
                "grade": "A",
                "score": 9
            }],
            "name": "Wilken'S Fine Food",
            "restaurant_id": "40356483"
        }, {
            "address": {
                "building": "9",
                "coord": [41.833333, 3.916667],
                "street": "11 Avenue",
                "postcode": "11219"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1405641600000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1375142400000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1360713600000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1345075200000
                },
                "grade": "A",
                "score": 2
            }, {
                "date": {
                    "$date": 1313539200000
                },
                "grade": "A",
                "score": 11
            }],
            "name": "Regina Caterers",
            "restaurant_id": "40356649"
        }, {
            "address": {
                "building": "10",
                "coord": [37.983333, 2.333333],
                "street": "Nostrand Avenue",
                "postcode": "11226"
            },
            "cuisine": "Ice Cream, Gelato, Yogurt, Ices",
            "grades": [{
                "date": {
                    "$date": 1405296000000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1373414400000
                },
                "grade": "A",
                "score": 8
            }, {
                "date": {
                    "$date": 1341964800000
                },
                "grade": "A",
                "score": 5
            }, {
                "date": {
                    "$date": 1329955200000
                },
                "grade": "A",
                "score": 8
            }],
            "name": "Taste The Tropics Ice Cream",
            "restaurant_id": "40356731"
        }, {
            "address": {
                "building": "11",
                "coord": [37.583333, 0.35],
                "street": "Southern Blues",
                "postcode": "10460"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1401235200000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1371600000000
                },
                "grade": "A",
                "score": 4
            }, {
                "date": {
                    "$date": 1339718400000
                },
                "grade": "A",
                "score": 3
            }],
            "name": "Wild Asia",
            "restaurant_id": "40357217"
        }, {
            "address": {
                "building": "12",
                "coord": [37.65, 0.05],
                "street": "18 Avenue",
                "postcode": "11214"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1397606400000
                },
                "grade": "A",
                "score": 5
            }, {
                "date": {
                    "$date": 1366675200000
                },
                "grade": "A",
                "score": 2
            }, {
                "date": {
                    "$date": 1335225600000
                },
                "grade": "A",
                "score": 5
            }, {
                "date": {
                    "$date": 1323993600000
                },
                "grade": "A",
                "score": 2
            }],
            "name": "C & C Catering Service",
            "restaurant_id": "40357437"
        }, {
            "address": {
                "building": "13",
                "coord": [37.65, -0.333333],
                "street": "Sutter Avenue",
                "postcode": "11208"
            },
            "cuisine": "Chinese",
            "grades": [{
                "date": {
                    "$date": 1410825600000
                },
                "grade": "B",
                "score": 21
            }, {
                "date": {
                    "$date": 1377648000000
                },
                "grade": "A",
                "score": 7
            }, {
                "date": {
                    "$date": 1364860800000
                },
                "grade": "C",
                "score": 56
            }, {
                "date": {
                    "$date": 1344988800000
                },
                "grade": "B",
                "score": 27
            }, {
                "date": {
                    "$date": 1332892800000
                },
                "grade": "B",
                "score": 27
            }],
            "name": "May May Kitchen",
            "restaurant_id": "40358429"
        }, {
            "address": {
                "building": "14",
                "coord": [37.45, -0.533333],
                "street": "East 66 Street",
                "postcode": "10065"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1399420800000
                },
                "grade": "A",
                "score": 3
            }, {
                "date": {
                    "$date": 1367539200000
                },
                "grade": "A",
                "score": 4
            }, {
                "date": {
                    "$date": 1335744000000
                },
                "grade": "A",
                "score": 6
            }, {
                "date": {
                    "$date": 1324944000000
                },
                "grade": "A",
                "score": 0
            }],
            "name": "1 East 66Th Street Kitchen",
            "restaurant_id": "40359480"
        }, {
            "address": {
                "building": "15",
                "coord": [38.016667, -1.366667],
                "street": "Kings Highway",
                "postcode": "11223"
            },
            "cuisine": "Jewish/Kosher",
            "grades": [{
                "date": {
                    "$date": 1415577600000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1381363200000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1349308800000
                },
                "grade": "A",
                "score": 7
            }, {
                "date": {
                    "$date": 1337558400000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1325203200000
                },
                "grade": "B",
                "score": 19
            }],
            "name": "Seuda Foods",
            "restaurant_id": "40360045"
        }, {
            "address": {
                "building": "16",
                "coord": [37.266667, -1.516667],
                "street": "Church Avenue",
                "postcode": "11218"
            },
            "cuisine": "Ice Cream, Gelato, Yogurt, Ices",
            "grades": [{
                "date": {
                    "$date": 1391990400000
                },
                "grade": "A",
                "score": 2
            }, {
                "date": {
                    "$date": 1357084800000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1326067200000
                },
                "grade": "A",
                "score": 3
            }, {
                "date": {
                    "$date": 1320624000000
                },
                "grade": "P",
                "score": 12
            }, {
                "date": {
                    "$date": 1311206400000
                },
                "grade": "A",
                "score": 13
            }],
            "name": "Carvel Ice Cream",
            "restaurant_id": "40360076"
        }, {
            "address": {
                "building": "17",
                "coord": [37.633333, -1.783333],
                "street": "Hillside Avenue",
                "postcode": "11004"
            },
            "cuisine": "Ice Cream, Gelato, Yogurt, Ices",
            "grades": [{
                "date": {
                    "$date": 1414454400000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1379462400000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1348099200000
                },
                "grade": "A",
                "score": 13
            }],
            "name": "Carvel Ice Cream",
            "restaurant_id": "40361322"
        }, {
            "address": {
                "building": "18",
                "coord": [36.633333, -0.45],
                "street": "3 Avenue",
                "postcode": "11209"
            },
            "cuisine": "Delicatessen",
            "grades": [{
                "date": {
                    "$date": 1408579200000
                },
                "grade": "A",
                "score": 4
            }, {
                "date": {
                    "$date": 1393977600000
                },
                "grade": "A",
                "score": 3
            }, {
                "date": {
                    "$date": 1357776000000
                },
                "grade": "A",
                "score": 10
            }],
            "name": "Nordic Delicacies",
            "restaurant_id": "40361390"
        }, {
            "address": {
                "building": "19",
                "coord": [36.95, -0.416667],
                "street": "East 174 Street",
                "postcode": "10021"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1409616000000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1387411200000
                },
                "grade": "B",
                "score": 16
            }, {
                "date": {
                    "$date": 1369699200000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1354838400000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1332979200000
                },
                "grade": "A",
                "score": 11
            }],
            "name": "Glorious Food",
            "restaurant_id": "40361521"
        }, {
            "address": {
                "building": "20",
                "coord": [37.283333, -0.5],
                "street": "1 Park West",
                "postcode": "11215"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1416355200000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1384387200000
                },
                "grade": "A",
                "score": 2
            }, {
                "date": {
                    "$date": 1354665600000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1337212800000
                },
                "grade": "A",
                "score": 11
            }],
            "name": "The Movable Feast",
            "restaurant_id": "40361606"
        }, {
            "address": {
                "building": "21",
                "coord": [37.15, -0.716667],
                "street": "20 Avenue",
                "postcode": "11356"
            },
            "cuisine": "Delicatessen",
            "grades": [{
                "date": {
                    "$date": 1408147200000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1377561600000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1348099200000
                },
                "grade": "A",
                "score": 7
            }, {
                "date": {
                    "$date": 1317254400000
                },
                "grade": "A",
                "score": 10
            }],
            "name": "Sal'S Deli",
            "restaurant_id": "40361618"
        }, {
            "address": {
                "building": "22",
                "coord": [36.816667, -1.166667],
                "street": "Broadway",
                "postcode": "10003"
            },
            "cuisine": "Delicatessen",
            "grades": [{
                "date": {
                    "$date": 1390262400000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1357257600000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1339027200000
                },
                "grade": "A",
                "score": 6
            }, {
                "date": {
                    "$date": 1326758400000
                },
                "grade": "A",
                "score": 8
            }],
            "name": "Bully'S Deli",
            "restaurant_id": "40361708"
        }, {
            "address": {
                "building": "23",
                "coord": [35.6, 3.116667],
                "street": "10 Street",
                "postcode": "11106"
            },
            "cuisine": "Delicatessen",
            "grades": [{
                "date": {
                    "$date": 1395187200000
                },
                "grade": "A",
                "score": 3
            }, {
                "date": {
                    "$date": 1363132800000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1332806400000
                },
                "grade": "A",
                "score": 8
            }, {
                "date": {
                    "$date": 1301961600000
                },
                "grade": "A",
                "score": 7
            }],
            "name": "Steve Chu'S Deli & Grocery",
            "restaurant_id": "40361998"
        }, {
            "address": {
                "building": "24",
                "coord": [35.116667, 1.233333],
                "street": "Ams Avenue",
                "postcode": "10024"
            },
            "cuisine": "Chicken",
            "grades": [{
                "date": {
                    "$date": 1410739200000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1393891200000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1374105600000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1357689600000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1334016000000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1321315200000
                },
                "grade": "A",
                "score": 7
            }],
            "name": "Harriet'S Kitchen",
            "restaurant_id": "40362098"
        }, {
            "address": {
                "building": "25",
                "coord": [36.7, 1.1],
                "street": "Columbus Avenue",
                "postcode": "10025"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1410480000000
                },
                "grade": "B",
                "score": 26
            }, {
                "date": {
                    "$date": 1377648000000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1364169600000
                },
                "grade": "B",
                "score": 20
            }, {
                "date": {
                    "$date": 1329177600000
                },
                "grade": "A",
                "score": 12
            }],
            "name": "P & S Deli Grocery",
            "restaurant_id": "40362264"
        }, {
            "address": {
                "building": "26",
                "coord": [35.283333, 0.516667],
                "street": "West 4 Street",
                "postcode": "10012"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1396483200000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1365120000000
                },
                "grade": "A",
                "score": 4
            }, {
                "date": {
                    "$date": 1332288000000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1303862400000
                },
                "grade": "A",
                "score": 5
            }],
            "name": "Angelika Film Center",
            "restaurant_id": "40362274"
        }, {
            "address": {
                "building": "27",
                "coord": [35.0, 1.016667],
                "street": "Myrtle Avenue",
                "postcode": "11205"
            },
            "cuisine": "Hamburgers",
            "grades": [{
                "date": {
                    "$date": 1395100800000
                },
                "grade": "A",
                "score": 8
            }, {
                "date": {
                    "$date": 1363564800000
                },
                "grade": "A",
                "score": 8
            }, {
                "date": {
                    "$date": 1349827200000
                },
                "grade": "A",
                "score": 7
            }, {
                "date": {
                    "$date": 1316649600000
                },
                "grade": "A",
                "score": 2
            }],
            "name": "White Castle",
            "restaurant_id": "40362344"
        }, {
            "address": {
                "building": "28",
                "coord": [35.508333, 0.673056],
                "street": "37 Avenue",
                "postcode": "11368"
            },
            "cuisine": "Chinese",
            "grades": [{
                "date": {
                    "$date": 1398038400000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1384214400000
                },
                "grade": "A",
                "score": 5
            }, {
                "date": {
                    "$date": 1370304000000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1352851200000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1349913600000
                },
                "grade": "P",
                "score": 0
            }, {
                "date": {
                    "$date": 1337817600000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1323302400000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1311120000000
                },
                "grade": "A",
                "score": 11
            }],
            "name": "Ho Mei Restaurant",
            "restaurant_id": "40362432"
        }, {
            "address": {
                "building": "29",
                "coord": [35.166667, 0.333333],
                "street": "Wall Street",
                "postcode": "10005"
            },
            "cuisine": "Turkish",
            "grades": [{
                "date": {
                    "$date": 1411689600000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1379462400000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1348185600000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1336521600000
                },
                "grade": "A",
                "score": 11
            }],
            "name": "The Country Cafe",
            "restaurant_id": "40362715"
        }, {
            "address": {
                "building": "30",
                "coord": [35.75, 0.5],
                "street": "East   56 Street",
                "postcode": "11203"
            },
            "cuisine": "Caribbean",
            "grades": [{
                "date": {
                    "$date": 1399939200000
                },
                "grade": "A",
                "score": 2
            }, {
                "date": {
                    "$date": 1367971200000
                },
                "grade": "A",
                "score": 7
            }, {
                "date": {
                    "$date": 1348272000000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1307318400000
                },
                "grade": "A",
                "score": 12
            }],
            "name": "Shashemene Int'L Restaura",
            "restaurant_id": "40362869"
        }, {
            "address": {
                "building": "31",
                "coord": [37.066667, 0.016667],
                "street": "Church Street",
                "postcode": "10007"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1405641600000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1393372800000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1377475200000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1359676800000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1326758400000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1318896000000
                },
                "grade": "A",
                "score": 11
            }],
            "name": "Downtown Deli",
            "restaurant_id": "40363021"
        }, {
            "address": {
                "building": "32",
                "coord": [36.066667, -0.3],
                "street": "East 233 Street",
                "postcode": "10466"
            },
            "cuisine": "Ice Cream, Gelato, Yogurt, Ices",
            "grades": [{
                "date": {
                    "$date": 1398297600000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1378339200000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1361404800000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1341273600000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1310342400000
                },
                "grade": "A",
                "score": 5
            }],
            "name": "Carvel Ice Cream",
            "restaurant_id": "40363093"
        }, {
            "address": {
                "building": "33",
                "coord": [35.866667, -1.083333],
                "street": "Court Street",
                "postcode": "11201"
            },
            "cuisine": "Donuts",
            "grades": [{
                "date": {
                    "$date": 1419897600000
                },
                "grade": "A",
                "score": 8
            }, {
                "date": {
                    "$date": 1389744000000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1357603200000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1326931200000
                },
                "grade": "A",
                "score": 10
            }],
            "name": "Dunkin' Donuts",
            "restaurant_id": "40363098"
        }, {
            "address": {
                "building": "34",
                "coord": [36.783333, -1.85],
                "street": "5 Avenue",
                "postcode": "11209"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1417651200000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1382572800000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1366243200000
                },
                "grade": "A",
                "score": 5
            }, {
                "date": {
                    "$date": 1333584000000
                },
                "grade": "A",
                "score": 13
            }],
            "name": "Mejlander & Mulgannon",
            "restaurant_id": "40363117"
        }, {
            "address": {
                "building": "35",
                "coord": [35.3, -0.366667],
                "street": "Prince Street",
                "postcode": "10012"
            },
            "cuisine": "Bakery",
            "grades": [{
                "date": {
                    "$date": 1413504000000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1379462400000
                },
                "grade": "A",
                "score": 13
            }, {
                "date": {
                    "$date": 1367280000000
                },
                "grade": "A",
                "score": 7
            }, {
                "date": {
                    "$date": 1334880000000
                },
                "grade": "A",
                "score": 7
            }, {
                "date": {
                    "$date": 1324252800000
                },
                "grade": "A",
                "score": 3
            }],
            "name": "Olive'S",
            "restaurant_id": "40363151"
        }, {
            "address": {
                "building": "36",
                "coord": [35.35, -0.783333],
                "street": "238 Ave",
                "postcode": "10474"
            },
            "cuisine": "Chinese",
            "grades": [{
                "date": {
                    "$date": 1388361600000
                },
                "grade": "A",
                "score": 8
            }, {
                "date": {
                    "$date": 1357603200000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1339459200000
                },
                "grade": "B",
                "score": 15
            }],
            "name": "Happy Garden",
            "restaurant_id": "40363289"
        }, {
            "address": {
                "building": "37",
                "coord": [34.75, 0.283333],
                "street": "8 Avenue",
                "postcode": "10018"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1402272000000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1389312000000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1354838400000
                },
                "grade": "A",
                "score": 4
            }, {
                "date": {
                    "$date": 1323734400000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1315526400000
                },
                "grade": "A",
                "score": 13
            }],
            "name": "Cafe Metro",
            "restaurant_id": "40363298"
        }, {
            "address": {
                "building": "38",
                "coord": [34.725, 0.05],
                "street": "Wyckoff Avenue",
                "postcode": "11385"
            },
            "cuisine": "Delicatessen",
            "grades": [{
                "date": {
                    "$date": 1399507200000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1386806400000
                },
                "grade": "A",
                "score": 8
            }, {
                "date": {
                    "$date": 1371772800000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1356307200000
                },
                "grade": "B",
                "score": 25
            }, {
                "date": {
                    "$date": 1318982400000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1308096000000
                },
                "grade": "A",
                "score": 10
            }],
            "name": "Tony'S Deli",
            "restaurant_id": "40363333"
        }, {
            "address": {
                "building": "39",
                "coord": [34.566667, 0.566667],
                "street": "Lexington Avenue",
                "postcode": "10174"
            },
            "cuisine": "Sandwiches/Salads/Mixed Buffet",
            "grades": [{
                "date": {
                    "$date": 1392940800000
                },
                "grade": "A",
                "score": 3
            }, {
                "date": {
                    "$date": 1379030400000
                },
                "grade": "A",
                "score": 3
            }, {
                "date": {
                    "$date": 1346112000000
                },
                "grade": "A",
                "score": 0
            }, {
                "date": {
                    "$date": 1315872000000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1304380800000
                },
                "grade": "A",
                "score": 5
            }],
            "name": "Lexler Deli",
            "restaurant_id": "40363426"
        }, {
            "address": {
                "building": "40",
                "coord": [34.125, 0.453056],
                "street": "Victory",
                "postcode": "10314"
            },
            "cuisine": "Delicatessen",
            "grades": [{
                "date": {
                    "$date": 1420761600000
                },
                "grade": "A",
                "score": 3
            }, {
                "date": {
                    "$date": 1386201600000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1371600000000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1357603200000
                },
                "grade": "A",
                "score": 11
            }],
            "name": "Bagels N Buns",
            "restaurant_id": "40363427"
        }, {
            "address": {
                "building": "41",
                "coord": [34.283333, 0.066667],
                "street": "Metropolitan Avenue",
                "postcode": "11379"
            },
            "cuisine": "Bagels/Pretzels",
            "grades": [{
                "date": {
                    "$date": 1410912000000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1389830400000
                },
                "grade": "B",
                "score": 23
            }, {
                "date": {
                    "$date": 1375833600000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1361404800000
                },
                "grade": "B",
                "score": 27
            }, {
                "date": {
                    "$date": 1340150400000
                },
                "grade": "B",
                "score": 27
            }, {
                "date": {
                    "$date": 1327968000000
                },
                "grade": "B",
                "score": 18
            }],
            "name": "Hot Bagels",
            "restaurant_id": "40363565"
        }, {
            "address": {
                "building": "42",
                "coord": [34.75, -0.1],
                "street": "Lefferts",
                "postcode": "11418"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1393286400000
                },
                "grade": "A",
                "score": 7
            }, {
                "date": {
                    "$date": 1376438400000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1344297600000
                },
                "grade": "A",
                "score": 7
            }, {
                "date": {
                    "$date": 1332720000000
                },
                "grade": "A",
                "score": 10
            }, {
                "date": {
                    "$date": 1320364800000
                },
                "grade": "A",
                "score": 0
            }, {
                "date": {
                    "$date": 1309305600000
                },
                "grade": "A",
                "score": 4
            }],
            "name": "Snack Time Grill",
            "restaurant_id": "40363590"
        }, {
            "address": {
                "building": "43",
                "coord": [34.45, -0.516667],
                "street": "Third Avenue",
                "postcode": "10028"
            },
            "cuisine": "Continental",
            "grades": [{
                "date": {
                    "$date": 1401667200000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1388102400000
                },
                "grade": "A",
                "score": 8
            }, {
                "date": {
                    "$date": 1363564800000
                },
                "grade": "B",
                "score": 26
            }, {
                "date": {
                    "$date": 1328054400000
                },
                "grade": "A",
                "score": 7
            }, {
                "date": {
                    "$date": 1309910400000
                },
                "grade": "B",
                "score": 25
            }],
            "name": "Lorenzo & Maria'S",
            "restaurant_id": "40363630"
        }, {
            "address": {
                "building": "44",
                "coord": [34.833333, -0.666667],
                "street": "3 Avenue",
                "postcode": "10016"
            },
            "borough": "Manhattan",
            "cuisine": "Pizza",
            "grades": [{
                "date": {
                    "$date": 1407196800000
                },
                "grade": "A",
                "score": 3
            }, {
                "date": {
                    "$date": 1394064000000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1373328000000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1359504000000
                },
                "grade": "A",
                "score": 4
            }, {
                "date": {
                    "$date": 1325721600000
                },
                "grade": "A",
                "score": 2
            }, {
                "date": {
                    "$date": 1316995200000
                },
                "grade": "A",
                "score": 0
            }],
            "name": "Domino'S Pizza",
            "restaurant_id": "40363644"
        }, {
            "address": {
                "building": "45",
                "coord": [34.766667, -0.683333],
                "street": "Madison Avenue",
                "postcode": "10022"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1401753600000
                },
                "grade": "A",
                "score": 9
            }, {
                "date": {
                    "$date": 1370563200000
                },
                "grade": "A",
                "score": 5
            }, {
                "date": {
                    "$date": 1340928000000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1328486400000
                },
                "grade": "A",
                "score": 11
            }, {
                "date": {
                    "$date": 1308787200000
                },
                "grade": "A",
                "score": 13
            }],
            "name": "Berkely",
            "restaurant_id": "40363685"
        }, {
            "address": {
                "building": "46",
                "coord": [34.914, -0.521],
                "street": "East 92 Street",
                "postcode": "11236"
            },
            "cuisine": "American ",
            "grades": [{
                "date": {
                    "$date": 1391558400000
                },
                "grade": "A",
                "score": 0
            }, {
                "date": {
                    "$date": 1359417600000
                },
                "grade": "A",
                "score": 3
            }, {
                "date": {
                    "$date": 1323302400000
                },
                "grade": "A",
                "score": 10
            }],
            "name": "Sonny'S Heros",
            "restaurant_id": "40363744"
        }, {
            "address": {
                "building": "47",
                "coord": [36.816667, -1.283333],
                "street": "Hylan",
                "postcode": "10305"
            },
            "cuisine": "Ice Cream, Gelato, Yogurt, Ices",
            "grades": [{
                "date": {
                    "$date": 1398297600000
                },
                "grade": "A",
                "score": 12
            }, {
                "date": {
                    "$date": 1361836800000
                },
                "grade": "A",
                "score": 5
            }, {
                "date": {
                    "$date": 1328140800000
                },
                "grade": "A",
                "score": 2
            }],
            "name": "Carvel Ice Cream",
            "restaurant_id": "40363834"
        }];

        //bind  data with popups on mousover
        for (d in data) {
            var coords = L.latLng({
                lat: data[d].address.coord[1],
                lng: data[d].address.coord[0]
            });

            var point = L.marker(coords).bindPopup(`<p style="font-weight: underline;">${data[d].name}</p> <p style="font-style: bold;">${data[d].cuisine} cuisine</p>`);
            point.on('mouseover', function() {
                this.openPopup();
            });
            point.on('mouseout', function() {
                this.closePopup();
            });
            point.addTo(map);


        }
    </script>
 
   
     <footer style="float:bottom;position:absolute;height:1px;width:1px; bottom:0%;right:100%">
<p><p>
<p></p>
   <style>
			.footer {
   				position:absolute;
  				 bottom:0;
  				 width:100%;
  				 height:60px;   
  				 background:grey;
  			}
 }
		</style> 
<div class="footer">
			<div class="column"> 
				<p><b>Contributors</b></p> 
				<ul style="list-style-type:disc"> 
					<li>SAMUEL OTEYO</li> 
					<li>Consultants</li> 
					
				</ul> 
			</div> 
				
			<div class="column"> 
				<p><b>Authors</b></p> 
				<ul> 
					<li><b>SAMUEL ONKENDI</b><br></li>
                        <li>ENC222-0163/2017</li> 

				</ul> 
			</div> 
				
			<div class="column"> 
				<p><b>Marginal information</b>	</p> 
				<ul> 
					
					<li><u>Year</u>:2020</li>
					<li><u>Publisher</u>:Survey of Kenya</li> 
			

				</ul> 
			</div> 
</footer>




</body>
