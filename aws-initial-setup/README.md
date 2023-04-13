## How to create EC2 server in AWS and Create and run a script


### The Steps to follow are: 


1. First login to AWS and select the Region Ireland.
2. Then type in EC2 into the Searcher bringing up the Dash board.
3. Select orange button “ Launch instance” without template unless you have a template. 
4. Create a name for the Instance using the name_class_subject.
5. Select “browse more AMI’S” and find the server UBUNTU 20.04 and hit select.
6. Then choose the “instance type” t2.micro. 
7. Then search for “key pair” “tech221”
8. In network settings we then want to create security group and also select “Allow HTTP traffic from the Internet” and select “MYIP” from the dropdown box next to “allow SSH traffic from, both boxes need to be selected as we are in the predevelopment stage.
9. After these are selected in the same area “Network setting” we can go to edit and rename the security group
10. Once this is done we click “launch instance”
11. Once the instance is launch go to the dash board and select instances (running)
12. Select your instance and go to connect in the top of the menu.
13. Then in bash goto the .ssh folder and type  - chmod 400 tech221.pem
14. Then copy the example and paste that into bash.
15. It may ask you to approve yes/no type yes then  should see ubuntu ip.
16. Once connected to ubuntu we can there install things.
17. Using `sudo apt install nginx`
18. once installed we can check in the browser by entering the ip address from aws

19. to run a script we need to create a shell file
20. `sudo nano provision.sh` 
21. then we enter the script to ebable a automated process as a follows 
22. 
```
#!/bin/bash

#update  
sudo apt update -y

#upgrade 
sudo apt upgrade -y

#install nginx - 
sudo apt install nginx -y

#restart nginx  
sudo systemctl restart nginx

#enable nginx 
sudo systemctl enable nginx
```
23. we then need to change the permissions by typing `sudo chmod =x provisions.sh` we can change the +x to r, w or wr depending on which permissions we want to grant, executable, read, write or read&write
24. to run the script we type `sudo ./provision.sh`
