# Project 9 - Pentesting Live Targets

Time spent: **X** hours spent in total

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

Vulnerability #1: __________________

Vulnerability #2: __________________


## Green

Vulnerability #1: User Enumeration
- Where: /staff/login.php
- Reveal: A valid Username
#### How:
1. Go to login page
2. Try a random username and look at the response text that gives an error message
3. Try a known username *pperson*
4. Look at the difference in how the error message is displayed

On green page, we will see that the error message is displayed in bold text when a known acceptable username is entered.

<img src="/gifs/user-enumeration.gif" alt="user-enumeration" />

Vulnerability #2: XSS
- Where: /public/contact.php
#### How:
1. Go to contact/feedback page
2. Fill out form with name and email
3. Insert html/script tag with an event listener which triggers an alert

As a staff member on green page wants to read through feedback, he/she is vulnerable to XSS attacks. The text area does not handle cross site scripts, which means that any scripts provided in the feedback can be run on the staff side of the website.

<img src="gifs/xss.gif" alt="xss" />


## Red

Vulnerability #1: __________________

Vulnerability #2: __________________


## Notes

Describe any challenges encountered while doing the work
