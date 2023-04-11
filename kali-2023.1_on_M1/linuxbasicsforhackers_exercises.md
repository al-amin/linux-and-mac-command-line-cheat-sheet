Book from : [this link](https://kea.nu/files/textbooks/humblesec/linuxbasicsforhackers.pdf)

=======================================================================================================
# Chapter -1 
=======================================================================================================

### 1. Use the ls command from the root (/) directory to explore the directory structure of Linux. Move to each of the directories with the cd command and run pwd to verify where you are in the directory structure.

#### Answer: ```cd /``` , ```pwd``` , ```ls``` 


### 2. Use the whoami command to verify which user you are logged in as.
#### Answer: ```whoami```

### 3. Use the locate command to find wordlists that can be used for password cracking.
#### Answer: ```locate wordlists```

### 4. Use the cat command to create a new file and then append to that file. Keep in mind that > redirects input to a file and >> appends to a file.
#### Answer: ```cat > new_file.txt``` , Then write the followings by: ```This is a file. created by cat command.```. Now Calt + C to save the file.
Now to append the input to new_file.txt by: ```cat >> new_file.txt``` Then write the followings by: ```This line was appended by cat >> command. This is awesome.``` Now Calt + C to save the file. To check if it saved or not by: ```cat new_file.txt```


### 5. Create a new directory called hackerdirectory and create a new file in that directory named hackedfile. Now copy that file to your /root directory and rename it secretfile.

#### Answer: 
Cd to a Desktop by: ```cd /home/USER_XXXX/Desktop```\
Create a directory called hackerdirectory by:```mkdir hackerdirectory``` \
change directory by ```cd hackerdirectory``` ,Create a new file called hackedfile by: ```touch hackedfile``` \
Now cp that file to /root directory by: ```sudo cp hackedfile /```
To check ```cd /```, then ls ```ls```

## Install snort on [kali linux](https://dev.to/ankitsahu/install-snort-on-kali-1co8) - does not work, later installed ubuntu ;)

=======================================================================================================
# Chapter -2
=======================================================================================================
### 1. Navigate to /usr/share/metasploit-framework/data/wordlists. This is a directory of multiple wordlists that can be used to brute force passwords in various password-protected devices using Metasploit, the most popular pentesting and hacking framework.
#### Answer: ```lcd /usr/share/metasploit-framework/data/wordlists```
### 2. Use the cat command to view the contents of the file password.lst.
#### Answer: ```cat password.lst```
### 3. Use the more command to display the file password.lst.
#### Answer: ```more password.lst```
### 4. Use the less command to view the file password.lst.
#### Answer: ```less password.lst```
### 5. Now use the nl command to place line numbers on the passwords in password.lst. There should be around 88,396 passwords.
#### Answer: ```nl password.lst```
### 6. Use the tail command to see the last 20 passwords in password.lst.
#### Answer: ```tail -20 password.lst```
### 7. Use the cat command to display password.lst and pipe it to find all the passwords that contain 123.
#### Answer: ```cat password.lst | grep 123```
