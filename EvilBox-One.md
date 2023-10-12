## EvilBox-One 

`192.168.181.212`

### Step 1 :-

First Start enumeration of above given IP using nmap.

![nmap](https://github.com/Jkrathod/OffSec-Machines_Writeups/assets/110445358/8db5f781-3456-4248-bf80-c27ba9503519)

Found two port are open

### Step 2 :- 

Manually trying for a robots.txt page i find:

![robot](https://github.com/Jkrathod/OffSec-Machines_Writeups/assets/110445358/b9faf38c-6a8f-4b31-ab65-afcd249284ec)

### Step 3 

Fuzzing for directories using feroxbuster tool

![ferox 1](https://github.com/Jkrathod/OffSec-Machines_Writeups/assets/110445358/e4216b8a-1bdc-47c9-bdcd-e8b54edfb5c4)

Use the extention and fuzz the directory 

![php file](https://github.com/Jkrathod/OffSec-Machines_Writeups/assets/110445358/f935d1e2-e135-46de-8dd2-bcc89b05f7cc)


I found the evil.php file 

### Step 4: -

Automate fuzzing with ffuf:

![fuzz](https://github.com/Jkrathod/OffSec-Machines_Writeups/assets/110445358/294cf6b8-0a9d-45a0-a9a5-234d3a00f3d1)


### Step 5: -

I found that command allows the inclusion of local files of the target.


![open command url](https://github.com/Jkrathod/OffSec-Machines_Writeups/assets/110445358/1b6737a4-1172-4839-a1b3-a2ca8361db37)

### Step 6: -

 In have to search sensitive files and i got default directory of ssh private key default location - .ssh/id_r

 ![id rsa 1](https://github.com/Jkrathod/OffSec-Machines_Writeups/assets/110445358/150cb3f9-8c10-4572-ac81-ebd27776e519)

GIve the read write permission  - chmod 600 id_rsa


### Step 6:- 

Now connect using ssh - using username 

![1 REqUpz2PdjQVksBJ7nsDaw (2)](https://github.com/Jkrathod/OffSec-Machines_Writeups/assets/110445358/b4fe83ad-f33d-4305-a2d5-685b4d610b67)


Boom.....................

Flag are find........................ flag: 36QtXfdJWvdC0VavlPIApUbDlqTsBM

