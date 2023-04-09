# Chapter -1 

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

