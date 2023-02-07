# Data-structures
Contains all data-structures that are used by the FlexMill-project

# Table of contents
* [JSON-Data](#JSON-Data)
* [SQL-Data](#SQL-Data)


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

Machining-Centre-Data:
```json
{
	"id": "100357",
	"type": "MachiningData",
	"Batch": {
		"type": "Text",
		"value": "D65847"},
	"MachiningCentre": {
		"type": "Int",
		"value": 1044},
	"IdealCycleTime": {
		"type": "Second",
		"value": 104.51612903225806},
	"MachiningDateStart": {
		"type": "Date",
		"value": "2022-11-11"},
	"MachiningTimeStart": {
		"type": "Time", 
		"value": "21:28:47"}, 
	"MachiningDateEnd": {
		"type": "Date", 
		"value": "2022-11-11"},
	"MachiningTimeEnd": {
		"type": "Time", 
		"value": "21:30:46"},
	"GoodPartsCount": {
		"type": "Int", 
		"value": "0"},
	"GoodPartsDateStart": {
		"type": "Date",
		"value": "2022-11-10"},
	"GoodPartsDateEnd": {
		"type": "Date", 
		"value": "2022-11-10"}
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

### Structure of KPI_DATA
```SQL
-- Server-Version: 10.3.34-MariaDB-0ubuntu0.20.04.1

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET AUTOCOMMIT = 0;
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Datenbank: `flexmill`
--

-- --------------------------------------------------------

--
-- Tabellenstruktur für Tabelle `KPI_DATA`
--

CREATE TABLE `KPI_DATA` (
  `id` bigint(20) UNSIGNED NOT NULL COMMENT 'Index',
  `date` date DEFAULT NULL COMMENT 'The date of the calculated KPIs',
  `availability` float DEFAULT NULL COMMENT 'Percentage, 0-100, ',
  `performance` float DEFAULT NULL,
  `quality` float DEFAULT NULL,
  `ooe` float DEFAULT NULL,
  `machine_tool_uptime` int(11) DEFAULT NULL COMMENT 'Uptime in seconds',
  `machine_tool_downtime` int(11) DEFAULT NULL COMMENT 'Downtime in seconds',
  `seconds_today` int(11) DEFAULT NULL COMMENT 'Amount of seconds on this day',
  `total_parts_count` int(11) DEFAULT NULL COMMENT 'Total number of parts for this day',
  `good_parts_count` int(11) DEFAULT NULL COMMENT 'Good parts for this day',
  `gpc_mismatch` varchar(32) DEFAULT NULL COMMENT 'Shows if good_part_count is not matching total_parts_count',
  `ideal_cycle_time` float DEFAULT NULL COMMENT 'Stores the ideal cycle time, that ist calculated manually',
  `calculated_cycle_time` float DEFAULT NULL COMMENT 'Stores tha cycle time that is calculated baset on the production-data',
  `workpiece_id` varchar(64) DEFAULT NULL COMMENT 'Id of the workpiece the data is sent for',
  `batch` varchar(32) DEFAULT NULL COMMENT 'Name of the batch the workpiece belongs to',
  `machining_centre` int(11) DEFAULT NULL COMMENT 'Identifier of the machining centre'
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COMMENT='Contains KPIs per day';

--
-- Indizes der exportierten Tabellen
--

--
-- Indizes für die Tabelle `KPI_DATA`
--
ALTER TABLE `KPI_DATA`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `machining_centre + date` (`machining_centre`,`date`);

--
-- AUTO_INCREMENT für exportierte Tabellen
--

--
-- AUTO_INCREMENT für Tabelle `KPI_DATA`
--
ALTER TABLE `KPI_DATA`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT COMMENT 'Index';
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
```


### Structure of KPI_DATA_RAW

```SQL
-- Server-Version: 10.3.34-MariaDB-0ubuntu0.20.04.1

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET AUTOCOMMIT = 0;
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Datenbank: `flexmill`
--

-- --------------------------------------------------------

--
-- Tabellenstruktur für Tabelle `KPI_DATA_RAW`
--

CREATE TABLE `KPI_DATA_RAW` (
  `id` bigint(20) UNSIGNED NOT NULL COMMENT 'Index',
  `availability` float DEFAULT NULL COMMENT 'Percentage, 0-100, ',
  `performance` float DEFAULT NULL,
  `quality` float DEFAULT NULL,
  `ooe` float DEFAULT NULL,
  `workpiece_id` varchar(64) DEFAULT NULL COMMENT 'Id of the workpiece the data is sent for',
  `batch` varchar(32) DEFAULT NULL COMMENT 'Name of the batch the workpiece belongs to',
  `good_parts_count` int(10) UNSIGNED DEFAULT NULL COMMENT 'Current amount of good parts',
  `good_parts_date_start` date DEFAULT NULL,
  `good_parts_date_end` date DEFAULT NULL,
  `ideal_cycle_time` float UNSIGNED DEFAULT NULL COMMENT 'Ideal cycle time in seconds',
  `machining_centre` int(11) DEFAULT NULL COMMENT 'Identifier of the machining centre',
  `machining_date_start` date DEFAULT NULL,
  `machining_date_end` date DEFAULT NULL,
  `machining_time_start` time DEFAULT NULL COMMENT 'The time the machining started',
  `machining_time_end` time DEFAULT NULL COMMENT 'The time, the machining ended'
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COMMENT='Contains machining data that is needed to generate KPIs';

--
-- Indizes der exportierten Tabellen
--

--
-- Indizes für die Tabelle `KPI_DATA_RAW`
--
ALTER TABLE `KPI_DATA_RAW`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `machining_date_start + machining_centre + machining_time_start` (`machining_date_start`,`machining_centre`,`machining_time_start`) USING BTREE;

--
-- AUTO_INCREMENT für exportierte Tabellen
--

--
-- AUTO_INCREMENT für Tabelle `KPI_DATA_RAW`
--
ALTER TABLE `KPI_DATA_RAW`
  MODIFY `id` bigint(20) UNSIGNED NOT NULL AUTO_INCREMENT COMMENT 'Index';
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
```
