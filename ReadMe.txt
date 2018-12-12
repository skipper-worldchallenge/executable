						Takayuki.Uchida Japan

Now I'm developping function of ReverseProxy in skipper(SWG), and I found serious Bugs at HTTP2 communication and Part of rules of snort are not working with pcre using ¥x00 format. I found bugs other else....
Rerverse Proxy function and Bug fix are almost there. Probably I will release it until this year.

At deploying 0.99-R02, I delete R01 because R01 has a lot of Bugs and I think I should not keep deploying it.
Thank you!

		Skipper 
---------------------------------------------------
+ please ask me(skipper.worldchallege@gmail.com) about zip password.
    [attention please!]  I will give you special password,    !skipper123#     Please try this! 

<For Linux> 
1. Install (Linux centos7)
  rpm -ihv skipper-swg-0.99-R01.x86_64.rpm   (uninstall: rpm -e ...,  list: rpm -qa | grep skipper)
      install to /usr/local/skipper/...
  systemctl start skipper | service skipper start
    - log: /usr/local/skipper/log/
    - default
       proxy port : 0.0.0.0/8080
       do [ssl intercept] all web-request.
  or
1. Install (Linux Ubuntu server)
   dpkg -i skipper-swg_0.99.1_amd64.deb  (unilstall: dpkg --purge ...,  list: dpkg --list | grep skipper)
      install to /usr/local/skipper/...
   service skipper start
2. You should get license-key from mail: skipper.worldchallege@gmail.com.
    you check GUI: Maintenance/Version and get [bliid /dev/sda1] and send get-value to mail.
      GUI: http://{install machine address}:9091   user[root] passwd[root]
    then I reply productId. you set this value.
    if you don't do this, proxy stop 30min after starting. but you can restart then you can use for 30min again.
    
<For Windows>    
1. Install WindowsServer2012R2 or more
      installer click only
      - install to service.  if you control skipper, you operate with [service].
      - install directory
           C:¥Program Files¥skipper1
     - default
       proxy port : 0.0.0.0/8080
       do [ssl intercept] all web-request.  
2. You should get license-key from mail: skipper.worldchallege@gmail.com.
   you check GUI: Maintenance/Version and get [ControlPanel - System - ProductID] and send get-value to mail.
       GUI: http://{install machine address}:9091    user[root] passwd[root]
   then I reply productId. you set this value.
   if you dont do this, proxy stop 30min after starting. but you can restart then you can use for 30min again.
   
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
