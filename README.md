## This is the readme file for the final.
This code counts 1 through 50 and ends of with saying it it ran and worked.

## How to get it to work
Copy the code right into the terminal.
Then hit enter and it will run.

## Added ssh key
```sh
ssh-keygen -o
Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/hayden/.ssh/id_ed25519): 
/home/hayden/.ssh/id_ed25519 already exists.
Overwrite (y/n)? y
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/hayden/.ssh/id_ed25519
Your public key has been saved in /home/hayden/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:+W6LYqi6RTBqd6219YfQUnim1EiBOjQqHXYBqs3WWAc hayden@hayden-VirtualBox
The key's randomart image is:
+--[ED25519 256]--+
|   .E.. .o.      |
|  .o = .. +      |
|o.o * +  + =     |
|o* * +. ..*      |
|o.B....oS= .     |
|.o. . o o.+ .    |
|  .  o .  .o .   |
| .  . o  o. .    |
|oo.. . ...o.     |
+----[SHA256]-----+
```
```sh
cat /home/hayden/.ssh/id_ed25519.pub
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAID1ysVao8AHD/SdwyR1WW3qmmwmf8w6qh9WGQQNhTnO6 hayden@hayden-VirtualBox
```
Then copy the ssh key and past it in the ssh and gpg keys in account settings in GitHub.
Next make a file in nano. This is where you will write your bash script.
```sh
nano yourfilename.txt
```
## What code means
Line one I use a shbang #! and /bin/bash. This tells the nano editor waht scripting language we are using.
On line three I used the for loop: for n in { 

## Errors and Fixes
Was not autherized with the terminal and GitHub. I fixed it by using 
```sh
git config --global user.name "Your Name"
```
```sh
git config --global user.email "Your Emmail"
```
