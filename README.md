## gid-curate-concept

A data component to curate concept

    <gid-curate-concept concept='1' user='1' entity = "CURATE-CONCEPT" 	curateconcept='{{curateconcept}}'></<gid-curate-concept>
    
The properties 'concept', 'user' and 'entity' are mandatory.

API endpoint:

    PUT /concepts/{id}/curate

Input:

- User Id (Query Param)

- Concept Id (URL Param)

- ~~List of recommended applications to start with~~

- Trigger that user has switched from define to explore

- Explicit yes or no on most of the synonyms, patterns and related concepts

- Explicit yes or no on most of the example columns and some of the example values

- ~~Search string for synonyms, patterns or related concepts~~

Sample Input: (as JSON payload)

	    {
	        "synonyms":[
	            {"id":"100052","verified":"Y"},
	            {"id":"100051","verified":"Y"},
	        ],
	        "patterns":[
	            {"id":"100152","verified":"Y"},
	            {"id":"100151","verified":"Y"},
	        ],
	        "relatedConcepts":[
	            {"id":"100052","verified":"Y"},
	            {"id":"100051","verified":"Y"},
	        ],
	        "exampleValues":[
	            {"id":"100052","verified":"Y"},
	            {"id":"100051","verified":"Y"},
	        ],
	        "exampleColumns":[
	            {"id":"100052","verified":"Y"},
	            {"id":"100051","verified":"Y"},
	        ],
	    }
	
