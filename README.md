# MS17-010

Porting to python3 of the exploit and mysmb.py helper made by @sleepya (https://www.exploit-db.com/exploits/42315).

## Improvements

Added a method to exploit SAMR named pipe. This, thanks to the connection with SYSTEM privileges due to EternalBlue bug, could lead to the creation, enumeration and modification of local SAM database.

## Tested environments

Windows Server 2003:
-full working

Windows 2000:
-hSamrChangePasswordUser not working on user without password. Is required to use an alternative method in order to set the first password (eg. RDP)
-hSamrRidToSid not present on Windows 2000, it reply with a op code error. You have to retrieve the domain SID manually (eg. from the output of hSamrGetMembersInAlias every account is listed with the relative SID, take the vale of the array concatenating them with a "-" and prepend to the result "S-1-5-")
