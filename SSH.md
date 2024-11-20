# SSH
ssh (secure shell) it is a network protocol allows users to  establish connection between remote servers and user's computer so that he can perform operations on it over an encrypted connection.\
SSH includes\
* Private key
* Public key
* SSH Agent

## Public Key
it is an encrypted key which is stored in server and it can be shared openly

## Private Key
it has the decription algorithm of public key so that it can access the server and it is stored in local machine and it should not be shared

## SSH Agent
it is used to store the private keys in a memory so that while connecting to a server it will manage the private keys and establish connection between local and server machine\
command to activate ssh agent is `eval "$(ssh-agent -s)"`\
to add private keys to ssh agent the command is `ssh-add "private key path"`
