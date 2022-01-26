# GDP labs pretest

## Adduser : corona
1. `sudo adduser corona` this command reffers to add new user called `corona`
    <p align="center">
        <img src=assets\adduser1.jpg />
    </p>

2. `sudo gpasswd -a corona sudo` this command will add user `corona` to sudo group and then user corona can access root. and to check it use `sudo groups corona`
    <p align="center">
        <img src=assets\adduser2.jpg />
    </p>

3. `su corona` login to user corona and fill the password with the same password we make before. and command `cd` to get access to directory `/home/corona`
    <p align="center">
        <img src=assets\adduser3.jpg />
    </p>


## Generate SSH
1. Inside user corona generate ssh by `ssh-keygen`. this command will generate directory .ssh and in the inside we will found file named `id_rsa.pub`. use command `cat id_rsa.pub` to see content and copy generated public ssh key
    <p align="center">
        <img src=assets\generatessh1.jpg />
    </p>
    <p align="center">
        <img src=assets\generatessh1.1.jpg />
    </p>

2. Login to linux server and make directory name .ssh`mkdir .ssh`. dot(.) in .ssh means the folder is hidden. And then command `chmod 700 .ssh` get user permission to read, write, and execute in directory `.ssh` 
3. `nano .ssh/authorized_keys` this command will generate file `authorized_keys` in directory .shh and paste the ssh key that copied before
    <p align="center">
        <img src=assets\generatessh2.jpg />
    </p>

4. and then restart ssh by command `sudo systemctl restart ssh`

## Access server using user corona
Login to user corona and type command 
```
ssh ubuntu@172.31.104.65
```
the format is `ssh <username>@serverIP`. This command is to login via ssh. and it will login to server with username corona
<p align="center">
    <img src=assets\accessuser.jpg />
</p>

as it is seen, it will login to server using user corona 
