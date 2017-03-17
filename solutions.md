--Create a new table called movies with an id, title and mediaTypeId.
--Make mediaTypeId a foreign key to the MediaType table on the MediaTypeId column.

CREATE TABLE movies (
  id INTEGER PRIMARY KEY AUTO_INCREMENT,
  title TEXT,
  mediaTypeId INTEGER,
  FOREIGN KEY(mediaTypeId) REFERENCES MediaType(MediaTypeId)
  );


  INSERT INTO movies (title, mediaTypeId)
  VALUES ('Point Break',

  insert into movies (title, mediaTypeId) values ("Aladdin", 3)

  ALTER TABLE movies ADD COLUMN genreId INTEGER REFERENCES Genre(GenreId);

  update movies set genreId=22 where id=1

  select Album.title, Artist.name
from Album
join Artist on Album.ArtistId = Artist.ArtistId

SELECT * FROM Track
WHERE GenreId in
(SELECT GenreId from Genre WHERE Name IN ('Jazz', 'Blues'))


SELECT * FROM Customer
WHERE Company IS NOT Null

SELECT Album.Title, Artist.Name, count(*)
FROM Album
JOIN Artist ON Artist.ArtistId = Album.ArtistId
GROUP BY Artist.Name
ORDER BY (count(*)) DESC

/*We have hundreds of customers
and want to know which countries our customers come from,
but no duplicates!*/

SELECT DISTINCT Country FROM Customer
