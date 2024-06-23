---
title: "How to Create an IP Checker Tool in Python"
date: 2024-03-07T11:28:03+07:00
slug: /information-gathring/
description: part of information gathring
image: images/recon3.jpg
caption: Photo by santricyber
categories:
  - hacking
tags:
  - recon
  - hacking
draft: false
---

At this stage of the ethical hacking series, I will share the source code for how to make the IP Checker tool using the Python programming language on our Kali Linux operating system. Making this tool also aims at Information Gathering to find the IP address of a website and the geolocation of the server where the target website is placed.


we simply create a file with the name we want with the file extension **[.py]** in this case I gave my file name **[checker.py]**  The contents of this file are as follows

`````````````````
import socket
import requests
import pprint
import json

hostname = input('Enter a domain name" ')
ip_address =  socket.gethostbyname(hostname)

request_url = '<https://geolocation-db.com/jsonp/>' + ip_address
response =  requests.get(request_url)
geolocation = response.content.decode()
geolocation = geolocation.split("(")[1].strip(")")
geolocation = json.loads(geolocation)
for k,v in geolocation.items():
	pprint.pprint(str(k) + ' : ' + str(v))
```````````````````````

after files checker.py is already filled with lines of code as above, then save and it's time to check whether the tools we have created can run properly.
what we need to do first we have to move to the directory where the checker.py is created, in this case, I put my files in the Documents directory
then we input this command in the 

**$ python terminal checker.py** then we enter the name of the target website and the results are as below.


``````````````
┌──(infosec㉿infosec)-[~/Documents]
└─$ python checker[.py](<http://geoloc.py/>)
Enter a domain name" [kominfo.go.id](<http://kominfo.go.id/>)
'country_code : US'
'country_name : United States'
'city : None'
'postal : None'
'latitude : 37.751'
'longitude : -97.822'
'IPv4 : 45.60.36.49'
'state : None'
``````````````


from the results above we can see some complete information such as IP address or geo-location. Until the discussion of this article is here, I will continue the discussion of information gathering in the next article