# Http Authentication Module
This is Simple Http Authentication Module for ASP.NET (MVC).
- Basic Authentication
- Digest Authentication 
- Restrict IP Address (ip4 or ip6)

```xml:Web.config
<appSettings>
	<!-- HttpAuth -->
	<!--
	  Http Authentication Mode.
	  - Basic: Basic authentication
	  - Digest: Digest authentication
	  - None: No authentication -->
	<add key="HttpAuth" value="Digest" />
	<add key="HttpAuth.Realm" value="SecureZone" />
	<!-- user1:pass1;user2:pass2;... -->
	<add key="HttpAuth.Credentials" value="hoge:hogepass;foo:foopass;"/>
	<!--
	  if HttpAuth.RestrictIPAddresses is specified, restrict IP
	  e.g)
	    - 10.23.0.0/24
	    - 127.0.0.1 (equals to 127.0.0.1/32)
	    - 2001:0db8:bd05:01d2:288a:1fc0:0001:0000/16
	    - ::1 (equals to ::1/128)
	-->
	<add key="HttpAuth.RestrictIPAddresses" value="127.0.0.1;182.249.0.0/16;182.248.112.128/26;::1" />
</appSettings>
```
