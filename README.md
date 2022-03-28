# MS17-010

Porting to python3 of the exploit and mysmb.py helper made by @sleepya (https://www.exploit-db.com/exploits/42315).

## Improvements

Added a method to exploit SAMR named pipe. This, thanks to the connection with SYSTEM privileges due to EternalBlue bug, could lead to the creation, enumeration and modification of local SAM database.

## Tested environments and open topic

Windows Server 2003:
* full working

Windows 2000:
* hSamrChangePasswordUser not working on user without password. Is required to use an alternative method in order to set the first password (eg. RDP)
