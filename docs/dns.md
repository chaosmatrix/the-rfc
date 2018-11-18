# DNS RFC

## https://tools.ietf.org/pdf/rfc3655.pdf
```
The presence of the CD (Checking Disabled) bit in a query does not
   affect the setting of the AD bit in the response.  If the CD bit is
   set, the server will not perform checking, but SHOULD still set the
   AD bit if the data has already been cryptographically verified or
   complies with local policy.  The AD bit MUST only be set if DNSSEC
   records have been requested via the DO bit [RFC3225] and relevant SIG
   records are returned.


   Note that having the AD bit clear on an authoritative answer is
   normal and expected behavior.
```
1. clear AD bit in response is more compatiible
2. "data has been cryptographically verified"
    * means "dnssec"
	* data from "authoritative server" to "client" are cryptographically verified
	* "recursive server" to "client" via https not in count, "authoritative server" to "recursive server" may not safe
