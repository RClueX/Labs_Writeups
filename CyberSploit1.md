# CyberSploit1

OffSec Machine - CyberSploit1

`192.168.60.92`

#### Step 1 : - 

First scan the given IP using nmap .

![2023-10-03 15_59_11-nmap](https://github.com/Jkrathod/CyberSploit1/assets/110445358/af181026-aa1f-45b3-8379-f327855a09e5)

I found two port are open

Port 22 — SSH

Port 80 — http


#### Step 2 :- 

Open the webpage source of the application

 ![username](https://github.com/Jkrathod/CyberSploit1/assets/110445358/36390439-f97f-477b-8c17-111b7f4dac67)

 Webapplication disclose the username in pagesource. `itsskv`
 
 
#### Step 3 :- 
 
I use Dirb for this 

![dirb](https://github.com/Jkrathod/CyberSploit1/assets/110445358/9b39202e-f71a-4651-99d1-da770a5392f2)

robots.txt is present in the web root

![view robots file](https://github.com/Jkrathod/CyberSploit1/assets/110445358/c0b781f4-1a80-4d02-b712-45f5fcf366b3)

It looks like base 64 encoded string. Decode the above string using online base 64 decoder.

![decode](https://github.com/Jkrathod/CyberSploit1/assets/110445358/e2f93653-66c8-405e-b4cf-abb9d16be309)


#### Step 4 :-

I try to make ssh connection using username and decoded string is the password so try to make SSH conection. 

![login ss](https://github.com/Jkrathod/CyberSploit1/assets/110445358/8c9724b9-99a5-41cd-a845-f8557a1e74f2)

Successfully authenticate as the user itsskv.


#### Step 5 :-

List the file using ls command.I have got local.txt file.

view the file using cat command.

![first flag](https://github.com/Jkrathod/CyberSploit1/assets/110445358/fe33907d-c7c5-46a8-84b0-25c6e911010f)


Zkkkasssss ............ I got successfuly flag.

