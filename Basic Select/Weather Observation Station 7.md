###
**[HackerRank SQL Query](https://www.hackerrank.com/challenges/weather-observation-station-7/problem?isFullScreen=true)**

Problem Statement: 

Query the list of CITY names ending with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates.

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
SELECT COUNT(CITY) - COUNT(DISTINCT CITY)
FROM STATION;
```
