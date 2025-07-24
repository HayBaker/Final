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
On line three I used the for loop: for n in {1..50}. The loop uses n as the variable and in the varable it as a culry brace extension with .. between 1 and 50 to indicate that it is the nombers 1 through 50. Then on line four we a do to let the for loop know we want it to do something. On line five we echo which means print the veriable n form the for loop like this: echo $n. This will print the numbers 1 through 50. One line six we have the code: sleep 0.001 which make each line of the code run for one millisecond then loop and do it again unilt it reaches 50. On the seventh line we have done to tell the script when it reaches 50 it is done and does not need to keep looping. On line eight I hev it echo "If ypu see this the programe worked and ran." after it is done looping and reaches 50 to let the user know it has worked. 

## Add to GitHub
I had to add the nano file to get hub by using this code:
```sh
git add Final.tx
```
Then to tell GitHub whatg it was I used the code:
```sh
git commit -m "Final that counts to 50"
```

Then I used the code: git status to see if it was added.
Next I had to push it to GitHub as it was not yet in GitHub by using the code:
```sh
git push origin master
```
The I could see it was on GitHub.

## Errors and Fixes
Was not autherized with the terminal and GitHub. I fixed it by using 
```sh
git config --global user.name "Your Name"
```
```sh
git config --global user.email "Your Emmail"
```
It did not want to update what I have done in nano to GitHub so I use these codes to fix it.
```sh
git config pull.rebase true
git reset --hard
HEAD is now at 3df27d0 Final that counts to 50
git pull origin master --rebase
```
Then it worked but, it did not make it exectable so I used this code:
```sh
chmod +x Final.txt
```
