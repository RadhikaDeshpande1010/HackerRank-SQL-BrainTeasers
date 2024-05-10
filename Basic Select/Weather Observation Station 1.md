###
**[HackerRank SQL Query](https://www.hackerrank.com/challenges/weather-observation-station-1/problem?isFullScreen=true)**

Problem Statement: 

Query all columns (attributes) for every row in the CITY table.

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
SELECT CITY, STATE
FROM STATION;
```
