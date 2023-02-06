# Data-structures
Contains all data-structures that are used by the FlexMill-project

## JSON-Data
Add a robot:
```json
{
    "version": "1.2",
    "name": "FlexMill robot",
    "status": "idle",
    "battery": "80",
    "macAddress": "cc4b73b20a20",
    "id": "urn:ngsi-ld:AMR:cc4b73b20a20",
    "refDestination": "urn:ngsi-ld:Idlestation:01",
    "type": "AMR"
}
```

Add Toolcenter:
```json
{
"location": {
  "type": "Point",
  "coordinates": [7.5328, -1.2],
    "metadata": {
       "angle": 1.58021
    }
 },
    "name": "Toolcenter",
    "status": "ready",
    "id": "urn:ngsi-ld:Warehouse:01",
    "type": "Warehouse"
}
```

Add Workstation 1:
```json
{
"location": {
  "type": "Point",
  "coordinates": [30.8749, 27.4959],
    "metadata": {
       "angle": 1.57418 
    }
 },
    "name": "1065",
    "status": "ready",
    "id": "urn:ngsi-ld:Workstation:1065",
    "type": "Workstation"
}
```

Add Workstation 2:
```json
{
"location": {
  "type": "Point",
  "coordinates": [11.4510, 31.9264],
    "metadata": {
       "angle": -0.0868751 
    }
 },
 "name": "1044",
 "status": "ready",
 "id": "urn:ngsi-ld:Workstation:1044",
 "type": "Workstation"
}
```

Optional: Add additional workstations if needed

Add idle station, the robot is charged and parked here
```json
{
"location": {
  "type": "Point",
  "coordinates": [-1.4216, -0.9897],
  "metadata": {
     "angle": 1.598769    
  }
},
 "name": "Idlestation",
 "status": "ready",
 "id": "urn:ngsi-ld:Idlestation:01",
 "type": "Idlestation"  
}
```

Add one or more Workorders
The entries in tools and components are shown to the user in the interface. These parts have to be placed on the robot.
```json
{
	"status": "scheduled",
	"scheduledAt": "04/10/2022 08:19:30",
	"warehouseId": "urn:ngsi-ld:Warehouse:01",
	"workstationId": "urn:ngsi-ld:Workstation:1044",
	"materials": [
		{
			"tools": [
				{
					"id": "2000268",
					"turret": " 2",
					"station": " 1",
					"orientation": " 1"
				},
				{
					"id": "2000269",
					"turret": " 1",
					"station": " 6",
					"orientation": " 2"
				},
				{
					"id": "2000280",
					"turret": " 2",
					"station": " 5",
					"orientation": " 1"
				},
				{
					"id": "2001287",
					"turret": " 2",
					"station": " 6",
					"orientation": " 1"
				},
				{
					"id": "2001287",
					"turret": " 3",
					"station": " 4",
					"orientation": " 2"
				},
				{
					"id": "2003290",
					"turret": " 2",
					"station": " 4",
					"orientation": " 1"
				}
			]
		},
		{
			"components": [
				{
					"id": "1200446 "
				},
				{
					"id": "1200484 "
				},
				{
					"id": "1200486 "
				}
			]
		}
	],
	"id": "urn:ngsi-ld:WorkOrder:1",
	"dateCreated": "04/10/2022 08:19:30",
	"type": "WorkOrder"
}
```

Tool-life-cycle:
```json
[
    {
        "id": "102630_ToolLife",
        "type": "Tool_life",
        "102630": {
            "type": "1065",
            "value": [
                {
                    "id": "2000037",
                    "2000037": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "30"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "5"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "3"
                        }
                    }
                },
                {
                    "id": "2000039",
                    "2000039": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "250"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "5"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "204"
                        }
                    }
                },
                {
                    "id": "2000013",
                    "2000013": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "250"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "5"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "102"
                        }
                    }
                },
                {
                    "id": "2003328_SR",
                    "2003328_SR": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "350"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "5"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "155"
                        }
                    }
                },
                {
                    "id": "2003328_SL",
                    "2003328_SL": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "500"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "5"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "363"
                        }
                    }
                },
                {
                    "id": "2000511",
                    "2000511": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "320"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "5"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "302"
                        }
                    }
                },
                {
                    "id": "2000705",
                    "2000705": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "570"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "5"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "526"
                        }
                    }
                },
                {
                    "id": "2001180",
                    "2001180": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "400"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "5"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "338"
                        }
                    }
                },
                {
                    "id": "2000328",
                    "2000328": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "400"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "20"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "93"
                        }
                    }
                },
                {
                    "id": "2000052",
                    "2000052": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "150"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "5"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "21"
                        }
                    }
                }
            ],
            "metadata": {}
        }
    },
    {
        "id": "101177_ToolLife",
        "type": "Tool_life",
        "101177": {
            "type": "1045",
            "value": [
                {
                    "id": "2000037",
                    "2000037": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "20"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "5"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "13"
                        }
                    }
                },
                {
                    "id": "2000039",
                    "2000039": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "150"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "10"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "88"
                        }
                    }
                },
                {
                    "id": "2000511",
                    "2000511": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "30"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "10"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "23"
                        }
                    }
                },
                {
                    "id": "2000011",
                    "2000011": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "300"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "10"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "244"
                        }
                    }
                },
                {
                    "id": "2000007",
                    "2000007": {
                        "monitoringtype": {
                            "type": "Int",
                            "value": "2"
                        },
                        "targetquantity": {
                            "type": "Int",
                            "value": "250"
                        },
                        "warninglimit": {
                            "type": "Int",
                            "value": "10"
                        },
                        "actualquantity": {
                            "type": "Int",
                            "value": "213"
                        }
                    }
                }
            ],
            "metadata": {}
        }
    }
]
```


## SQL-Data
