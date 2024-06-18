# Database-assignment
1. I have chosen the Netflix Shows Dataset that intrested me.
2. I have noticed that the Data on some fields like the Director and Cast have missing values. And to ensure consistency, cleaning the fields can be challenging. 

3. A Data fun. Fact 1- The Most Popular Genre is Documentaries.
SELECT ListedIn, COUNT(*) AS GenreCount
FROM NetflixShows
GROUP BY ListedIn
ORDER BY GenreCount DESC
LIMIT 1;

B. Fact 2- The average release year of Netflix shows is approximately 2015.
SELECT AVG(ReleaseYear) AS AvgReleaseYear
FROM NetflixShows;

4 ASK AWAY questions
Q1: What are the top 5 countries producing Netflix shows?
SELECT Country, COUNT(*) AS ShowCount
FROM NetflixShows
GROUP BY Country
ORDER BY ShowCount DESC
LIMIT 5;
The top 5 countries producing Netflix shows are the United States, India, United Kingdom, Japan, and Canada.

Q2 How many shows were added in 2002?
SELECT COUNT(*) AS ShowsAdded
FROM NetflixShows
WHERE YEAR(DateAdded) = 2020;
A significant number of shows were added to Netflix in 2020, reflecting an increase in content production or acquisition.

