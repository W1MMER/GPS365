# GPS365 Trackers
The GF21 is a small lightweight GPS Tracker that works over cellular to be tracked from anywhere.

**Base URL**: `http://120.76.241.191/n365_ilist.php`

**Base URL**: `365gps.com/n365_ilist.php`

**Base URL**: `gps365.com/n365_ilist.php`

**Method**: `GET`

**Parameters**:

| Parameters | Value                    |
| ---------- | ------------------------ |
| imei       | tracker-imei             |
| pw         | tracker-password         |

The Response should yield something like this:

```
[
    {
        "login": "<TRACKER-NAME>",
        "imei": "<TRACKER-IMEI>",
        "name": "303_302",
        "carno": "3",
        "gps": "2020-07-13 3:07:34,0,2,0,0,<LATITUDE>,<LONGITUDE>,0",
        "log": "IN 2020-07-13 3:08:48",
        "google": "<LATITUDE>,<LONGITUDE>",
        "baidu": "<LATITUDE>,<LONGITUDE>",
        "speed": null,
        "bat": "68",
        "icon": "2",
        "marker": "2",
        "device": "303",
        "ver": "77;0000;0",
        "sec": "120",
        "level": "40",
        "expdate": null,
        "loc": "FF",
        "onoff": "3",
        "gexpdate": null,
        "iccid": "<TRACKER-ICCID>",
        "ggkey": null,
        "startdate": "2020-01-13"
    }
]
```

**Other Endpoints**

**Method**: `GET` or `POST` (it doesn't matter)

Turn LED's Off: `gps365.com/n365_ilist.php?hw=iOS&imei=TRACKER-IMEI&req=44`
    
Turn LED's On: `gps365.com/n365_ilist.php?hw=iOS&imei=TRACKER-IMEI&req=45`
    
Remote Reboot: `gps365.com/n365_ilist.phpgps365.com/n365_ilist.php?hw=iOS&imei=TRACKER-IMEI&req=48`
    
Remote Shutdown: `gps365.com/n365_ilist.php?hw=iOS&imei=TRACKER-IMEI&req=49`
    
Change GPS Update Time: `gps365.com/n365_ilist.php?hw=iOS&imei=TRACKER-IMEI&login=tracker-imei&sec=120`

Request New GPS Location?: `gps365.com/n365_ilist.php?hw=iOS&imei=TRACKER-IMEI&t=1` - Not entirely sure if this works as I haven't seen a GPS Update when command is sent
