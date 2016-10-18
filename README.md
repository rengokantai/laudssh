# laudssh
##2. Connect Securely with a Key
###2 Generating a key pair on Mac OS X or Linux
```
ssh-keygen -t rsa
```
####01:53 copy to remote server
```
ssh-copy-id user@ip
```
###3 Connecting to an SSH server from Mac OS X and Linux using a key
```
ssh -i .ssh/id_rsa user@ip
```
create a config profile  
.ssh/config
```
Host ke
    User username
    HostName ip
    IdentityFile ~/.ssh/id_rsa
```
connect
```
ssh ke
```

###4 Generating a key pair on Windows
puttygen.  
private key = mykey.ppk  
public ley = mykey

##3. Other Uses of SSH
###1 Transferring files with SSH File Transfer Protocol (SFTP)
```
sftp
lls
lcd
put file.txt
```
###3 Creating an SSH tunnel
local port forwarding (port local port 9000 to remote port 3306)
```
ssh -L 9000:localhost:3306 user@ip
```
####01:40
then when connect to database, use host: localhost port:9000  

####02:10
quit session
```
exit
```
another way to use forwarding
```
ssh -L 9000:localhost:3306 user@ip -N
```
when dont want this session,
```
ctrl c
```
  
