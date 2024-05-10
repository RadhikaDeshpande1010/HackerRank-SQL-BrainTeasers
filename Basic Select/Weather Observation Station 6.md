###
**[HackerRank SQL Query](https://www.hackerrank.com/challenges/weather-observation-station-6/problem?isFullScreen=true)**

Problem Statement: 

Query the list of CITY names starting with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates.

The STATION table is described as follows:

|  Field | Type |
|-------|-----|
| ID  | NUMBER |
| CITY | VARCHAR2(21)   |
| STATE  | VARCHAR2(2)  |
| LAT_N |  NUMBER |
| LONG_W | NUMBER |

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution**
```sql
SELECT DISTINCT 
CITY 
FROM STATION 
WHERE lower(substr(CITY,1,1)) in ('a','e','i','o','u') ;
```
