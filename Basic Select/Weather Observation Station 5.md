###
**[HackerRank SQL Query](https://www.hackerrank.com/challenges/weather-observation-station-5/problem?isFullScreen=true)**

Problem Statement: 

Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.

The STATION table is described as follows:

|  Field | Type |
|-------|-----|
| ID  | NUMBER |
| CITY | VARCHAR2(21)   |
| STATE  | VARCHAR2(2)  |
| LAT_N |  NUMBER |
| LONG_W | NUMBER |

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Sample Input**

For example, CITY has four entries: DEF, ABC, PQRS and WXY.

**Sample Output**

```SQL
ABC 3
PQRS 4
```

**Explanation**

When ordered alphabetically, the CITY names are listed as ABC, DEF, PQRS, and WXY, with lengths  and . The longest name is PQRS, but there are  options for shortest named city. Choose ABC, because it comes first alphabetically.

Note
You can write two separate queries to get the desired output. It need not be a single query.

For example, if there are three records in the table with CITY values 'New York', 'New York', 'Bengalaru', there are 2 different city names: 'New York' and 'Bengalaru'. The query returns , because because total number of records - number of unique city namess = 3 - 2 = 1.

**Solution**
```sql
SELECT * FROM (SELECT DISTINCT city, LENGTH(city) FROM station ORDER BY LENGTH(city) ASC, city ASC) WHERE ROWNUM = 1   
UNION  
SELECT * FROM (SELECT DISTINCT city, LENGTH(city) FROM station ORDER BY LENGTH(city) DESC, city ASC) WHERE ROWNUM = 1;  
```
