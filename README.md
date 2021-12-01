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
- `ls | tail -2`


### Env Variables
- how to check env variables `env` or `printenv key`
- DB_HOST=database
- we need to use `export key=value`
- making env var persistent
- how to make env var persistent in linux 

### Reverse Proxy with Nginx
- We have our node app listening on port 3000 and we would like it to be available on port 80 which is default port for browser 
- 

```
server {
    listen 80;

    server_name _;

    location / {
        proxy_pass http://localhost:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}

```


