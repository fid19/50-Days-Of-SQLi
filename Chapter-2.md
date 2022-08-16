A golden rule accept input from users on a web application is to regard all of it as untrusted. This does not mean all the time user is malicious, but they're certain strings of characters that might be inputed and cause a total breakdown of our web app.

A number of security features can be implemented in order to prevent this from happening. These could include;

-> Handling user input to the application's function, to prevent malformed input from causing undesirable behaviour

->Managing the application itself, by enabling administrators to monitor its activities and configure it's functionality

Even if you're new to the hacking world, taking time to study your enemy and knowing his weak points could leave them vulnerable to attack.

**Handling User Access**
They're different categories of users, these include anonymous, administrative, ordinary authenticated users e.t.c. A web app needs to control users' access to it's data and functionality and this is performed through the following security mechanism

**-> Authentication**
The authentication model is the most basic level of trust to ensure a user is really who he said he is. Common attacks that can be performed at this stage is bruteforcing of username and pass or bypassing the login function all together by exploiting a defect.

-> Session Management
After authentication, the application creates a session and issues a token to each user as a means of managing a user state. This session token is automatically submitted by the browser enabling the application to know if it's logged in.

-> Access Control
At this stage, we decide wether to deny or permit a request by a user. If the previous mechanisms are working,the application knows the identity of each user from the requests it'll receive.

A defect in any one of these security mechanism could enable an attacker to gain unrestricted access to the application's functionality and data.

**Approaches to Input Handling**

**Reject Known Bad**
This typically involves making a blacklist containing a set of literal strings or patterns that are known to be used in attacks.

**Accept Known Good**
This approach employs a white list containing a set of literal strings or patterns and allows data that matches the whitelist and blocks everything else.

**Sanitization**
Instead of rejecting input with known bad, the application sanitizes the input in various ways to prevent it from having any adverse effects

**Boundary Validation**
Here, each individual component or functional unit of the server side application performs data validation according to the type of attack they're vulnerable to.
An example is a user login in to the database, a form validation is performed to check if user has inputted the correct data and is passed to the application which sanitizes the data for sql injection before performing sql queries, as it returning it's response to the user, the application check data for cross site scripting attack before finally giving it's response to the user. 

Others include Safe Data Handling, Semantic Checks

**Issue With Multi-Step Validation and  Canonicalization**

An application may attempt to defend against some cross site scripting attacks by stripping the expression

<script>

However an attacker maybe able to bypass the filter if a rescursive mechanism is not put in place

<scr<script>ipt>

When the blocked expression is removed, the surrounding data contracts to restore the malicious ppayload.
If more than one validation step is performed on user input, an attacker maybe able to exploit the ordering of these steps to bypass the filter.

Another issue arises which has to do with data canonicalization. Canonicalization is the process of converting or decoding data into a common character set. An attacker maybe able to use encoding to bypass the validation mechanism.

It maybe preferable to avoid attempting to clean some kinds of bad input, and simply reject it all together


**Handling Attackers**

Measures implemented to handle attackers typically include

-> Handling errors
In a production context, the should never return any system generated message to the user as a result of an error. This messages can greatly assist the malicious attacker in furthering their attacks against the application.

-> Maintaining audit logs
-> Alerting administrators
-> Reacting to attacks
