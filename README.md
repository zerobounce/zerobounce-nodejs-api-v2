[ZeroBounce](https://www.zerobounce.net) NodeJS API v2

This is a NodeJS wrapper class example for the ZeroBounce API v2.

##### Example usage:

```javascript
var https = require("https");
var api_key = "YOUR_API_KEY";
var email = "sampleemail@email.com";
var ip_address = "";

var options = {
    hostname: 'api.zerobounce.net',
    port: 443,
    path: "/v2/validate?api_key="+api_key+"&email="+email+"&ip_address='"+ip_address+"'",
    method: 'GET',
    secureProtocol: "TLSv1_2_method"
}

https.request(options, res => {
    let body = '';
    res.on('data', d => body += d)
    res.on('end', () => {
        var result = JSON.parse(body);
	// DO SOMETHING WITH result JSON

    })
}).on('error', err => {

    //DO SOMETHING FOR ERRORS
    return;

}).end()
```

**Any of the following email addresses can be used for testing the API, no credits are charged for these test email addresses:**
+ disposable@example.com
+ invalid@example.com
+ valid@example.com
+ toxic@example.com
+ donotmail@example.com
+ spamtrap@example.com
+ abuse@example.com
+ unknown@example.com
+ catch_all@example.com
+ antispam_system@example.com
+ does_not_accept_mail@example.com
+ exception_occurred@example.com
+ failed_smtp_connection@example.com
+ failed_syntax_check@example.com
+ forcible_disconnect@example.com
+ global_suppression@example.com
+ greylisted@example.com
+ leading_period_removed@example.com
+ mail_server_did_not_respond@example.com
+ mail_server_temporary_error@example.com
+ mailbox_quota_exceeded@example.com
+ mailbox_not_found@example.com
+ no_dns_entries@example.com
+ possible_trap@example.com
+ possible_typo@example.com
+ role_based@example.com
+ timeout_exceeded@example.com
+ unroutable_ip_address@example.com
+ free_email@example.com

**You can this IP to test the GEO Location in the API.**

+ 99.110.204.1

