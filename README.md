# Database-assignment
1. I have chosen the Netflix Shows Dataset that intrested me.
2.a I have noticed that the Data on some fields like the Director and Cast have missing values. And to ensure consistency, cleaning the fields can be challenging. 
The dateAdded field had dates in different formats, requiring normalisation.
c. Data Types:
TEXT vs. VARCHAR: Deciding between TEXT and VARCHAR for fields like Description and Cast based on their lengths and typical content.
Duration: Representing Duration in a way that allows meaningful analysis (e.g., as a numerical value rather than a string)

Interesting Observation
The dataset showcases a diverse range of genres and countries, highlighting Netflix's global reach and appeal. Analyzing the distribution of shows by country and genre can provide insights into content preferences across different regions.


3. A Data fun. Fact 1- The Most Popular Genre is Documentaries.
SELECT Listed_In, COUNT(*) AS GenreCount
FROM Netflix_titles
GROUP BY Listed_In
ORDER BY GenreCount DESC
LIMIT 1;

B. Fact 2- The average release year of Netflix shows is approximately 2015.
SELECT AVG(ReleaseYear) AS AvgReleaseYear
FROM NetflixShows;

4 ASK AWAY questions
Q1: What are the top 5 countries producing Netflix shows?
SELECT Country, COUNT(*) AS ShowCount
FROM Netflix_titles
GROUP BY Country
ORDER BY ShowCount DESC
LIMIT 5;
The top 5 countries producing Netflix shows are the United States, India, United Kingdom, Japan, and Canada.

Q2 How many shows were added in 2002?
SELECT COUNT(*) AS ShowsAdded
FROM Netflix_titles
WHERE YEAR(DateAdded) = 2020;
A significant number of shows were added to Netflix in 2020, reflecting an increase in content production or acquisition.

