The World Wide Web in the early days consisted of only static websites containing information repositories. But today's modern world wide web is almos unrecognizable, majority of sites are considered web application instead

"This Site Is Secure"
The fact you see these when going to a site on you firefox or google chrom chrome browser doesn't mean the site is completely secure. Some of the vulnerabilities these sites are vulnerable to despite seeing this slogan could be

**Broken Authentication** -- These type of vulnerability has to do with the application weak login mechanism.

**Broken Access Control** -- When an application fails to properly protect access to it's data, it enables an attacker to view sensitive data not meant to be seen

**SQL Injection** -- These vulnerability enable an attacker to submit crafted input to enable him have interaction with the application backend database.

**Cross-site scripting** -- This enables an attacker to target other users of an application, performation unauthorized actions on their behalf.

**Information Leakage** -- This involves application leaking out information not meant to be seen enabling an attacker to develop an assault against the application.

**Core Security Problem:**
Users Can Submit Arbitrary Input and this problem can manifests in various ways

1. Users can interfere with any piece of data between the client and server e.g. HTTP headers and cookies.
2. Users are not restricted to using web browsers to access application. They're tools that can make request that no browser would ordinarily make and can generate huge numbers of requests that no browser would ordinarily make to find exploits.

Objectives of users submitting this arbitrary input could be to:

1. Changing the price of a product transmitted in a hidden HTML form field, to fraudulently purchase for cheaper amouont.
2. Modifying a session token transmitted in an HTTp cookie, to hijack authenticated user.
3. Altering some inut that will be processed by a back-end database, to inject a malicious databse query and access sensitive data.

It's important to note that SSL being active on a website doesn't not stop an attacker from submitting crafted input to the server, it simply 
means other users on the network cannot view or modify the attacker's data in transit because the attacker controls her end of the SSL tunnel.

Some of the key factors which explain the reason why many web app on the internet today have such poor web security includes.
-> Immature Security Awareness
-> In-House Development
-> Deceptive Simplicity
-> Rapidly Evolving Threat Profile
-> Resource and Time Contstraints
-> Overextended Technologies

**The New Security Perimeter**
Before web app, organizations mostly focused on the network perimeter of their internal network. Web app changed all this. For an application to function, the perimeter firewall must allow inbound connections to the server over HTTPS.
A significant part of the perimeter is now positioned on the organization's web applications.

