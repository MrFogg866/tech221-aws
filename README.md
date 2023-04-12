#### Steps to create SSH Key and Repo

## The 5 Steps to follow are 

1. Create a SSH Key Pair (local)
2. Register the padlock public key (GitHub)
3. Add private Key to the SSH Register (local)
4. Create test repository (GitHub)
5. Use SSH to test Repo (local)


## Step 1 (local)

* In bash check you are in the correct folder by typing LS
* Use LS .. to go back if nessecary 
* Once you are in the correct location type mkdir .ssh to create the .ssh folder
* (Pic1)
* Then type ssh-keygen -t rsa -b 4096 -C “your email address”
* (Pic2)
* Then type LS to confirm your keys have been created

## Step 2 (GitHub)

- We need to enter cat followed buy the key name in the terminal to show the .pub key 
- Next we need to go over to GitHub settings
- On the left click on “SSH & GPG keys”
- In “title” use the same name that your key is called
- “Key type” leave as “authentication type”
- Then copy and paste the .pub key into the box on GitHub starting from ssh-rsa and to the end of your email address only
- There click on “add SSH Key”
- (Pic3)

# Step 3 (local)

- Now back to bash we need to addd the private key to the SSH Register
- 1st enter eval `ssh-agent -s` and we should see a “agent pid” with a number
- (Pic4)
- Then we type ssh-add then the key name to add the private key
- (Pic5)
- Now test the connection using this command ssh -T git@github.com if you see this message below you know your key is working with GitHub
- (Pic6)

## Step 4 (GitHub)

- Next we create a repository on GitHub
- Click on the + symbol in the top right of GitHub and click “create repository”
- Enter a repository name and leave it public 
- Please select the SSH option next to the HTTPS option
- (Pic7)
- We can do this from the bash also
- First we use mkdir and the folder name for your repo
- Then we use cd to go into that folder
- Then we use touch README.md to create a markdown file

## Step 5 (local) 

- We will TEST  the SSH is working correctly
- First we use nano README.md to enter the bash editor
- Then we can add some text to update the readme
- (Pic8)
- For Mac we use CMD + S to save 
- Then CTRL X to return back to bash 