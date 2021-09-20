From pgexercises.com

[Simple Join #1](https://pgexercises.com/questions/joins/simplejoin.html):

Retrieve the start times of members' bookings

**Hints:**  
Use aliases: SELECT t.name FROM example_table t  
You will use the `ON`, `WHERE` and `AND` keywords.  


SELECT b.starttime  
    FROM cd.bookings b  
    JOIN cd.members m  
ON b.memid = m.memid  
WHERE m.firstname = 'David'  
AND m.surname = 'Farrell'  

[Simple Join #2](https://pgexercises.com/questions/joins/simplejoin.html): 

How can you produce a list of the start times for bookings for tennis courts, for the date '2012-09-21'? Return a list of start time and facility name pairings, ordered by the time.

**Hints**:  

Datetime objects ('2021-09-21') can be used with >/< logic  
Use the `LIKE` and `%` operators to match the strings

SELECT b.starttime AS start, f.name  
	from cd.bookings b  
	JOIN cd.facilities f  
	ON b.facid = f.facid  
WHERE b.starttime > '2012-09-21'  
AND b.starttime < '2012-09-22'  
AND f.name LIKE 'Tennis Court%'  
ORDER BY b.starttime  


```python

```
