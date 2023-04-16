## LINUX COMMANDS

1. `ls` - to show the files in current location
2. `ls-a` - to show all files including hidden files in current location
3. `whoami` - tells you what processor is being used
4. `pwd’ - shows the file path of the present working directory
5. `uname` - shows username
6. `name -a` - shows more info
7. `mkdir folder name` - makes a new folder/directory
8. `cd ..` - moves back a folder
9. `touch filename’ - makes a new file
10. `nano filename` - opens the file
11. `ctrlx` - to save any changes in that file 
12. `cat filename` - to check the file contents has saved
13. `cp filename folder name` - will copy and paste file to the folder
14. `rm filename` - will remove/delete the file 
15. `mv filename folder name` - will cut and paste file into folder
16. `ll` - tells you the permissions, read , write 
17. `chmod permission# file` - will change permission according to number used - can add `sudo` if access denied to become a superuser
18. `top` - shows all the running process similar to ctrl-alt-del
19. `ctrlz` - will exit `top`
20. `history` - shows all the commands used in that session
21. `-rf` - will force delete 
22. `ps -aux` - shows more specific information
23. `cat filename | grep test` to find a specific item in `ps -aux`
24. `kill pid#` - force quit
25. `sudo su` - to use as superuser - but careful there are no warnings 
26. `exit` - exit superuser 
27. `apt install xxx` - install things (may need to add sudo at start)
28. `sudo apt upgrade` - run any upgrades available
29. `sudo systemctl status` - check status
30. `sudo systemctl start xxxx` - start a server
31. `sudo systemctl stop xxxx` - stop server
32. `sudo systemctl  enable xxx` - enable
33. `sudo nano provision.sh` - create a shell file
34. `sudo chmod +x provision.sh` - change permissions
35. `Sudo ./provision.sh` - run the script

## Creating variables in Linux

36. `printenv` - Prints all the environmental variables

37. `env` - Shows all current variables and their values

38. `Printenv variable_name` - Prints the value of the variable

39. `echo $variable_name` - Prints the value of specified variable

40. `export VARIABLE=value` - creates a new environmental variable with a specified value

41. `source .bashrc` - refreshes the .bashrc to show any updated changes

In order to store variables in the environement so you can access it next time, you have to add them to the .bashrc script. The steps to do this are below:

- Open the script with a nano command which is nano .bashrc

- Scroll to the bottom and add your new code there. Make sure to not touch any of the codes already there

- Now type in export Variable=value - this is to create an environmental variable which will be added to this script

- Now use printenv Variable to see if there was a change. You'll see that it has not and that's because it needs to be refreshed

- Use source .bashrc - this will show the updated .bashrc with your new added variable
