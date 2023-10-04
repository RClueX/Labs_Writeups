## EvilBox-One

`192.168.181.212`

### Step 1 :-

First Start enumeration of above given IP using nmap

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

