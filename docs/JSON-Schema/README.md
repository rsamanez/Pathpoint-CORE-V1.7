## KPI
* type : Required -  [100, 101] - 100 represents current value, 101 compares current value with past value
* name : Required - "KPI Name"
* shortName : Required - "KPI Short Name to show in GUI"
* measure : Required - One Object by City [BTR,WIC,PHX,LAS,OMA,HR]
  * accountID : 
  * city : Required - [BTR,WIC,PHX,LAS,OMA,HRD]
  * query : Required - The query changes depending on the KPI Type
  * link : Required - short Permalink, 
* value_type : Required - [INT, FLOAT]
* prefic : Required - some prefix to show in the GUI KPI, sample "$"
* suffix : Required - some suffix to show in the GUI KPI, sample "Orders"

#### KPI Type 101 Sample
```bash
"kpis": [
        {
            "type": 101,
            "name": "Unique Agents",
            "shortName": "U-Agent",
            "measure": [
                {
                    "accountID": 1345223,
                    "city": "BTR",
                    "query": "SELECT uniqueCount(operatorID) as value FROM Log COMPARE WITH 1 day ago",
                    "link": "https://onenr.io/0JBQrGyBNwZ"
                },
                {
                    "accountID": 1345223,
                    "city": "WIC",
                    "query": "SELECT uniqueCount(operatorID) as value FROM Log COMPARE WITH 1 day ago",
                    "link": "https://onenr.io/0JBQrGyBNwZ"
                },
                {
                    "accountID": 1345223,
                    "city": "PHX",
                    "query": "SELECT uniqueCount(operatorID) as value FROM Log COMPARE WITH 1 day ago",
                    "link": "https://onenr.io/0JBQrGyBNwZ"
                },
                {
                    "accountID": 1345223,
                    "city": "LAS",
                    "query": "SELECT uniqueCount(operatorID) as value FROM Log COMPARE WITH 1 day ago",
                    "link": "https://onenr.io/0JBQrGyBNwZ"
                },
                {
                    "accountID": 1345223,
                    "city": "OMA",
                    "query": "SELECT uniqueCount(operatorID) as value FROM Log COMPARE WITH 1 day ago",
                    "link": "https://onenr.io/0JBQrGyBNwZ"
                },
                {
                    "accountID": 1345223,
                    "city": "HRD",
                    "query": "SELECT uniqueCount(operatorID) as value FROM Log COMPARE WITH 1 day ago",
                    "link": "https://onenr.io/0JBQrGyBNwZ"
                }
            ],
            "value_type": "INT",
            "prefix": "",
            "suffix": ""
        }
    ]
```
#### KPI Type 100 Sample
```bash
"kpis": [
        {
            "type": 100,
            "name": "Unique Agents",
            "shortName": "U-Agent",
            "measure": [
                {
                    "accountID": 1345223,
                    "city": "BTR",
                    "query": "SELECT uniqueCount(operatorID) as value FROM Log",
                    "link": "https://onenr.io/0JBQrGyBNwZ"
                },
                {
                    "accountID": 1345223,
                    "city": "WIC",
                    "query": "SELECT uniqueCount(operatorID) as value FROM Log",
                    "link": "https://onenr.io/0JBQrGyBNwZ"
                },
                {
                    "accountID": 1345223,
                    "city": "PHX",
                    "query": "SELECT uniqueCount(operatorID) as value FROM Log",
                    "link": "https://onenr.io/0JBQrGyBNwZ"
                },
                {
                    "accountID": 1345223,
                    "city": "LAS",
                    "query": "SELECT uniqueCount(operatorID) as value FROM Log",
                    "link": "https://onenr.io/0JBQrGyBNwZ"
                },
                {
                    "accountID": 1345223,
                    "city": "OMA",
                    "query": "SELECT uniqueCount(operatorID) as value FROM Log",
                    "link": "https://onenr.io/0JBQrGyBNwZ"
                },
                {
                    "accountID": 1345223,
                    "city": "HRD",
                    "query": "SELECT uniqueCount(operatorID) as value FROM Log",
                    "link": "https://onenr.io/0JBQrGyBNwZ"
                }
            ],
            "value_type": "INT",
            "prefix": "",
            "suffix": ""
        }
    ]
```
