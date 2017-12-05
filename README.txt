Author:Pranati Shrivastava

Deliverables
------------

(1) Java program that can be run from command line: parser.jar
	

java -cp "parser.jar" com.ef.Parser --accesslog=/path/to/file --startDate=2017-01-01.13:00:00 --duration=hourly --threshold=100 


(2) Source Code for the Java program: parser.zip


(3) MySQL schema used for the log data: Logs.sql


(4) SQL queries for SQL test


1) Write MySQL query to find IPs that mode more than a certain number of requests for a given time period.

 Ex: Write SQL to find IPs that made more than 100 requests starting from 2017-01-01.13:00:00 to 2017-01-01.14:00:00.

NOTE: MY JAVA Program increased the hour and the day of the end date/timestamp.

SELECT IP FROM Logs 
WHERE Date BETWEEN '2017-01-01.13:00:00' AND '2017-01-01.14:00:00 
GROUP BY IP 
HAVING count(IP) >= 100;
   

(2) Write MySQL query to find requests made by a given IP.

SELECT IP, REQUEST FROM Logs 
WHERE IP='192.168.234.82';





