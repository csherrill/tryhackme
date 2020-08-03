# IP =  10.10.210.115


# Task 1 
```
Scan the machine. (If you are unsure how to tackle this, I recommend checking out the room RP: Nmap)
```
1. No answer needed


```
How many ports are open with a port number under 1000?
```
1. 3


```
What is this machine vulnerable to? (Answer in the form of: ms??-???, ex: ms08-067)
```
1. ms17-010


# Task 2  

```
Start Metasploit
```
1. No answer needed


```
Find the exploitation code we will run against the machine. What is the full path of the code? (Ex: exploit/........)
```
1. exploit/windows/smb/ms17_010_eternalblue


```
Show options and set the one required value. What is the name of this value? (All caps for submission)
```
1. RHOSTS


```
Run the exploit!
```
1. No answer needed


```
Confirm that the exploit has run correctly. You may have to press enter for the DOS shell to appear. Background this shell (CTRL + Z). If this failed, you may have to reboot the target VM. Try running it again before a reboot of the target. 
```
1. No answer needed




# Task 3

```
If you haven't already, background the previously gained shell (CTRL + Z). Research online how to convert a shell to meterpreter shell in metasploit. What is the name of the post module we will use? (Exact path, similar to the exploit we previously selected) 
```
1. post/multi/manage/shell_to_meterpreter


```
Select this (use MODULE_PATH). Show options, what option are we required to change? (All caps for answer)
```
1. SESSION


```
Set the required option, you may need to list all of the sessions to find your target here. 
```
1. No answer needed


```
Run! If this doesn't work, try completing the exploit from the previous task once more.
```
1. No answer needed


```
Once the meterpreter shell conversion completes, select that session for use.
```
1. No answer needed


```
Verify that we have escalated to NT AUTHORITY\SYSTEM. Run getsystem to confirm this. Feel free to open a dos shell via the command 'shell' and run 'whoami'. This should return that we are indeed system. Background this shell afterwards and select our meterpreter session for usage again. 
```
1. No answer needed


```
List all of the processes running via the 'ps' command. Just because we are system doesn't mean our process is. Find a process towards the bottom of this list that is running at NT AUTHORITY\SYSTEM and write down the process id (far left column).
```
1. No answer needed


```
Migrate to this process using the 'migrate PROCESS_ID' command where the process id is the one you just wrote down in the previous step. This may take several attempts, migrating processes is not very stable. If this fails, you may need to re-run the conversion process or reboot the machine and start once again. If this happens, try a different process next time. 
```
1. No answer needed



# Task 4

```
Within our elevated meterpreter shell, run the command 'hashdump'. This will dump all of the passwords on the machine as long as we have the correct privileges to do so. What is the name of the non-default user? 
```
1. Jon


```
Copy this password hash to a file and research how to crack it. What is the cracked password?
```
1. alqfna22


# Task 5 FLAGS

1. flag{access_the_machine}

2. flag{sam_database_elevated_access}

3. flag{admin_documents_can_be_valuable}