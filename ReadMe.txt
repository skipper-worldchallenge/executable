						Takayuki.Uchida Japan
		Skipper 
---------------------------------------------------
+ please ask me(skipper.worldchallege@gmail.com) about Rpm.zip password.
+ Install (Linux centos7)
  rpm -ihv skipper-swg-0.99-R01.x86_64.rpm
      install to /usr/local/skipper/...
  systemctl start skipper | service skipper start.
    - log: /usr/local/skipper/log/
    - default
       proxy port : 0.0.0.0/8080
       do [ssl intercept] all web-request. 
+ You should get license-key from mail: skipper.worldchallege@gmail.com.
    you check GUI: Maintenance/Version and get [bliid /dev/sda1]
    if you dont do this, proxy stop 30min after starting.

--
Skipper is Valued-Secure Web Gateway and has specific any function below.

1) Supported HTTP/2 intercept(decode) and WebSocket, of couse HTTP/1, FTP.
2) To enbbed User Library is possible. 
3) Filterling
  - Now Skipper dont have URL-Filtering DB, But Skipper can filter WebRequest by ACL that Client set,
     Filter Target:
      URL/Host/HttpHeader/Query/SrcIp/Port/DstIp/Port/DstCountry/Protocol/…
  - Skipper can filter WebRequest by Snort Rules(outside direction only) and Reputation.
4) Multiple Authentiations(LDAP/NTLM/Private) 
5) Detailed Logging for SIEM.
6) Rich Setting GUI.
7) Multi-environment as Windows, Linux.

Now Skipper has any issue below.
- Skipper doesnt have URL-FilteringDB including Black/WhiteList and distribute such DB.

Possibility
- To enbbed User Library is possible. so that we can develop the Gateway Solution.



