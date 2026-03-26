# dvwa-sql-injection--lab
SQL Injection and Blind SQL Injection lab using DVWA for cybersecurity practice

Disclaimer : This project was conducted in a controlled lab environment for educational purposes only.

Title:
SQL Injection & Blind SQL Injection Lab (DVWA)

Objective:
The objective of this project is to identify and exploit SQL Injection vulnerabilities using the Damn Vulnerable Web Application (DVWA).

Tools Used:
- Kali Linux
- DVWA
- Web Browser

SQL Injection (Basic)
Payload used: 
1' OR '1'='1
Result:
Successfully bypassed the query condition
Retrieved all user records from the database

Blind SQL Injection
Payloads used:
1' AND 1=1 --
1' AND 1=2 --
Result:
Able to differentiate TRUE and FALSE responses
Confirmed vulnerability using boolean-based SQL Injection

Database Enumeration (Blind)
Example:
1' AND database() = 'dvwa'#
Confirmed database name successfully

Impact
An attacker can:
Bypass authentication
Access sensitive data
Extract database information

Mitigation
To prevent SQL Injection:
Use prepared statements (parameterized queries)
Implement input validation
Avoid directly inserting user input into SQL queries
