# SQL_Odev4
lcw bootcamp sql 4.ödev reposudur.

-- 1. Film Tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralama
SELECT DISTINCT replacement_cost
FROM film
ORDER BY replacement_cost;

-- 2. Film Tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?
SELECT COUNT(DISTINCT replacement_cost) AS distinct_count
FROM film;

-- 3. Film Tablosunda bulunan film isimlerinde (title) kaç tanesi 'T' karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?
SELECT COUNT(*) AS count
FROM film
WHERE title LIKE 'T%' 
  AND rating = 'G';

-- 4. Country Tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?
SELECT COUNT(*) AS count
FROM country
WHERE LENGTH(country) = 5;

-- 5. City Tablosundaki şehir isimlerinin kaç tanesi 'R' veya 'r' karakteri ile biter?
SELECT COUNT(*) AS count
FROM city
WHERE city LIKE '%R' OR city LIKE '%r';

