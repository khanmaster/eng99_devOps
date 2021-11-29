# DevOps Intro
## Development Env

- Install vagrant
- Install Ruby


**Linux commands**
- `sudo apt-get update -y`
```
# creating a virtual machine with Linux Ubuntu 16.04
# ubuntu/xenial64

Vagrant.configure("2") do |config|

 # choose the os/box/distro
 config.vm.box = "ubuntu/xenial64"
 config.vm.network "private_network", ip: "192.168.10.100"  
# vagrant destroy
# vagrant up
# vagrant reload
end
```
- Who am I `uname -a`
- Where am I `pwd`
- list dir or all `ls` or `ls -a`
- copy file `cp filename destination`
- cut or rename `mv filename destination`
- create file `touch filename`
- create folder `mkdir foldername`
- how to navigate `cd foldername` retrun step back `cd ..`
- deleting file folders `rm -rf namefolder`

> Task: Create a folder called test, create a file called text.txt inside the test folder then copy the text.txt to your home location `/home/vagrant`

**File Permissions**
- Read `r`, Write `w` and `x`
- how to check permissions `ll`
- change permision `chmod permision filename`

- find out all processes running `top`
- how to `kill` a process 

### Automate everything we have done manually
- provision the steps of updating, upgrading and nginx installation
  
> vagrant up again
- redo all the steps 
- install nginx and load it in the browser 



