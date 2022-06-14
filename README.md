# Bug Bounty Checklist

### Forgot Password functionnality
* Username Enumeration
* Reset token key expiration time
* Check if password getting changed over SSL or not 
* Weak password policy testing
* Predict reset token 
* Check bruteforcing for security answer 
* All active user sessions should be destroyed when user change his password 

### Search functionnality 
* Scanner functionnality to test

### Product pruchase 
* Change product id to pruchase higher valued price at lower cost 
* Change value of gift vouchre to receive more gift vouchers instead of 1
* Add product to other user's cart 
* Tamper the cart id parameter for deleting other users product 
    * Testing case : Delete product from other user's cart 
* Place order behalf of other user 
* Give negative values in price to add money in your account + buying product 
* Check payment card gateway testing

### Booking mechanism 
* Check other user's e-ticket
* Get refund behalf of other user 
* Get more refunded by Changing refund amount
* Book business / high class ticket by changing parameter value of economy class variable 
* Book delux room by changing parameter value of normal room fare
* Book multiple seats / rooms by changing quantity parameter value for 1 seat / room book
* List application functionnalities and test it 
    * Multiple test cases based on application functionnality 
 
### Input Data Validation 
* XSS
    * Reflected 
    * Stored XSS
    * Cross Site flashing
* SQLi
    * Blind 
    * Boolean
    * Error 
* LDAP Injection
* XML Injectin
* Remote Code Injection
* XPATH Injection
* OS Command Injection
* X-Query Injection
* SSL Injection
* Code Injection
* Open Redirect
    * Find red, redirect, origin type of parameters and change their value to testinsane.com. Check for application bahavior for response
* Arbitrary File Download Vulnerability
    * RFI / LFI 
    * dotdotpwn.pl tool 
### Misc 
* Internal files leaked
* Internal IP disclosed 
* Clickjacking vulnerability
* ASP.Net viewstate encrypted or not
* Apache Multiview Attack
* Application doest not display Last login time and date 
* Weak Etag disclosed 
* Server side validation is not in place 
* Sensitive Information gets stored in History
* Oracle Padding attack ASPX 
* Downloadable objects 
    * Find metadata within object see if potential information is disclosed or not 
* Comment 
    * Cross Site scripting
    * Comment behalf of other users
* CAPTCHA Testing 
    * Identify parameters which are used to send CAPTCHA
    * Captcha Replay attack
    * Remove captcha parameter and send request to server 
    * Check whether the logic for generating CAPTCHAs is there in a .js file itself ? 
    * Captcha should not disclose absolute path
    * Remove captcha element with firebug and send it 
    * Check with free-ocr tool 
    * Insert captcha check response if captcha value is false changed to true and forward response.


### Automated testing 
* Netsparker 
* Burp Scan 

### Contact Us / Complaning / Feedback 
* Send message as other user (Applicable inside authentication)
* Captcha testing
* Captcha bypass
* Bruteforce

### Account functionnality 
* Check for CSRF 
* Check for CSRF token bypass
* Tamper user id to change other user's account information
* Impersonate other user's account
* Check account deletion functionnality 

### Error Codes 
* Test 404, 301 etc pages by /test.php, /test.aspx ...
* Use Input date -"&^%$#&!
* Send wrong cookie value to generate error 
* Change value to hidden parameter to generate error 
* Add "[]" in all parameters 
* Change get req to post adn post to get to generate error 
* Bypassing Web firewalls to generate error 
    * Javascript Ofuscation 
    * Alphanumeric Characters 
### Authentication Testing 
* Username enumeration
* Bypassing Authentication using SQL Injection
* Credential transmission over SSL or not ? 
* Account lockout 
* Check for OAuth functionality 
* User credentials are stored in browser memory in clear text 
* Back refresh Attack (Refer OWASP)

### Registration 

### Session Management
* Cookie
    * Sensitive info over cookie
    * Cookie with httpOnly flag 
    * Cookie with no secure flag 
    * Path attribute not set in session cookie
    * Apache HTTPOnly cookie disclosure (Specific to Apache)
* Session
    * Session prediction
    * Session randomness
    * Session expiration mechanisme legitimate ? 
    * Check if the Session ID is reissued for user critical actions
    * Check session cookie before and after login
    * Session Hijacking
    * Session token in URL? 
    * Session Hijacking
* Log out functionality 
    * Does session expires 
    * Session relay
    * After logout test check temp folder for cache and sensitive info stored 
* Strict Transporation Policy checking

### Application Entry Points 
* Login
* Search box  
* Comment Section
* Feedback Section
* Contact us section
* GET requests & Post requests 
* Cookies 
* Find out hidden post parameters and their usage 
* File Upload 
* Import things (contacts...)

### Web App Fingerprint 
* Default banner 
    * HEAD 
    * OPTION
    * GET 
* /robots.txt
* Check for admin interface 
    * Find using CMS identification
    * Fuzzing 
* Check for TRACE/TRACK method 
* Server fingerprint -  http://w3techs.com/sites/info/testinsane.com
* Auto Complete enabled or not ? 
* Which client side language is ued ? netcraft
* Debug Method Allow of IIS
* Info leak via stored cache
* Source code check (html)