Output:
	- ~~5 synonyms (with likelihood)~~
	- ~~5 patterns (with likelihood)~~
	- ~~5 related concepts (with likelihood)~~
	
	- list of 10 example columns and 100 example values (prioritised by relevance)
	
	- output 2 + revised list of synonyms, patterns and related concepts 
		
	- ~~search results~~
		
		{
	    "synonyms": [
	        {
	            "id": "700129",
	            "label": "product_desc",
	            "verified": "Y",
	            "relevance": 20
	        },
	        {
	            "id": "700132",
	            "label": "cust_name",
	            "verified": "N",
	            "relevance": 27
	        },
	        {
	            "id": "700136",
	            "label": "cust_id",
	            "verified": "N",
	            "relevance": 55.00000000000001
	        },
	        {
	            "id": "700125",
	            "label": "user_name",
	            "verified": "N",
	            "relevance": 11
	        },
	        {
	            "id": "700131",
	            "label": "f_name",
	            "verified": "N",
	            "relevance": 11
	        },
	        {
	            "id": "700128",
	            "label": "product_cd",
	            "verified": "N",
	            "relevance": 40
	        },
	        {
	            "id": "700127",
	            "label": "last_name",
	            "verified": "N",
	            "relevance": 20
	        },
	        {
	            "id": "700134",
	            "label": "first_name",
	            "verified": "N",
	            "relevance": 22
	        },
	        {
	            "id": "700133",
	            "label": "customer_name",
	            "verified": "N",
	            "relevance": 11
	        },
	        {
	            "id": "700126",
	            "label": "l_name",
	            "verified": "N",
	            "relevance": 11
	        },
	        {
	            "id": "700124",
	            "label": "product",
	            "verified": "N",
	            "relevance": 40
	        },
	        {
	            "id": "700135",
	            "label": "cust_phone",
	            "verified": "N",
	            "relevance": 9
	        },
	        {
	            "id": "700130",
	            "label": "cust_fname",
	            "verified": "N",
	            "relevance": 9
	        }
	    ],
	    "patterns": [
	        {
	            "id": "600408",
	            "label": "Zzzzzzz",
	            "verified": "N",
	            "count": 23
	        },
	        {
	            "id": "600405",
	            "label": "Zzzzz",
	            "verified": "N",
	            "count": 14
	        },
	        {
	            "id": "600401",
	            "label": "Zzzzzz",
	            "verified": "N",
	            "count": 11
	        },
	        {
	            "id": "600406",
	            "label": "Zzzzzzzz-Zzzzzz",
	            "verified": "N",
	            "count": 1
	        },
	        {
	            "id": "600399",
	            "label": "Zzzzzzzz",
	            "verified": "N",
	            "count": 25
	        },
	        {
	            "id": "600407",
	            "label": "Zzzz",
	            "verified": "N",
	            "count": 8
	        },
	        {
	            "id": "600403",
	            "label": "Zzzzzzzzzzzz",
	            "verified": "N",
	            "count": 1
	        },
	        {
	            "id": "600409",
	            "label": "Zzz",
	            "verified": "N",
	            "count": 1
	        },
	        {
	            "id": "600404",
	            "label": "Zzzzzzzzzz",
	            "verified": "N",
	            "count": 3
	        },
	        {
	            "id": "600400",
	            "label": "Zzzzzzzzzzz",
	            "verified": "N",
	            "count": 1
	        },
	        {
	            "id": "600402",
	            "label": "ZzZzzzzzz",
	            "verified": "N",
	            "count": 1
	        },
	        {
	            "id": "600410",
	            "label": "Zzzzzzzzz",
	            "verified": "N",
	            "count": 13
	        }
	    ],
	    "relatedConcepts": [
	        {
	            "id": "100376",
	            "label": "Email-Address",
	            "verified": "N",
	            "relevance": 18
	        },
	        {
	            "id": "100358",
	            "label": "Birth-Date",
	            "verified": "N",
	            "relevance": 16
	        },
	        {
	            "id": "100352",
	            "label": "Address",
	            "verified": "N",
	            "relevance": 12
	        },
	        {
	            "id": "100386",
	            "label": "First-Name",
	            "verified": "N",
	            "relevance": 18
	        },
	        {
	            "id": "100033",
	            "label": "City",
	            "verified": "N",
	            "relevance": 2
	        },
	        {
	            "id": "100387",
	            "label": "Gender",
	            "verified": "N",
	            "relevance": 17
	        },
	        {
	            "id": "100501",
	            "label": "person-id",
	            "verified": "N",
	            "relevance": 17
	        }
	    ],
	    "exampleValues": [
	        {
	            "id": "3642043d",
	            "label": "Breckell",
	            "verified": "N"
	        },
	        {
	            "id": "ace70260",
	            "label": "Pallister",
	            "verified": "N"
	        },
	        {
	            "id": "0a0bdcae",
	            "label": "Cleere",
	            "verified": "N"
	        },
	        {
	            "id": "9430c213",
	            "label": "Ruppertz",
	            "verified": "N"
	        },
	        {
	            "id": "40653d98",
	            "label": "Newcomen",
	            "verified": "N"
	        },
	        {
	            "id": "3ecdaab9",
	            "label": "Mulvenna",
	            "verified": "N"
	        },
	        {
	            "id": "afacd702",
	            "label": "Crutchley",
	            "verified": "N"
	        },
	        {
	            "id": "9ed6b924",
	            "label": "Smidmore",
	            "verified": "N"
	        },
	        {
	            "id": "46f1198c",
	            "label": "Baynes",
	            "verified": "N"
	        },
	        {
	            "id": "68144aa9",
	            "label": "Sterzaker",
	            "verified": "N"
	        },
	        {
	            "id": "03d4b129",
	            "label": "Echallier",
	            "verified": "N"
	        },
	        {
	            "id": "e0a61327",
	            "label": "Corps",
	            "verified": "N"
	        },
	        {
	            "id": "f21512c4",
	            "label": "Orrom",
	            "verified": "N"
	        },
	        {
	            "id": "427b01d1",
	            "label": "Sylvester",
	            "verified": "N"
	        },
	        {
	            "id": "e9a03cbc",
	            "label": "Vidineev",
	            "verified": "N"
	        },
	        {
	            "id": "5450481e",
	            "label": "Ellinor",
	            "verified": "N"
	        },
	        {
	            "id": "fc56d55e",
	            "label": "Karpman",
	            "verified": "N"
	        },
	        {
	            "id": "ad0e463b",
	            "label": "Berzons",
	            "verified": "N"
	        },
	        {
	            "id": "94aceefd",
	            "label": "Danshin",
	            "verified": "N"
	        },
	        {
	            "id": "2b24a83f",
	            "label": "Christensen",
	            "verified": "N"
	        },
	        {
	            "id": "845ce769",
	            "label": "McKinstry",
	            "verified": "N"
	        },
	        {
	            "id": "12d7588c",
	            "label": "Knibb",
	            "verified": "N"
	        },
	        {
	            "id": "16a47b3e",
	            "label": "Bassindale",
	            "verified": "N"
	        },
	        {
	            "id": "b6aed81a",
	            "label": "Donaher",
	            "verified": "N"
	        },
	        {
	            "id": "4cba59ba",
	            "label": "Conti",
	            "verified": "N"
	        },
	        {
	            "id": "edf4c548",
	            "label": "Gentzsch",
	            "verified": "N"
	        },
	        {
	            "id": "a8243e82",
	            "label": "Geldeard",
	            "verified": "N"
	        },
	        {
	            "id": "ec9f7c38",
	            "label": "Somerlie",
	            "verified": "N"
	        },
	        {
	            "id": "c360f7ef",
	            "label": "Flea",
	            "verified": "N"
	        },
	        {
	            "id": "f20df0f3",
	            "label": "Dilland",
	            "verified": "N"
	        }
	    ],
	    "exampleColumns": [
	        {
	            "id": "200029",
	            "label": "ship_city",
	            "verified": "Y",
	            "relevance": 95
	        },
	        {
	            "id": "200003",
	            "label": "product_code",
	            "verified": "Y",
	            "relevance": 95
	        },
	        {
	            "id": "200013",
	            "label": "last_name",
	            "verified": "N",
	            "relevance": 1
	        },
	        {
	            "id": "200053",
	            "label": "X9813_AVOCADO",
	            "verified": "N",
	            "relevance": 95
	        },
	        {
	            "id": "200013",
	            "label": "last_name",
	            "verified": "Y",
	            "relevance": 95
	        },
	        {
	            "id": "e2c8f630-4a37-38d7-9359-1d1be8375fcd",
	            "label": "l_name",
	            "verified": "N",
	            "relevance": 1
	        },
	        {
	            "id": "28389982-3cdc-30d6-bc3f-cec02ae547ff",
	            "label": "last_name",
	            "verified": "N",
	            "relevance": 1
	        },
	        {
	            "id": "200033",
	            "label": "PRODUCT",
	            "verified": "N",
	            "relevance": 95
	        },
	        {
	            "id": "200076",
	            "label": "UNIQUE_GROUP",
	            "verified": "N",
	            "relevance": 95
	        },
	        {
	            "id": "8eefd496-038d-3485-9b32-3eece55d3569",
	            "label": "last_name",
	            "verified": "N",
	            "relevance": 1
	        },
	        {
	            "id": "4ed34e05-5aa8-3e24-b17f-b57305156ad9",
	            "label": "cust_lname",
	            "verified": "N",
	            "relevance": 1
	        },
	        {
	            "id": "200043",
	            "label": "SEC_CITY",
	            "verified": "N",
	            "relevance": 95
	        },
	        {
	            "id": "200063",
	            "label": "SEC_CITY",
	            "verified": "N",
	            "relevance": 95
	        },
	        {
	            "id": "4ed34e05-5aa8-3e24-b17f-b57305156ad9",
	            "label": "cust_lname",
	            "verified": "N",
	            "relevance": 1
	        },
	        {
	            "id": "200021",
	            "label": "first_nm",
	            "verified": "N",
	            "relevance": 95
	        }
	    ]
	}
