						Takayuki.Uchida Japan

This system has three challenges . 
First, we don't have URL category database. this system can't be SWG without URL category database.
Next, we need testing and field verification. but we don't have enough resources.
Finally, this system has below funtions (1)-(9). but it's not enough as next generation gateway system. so I'm finding new function that bring new value.

So that I need collaborators to develop together and cordinators to deploy around the world as New value gateway.
Please contact me!


		Skipper 
---------------------------------------------------
+ environment to deverlop
  I'm using "Visual Studio Express 2013 for Windows Desktop" to deverlop.
  If you can collaborate, you need same environments.

+ please ask me(skipper.worldchallege@gmail.com) about zip password.
    [attention please!]  I will give you special password,    !skipper123#     Please try this! 

<For Linux> 
*) we need [openldap] pkg when installing this system!
1. Install (Linux centos7)
  rpm -ihv skipper-swg-0.99-R02.x86_64.rpm   (uninstall: rpm -e ...,  list: rpm -qa | grep skipper)
      install to /usr/local/skipper/...
  systemctl start skipper | service skipper start
    - log: /usr/local/skipper/log/
    - default
       proxy port : 0.0.0.0/8080
       do [ssl intercept] all web-request.
  or
1. Install (Linux Ubuntu server)
   dpkg -i skipper-swg_0.99.2_amd64.deb  (unilstall: dpkg --purge ...,  list: dpkg --list | grep skipper)
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
      [**New R02] As new filter condition, OwnIPPort and SourceCountry
  - Skipper can filter WebRequest by [Snort] Rules and Reputation.
     as forward-proxy: upstream-direction only(home_net->external_net),  as reverse-proxy: upstream-direction only(external_net->home_net)
  * When blocking, this system doesnot display blocking-page, only disconnecting.
4) Multiple Authentiations(LDAP/NTLM/Private) 
5) Detailed Logging for SIEM.
6) Cache for static contents.
7) Rich Setting GUI.
8) Multi-environment as Windows, Linux.
9) [**New R02] Preverse Proxy function!

Now Skipper has any issue below.
- Skipper doesnt have URL-FilteringDB including Black/WhiteList and distribute such DB.
  ***** please provide these or make these together with me!   ask me! *******

Possibility
- To enbbed User Library is possible. so that we can develop the Gateway Solution.
