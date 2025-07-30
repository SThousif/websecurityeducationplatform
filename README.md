Ethical Hacking Internship Project Report 
Intern Details 
• Name: Syed Thousif 
• Project Title: Web Application Vulnerability Assessment 
• Internship Domain: Ethical Hacking 
• Date: 30 July 2025 
Task 1: Solving XSS Labs on PortSwigger 
The following five XSS labs were selected and successfully completed from the 
PortSwigger Web Security Academy. Each lab demonstrates a unique form of cross-site 
scripting (XSS) vulnerability encountered in web applications. 
Labs Solved 
1. Reflected XSS into HTML context with nothing encoded 
2. Stored XSS into a blog comment 
3. Reflected XSS in canonical link tag 
4. DOM XSS in document.write sink 
5. Reflected XSS into JavaScript string with angle brackets HTML-encoded 
Each lab was solved successfully, and a "Solved" status was displayed.  
Task 2: Vulnerability Report on http://testasp.vulnweb.com/ 
1. Reflected XSS in Search Parameter 
• Summary: 
A reflected XSS vulnerability exists in the search.asp page. User input is rendered 
directly into the page response without proper sanitization or encoding. 
• URL: 
http://testasp.vulnweb.com/search.asp?query=<script>alert('XSS')</script> 
• Impact: 
This can allow attackers to execute arbitrary scripts, steal cookies, or redirect 
users to malicious pages. 
• Recommendation: 
Sanitize and encode all user input before rendering it on the page. Implement a 
Content Security Policy (CSP). 
•  
•  
2. SQL Injection in Login Page 
• Summary: 
The login page is vulnerable to SQL Injection, allowing attackers to bypass 
authentication. 
• URL: 
http://testasp.vulnweb.com/Login.asp 
• Payload Used: 
' OR '1'='1 
• Impact: 
Unauthorized access, data theft, or complete database compromise. 
• Recommendation: 
Use parameterized queries or stored procedures. Never concatenate user input 
in SQL statements. 
•  
•  
3. Insecure Cookies 
• Summary: 
Cookies are set without the Secure and HttpOnly flags, making them vulnerable 
to theft. 
• Observation: 
Using browser dev tools or Burp Suite, cookies can be intercepted and viewed in 
plain text. 
• Impact: 
Allows attackers to steal session cookies through XSS or man-in-the-middle 
attacks. 
• Recommendation: 
Always set the Secure, HttpOnly, and SameSite attributes on all session cookies. 
•  
 
 
