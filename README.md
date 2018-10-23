# Week-8-Codepath
# Project 8 - Pentesting Live Targets

Time spent: 6 hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection

1. Added the basic logic in SQLI as ' OR 1=1 -- '

<img src="https://github.com/Manchukonda/Week-8-Codepath/blob/master/SQLInjection.gif" width="800">

Vulnerability #2: Session Hijacking / Fixation

1. Observed as the session id has changed when we login and logout in red and green websites.
2. In blue the session id is not changing when we login and logout. Session Id remains constant ,this leads to session hijacking.

<img src="https://github.com/Manchukonda/Week-8-Codepath/blob/master/SessionHiJacking.gif" width="800">


## Green

Vulnerability #1: Cross site scripting(XSS)

1. Added <script>alert("You have been Hacked");</script> in the comments section of the feedback. 
2. When we load the page, the popup arises with the message.

<img src="https://github.com/Manchukonda/Week-8-Codepath/blob/master/XSS.gif" width="800">


Vulnerability #2: User Enumeration

1. When we enter the login name which is existing in the database, the message shown in bold.
2. When we enter the login name which is not existing in the database, the message is not shown in bold.

<img src="https://github.com/Manchukonda/Week-8-Codepath/blob/master/UserEnumeration.gif" width="800">

## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)

1. When we change the id number in the url , the data will be retrived. We can observe the data changed in the website.

<img src="https://github.com/Manchukonda/Week-8-Codepath/blob/master/IDOR.gif" width="800">

Vulnerability #2: CSRF

1. If we inject the external file with the form code and the values . If we execute the html form the data is automatially inserted and   displayed in the sales persons list.

<img src="https://github.com/Manchukonda/Week-8-Codepath/blob/master/CSRF.gif" width="800">
