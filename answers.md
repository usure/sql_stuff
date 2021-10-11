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
