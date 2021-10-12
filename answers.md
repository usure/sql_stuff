## Answers
My answers to each SQLBolt question.

## Lesson 1: SELECT queries 101

### Question 1
Find the title of each film 
```sql
SELECT titleFROM movies;
```

### Question 2
Find the director of each film 
```sql
SELECT director FROM movies;
```

### Question 3
Find the title and director of each film 
```sql
SELECT title, director FROM movies;
```

### Question 4
Find the title and year of each film 
```sql
SELECT title, year FROM movies;
```

### Question 5
Find all the information about each film
```sql
SELECT * FROM movies;
```

## Lesson 2: Queries with constraints (Pt. 1)

### Question 1
Find the movie with a row id of 6
```sql
SELECT * FROM movies WHERE id = 6;
```

### Question 2
Find the movies released in the years between 2000 and 2010 
```sql
SELECT * FROM movies WHERE year between 2000 and 2010;
```

### Question 3
Find the movies not released in the years between 2000 and 2010
```sql
SELECT * FROM movies WHERE year NOT BETWEEN 2000 AND 2010;
```

### Question 4
Find the first 5 Pixar movies and their release year
```sql
SELECT * FROM movies WHERE id BETWEEN 1 AND 5;
```

## Lesson 3: Queries with constraints (Pt. 2)

### Question 1
Find all the Toy Story movies
```sql
SELECT * FROM movies WHERE title LIKE "%Toy Story%";
```

### Question 2
Find all the movies directed by John Lasseter
```sql
SELECT * FROM movies WHERE director = "John Lasseter";
```

### Question 3
Find all the movies (and director) not directed by John Lasseter 
```sql
SELECT * FROM movies WHERE director != "John Lasseter";
```

### Question 4
Find all the WALL-* movies
```sql
SELECT * FROM movies WHERE title LIKE "%Wall-%";
```

## Lesson 4: Filtering and sorting Query results

### Question 1
List all directors of Pixar movies (alphabetically), without duplicates 
```sql
SELECT DISTINCT director FROM movies ORDER BY director ASC;
```

### Question 2
List the last four Pixar movies released (ordered from most recent to least) 
```sql
SELECT * FROM movies ORDER BY year DESC LIMIT 4;
```

### Question 3
List the first five Pixar movies sorted alphabetically 
```sql
SELECT * FROM movies ORDER BY title ASC LIMIT 5;
```

### Question 4
List the next five Pixar movies sorted alphabetically 
```sql
SELECT * FROM movies ORDER BY title LIMIT 5 OFFSET 5;
```

## SQL Review: Simple SELECT Queries

### Question 1
List all the Canadian cities and their populations
```sql
SELECT City, Population FROM north_american_cities WHERE country = "Canada";
```

### Question 2
Order all the cities in the United States by their latitude from north to south
```sql
SELECT * FROM north_american_cities WHERE country = "United States" ORDER by Latitude DESC;
```

### Question 3
List all the cities west of Chicago, ordered from west to east
```sql
SELECT * FROM north_american_cities WHERE -87.629798 > Longitude ORDER BY Longitude ASC;
```

### Question 4
List the two largest cities in Mexico (by population) 
```sql
SELECT * FROM north_american_cities WHERE country = "Mexico" ORDER BY population DESC LIMIT 2;
```

### Question 5
List the third and fourth largest cities (by population) in the United States and their population
```sql
SELECT * FROM north_american_cities WHERE country = "United States" ORDER BY population DESC LIMIT 2 OFFSET 2;
```
