1.  Get everything:

SELECT
*

FROM
    movies.movies,



2.  Get only movie ID and title:

SELECT
    movieid, title
FROM
    movies.movies
LIMIT 10

3.  -Last Action Hero -Get movieID 485
SELECT
    movieid, title
FROM
    movies.movies
WHERE movieid = 485

4.  Get ID only (#489) for Made in America
SELECT
    movieid
FROM
    movies.movies
WHERE title = 'Made in America (1993)'

5.  Find the first 10 sorted alphabetically


SELECT
*

FROM
    movies.movies
   ORDER BY title ASC
   LIMIT 10 ;



6.   #Find all movies from 2002


SELECT *
FROM `movies`.`movies`
WHERE
title LIKE '%2002%'

7. #Find out what year the Godfather came out



SELECT *
FROM `movies`.`movies`
WHERE
title LIKE '%Godfather,%'  #putting in a comma gives only one not all


8. #Without using joins find all the comedies

SELECT *
FROM movies.genre
WHERE
genres LIKE '%comedy%';


9. #Find all comedies in the year 2000

SELECT *
FROM movies.movies
WHERE
genres LIKE '%comedy%'  AND title LIKE '%2000%'


10. #Find any movies that are about death and are a comedy

SELECT * FROM movies.movies
WHERE
genres LIKE '%comedy%'  AND title LIKE '%death%';

11. #Find any movies from either 2001 or 2002 with a title containing super

SELECT
    *
FROM
    movies.movies
WHERE
    title LIKE '%super%'
        AND title LIKE '%2001%'
        OR title LIKE '%super%'
        AND title LIKE '%2002%'
