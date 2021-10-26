# MS17-010

Porting to python3 of the exploit and mysmb.py helper made by @sleepya.
Added a method to exploit SAMR named pipe. This, thanks to the connection with SYSTEM privileges due to EternalBlue bug, could lead to the creation, enumeration and modification of local SAM database.

Tested on Windows Server 2003

Credits to @sleepya (https://www.exploit-db.com/exploits/42315)
