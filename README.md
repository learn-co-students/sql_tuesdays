From pgexercises.com

[Simple Join #1](https://pgexercises.com/questions/joins/simplejoin.html):

Retrieve the start times of members' bookings

Hints:  
Use aliases: SELECT t.name FROM example_table t  
You will use the `ON`, `WHERE` and `AND` keywords.  


==SOLUTION==  
SELECT b.starttime  
    FROM cd.bookings b  
    JOIN cd.members m  
ON b.memid = m.memid  
WHERE m.firstname = 'David'  
AND m.surname = 'Farrell'  


```python

```
