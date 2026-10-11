# Level 0

## Goal

The goal of this level is to use SSH to connect to the game. Once I input the credentials, I must find a file that contains the password to access the next level.

## Concepts

SSH (Secure Shell) is a protocol for securely connecting to remote machines over a network.
`ls` was used to list information about the files in the current directory.
`cat` was used to concatenate the files `README` to standard output.

## What I did

Information I was given:

- Host: bandit.labs.overthewire.org
- Username: bandit0
- Password: bandit0

I connected to OverTheWire using the command:

`ssh -p port user@host`

In which `-p` specifies the port and `user@host` being our user and host, I input the command:

`ssh -p 2220 bandit0@bandit.labs.overthewire.org`

Once I did this, I was given a field to input the password `bandit0`.

Now, logged in, I used the command:

`ls`

Which gave me the contents of the directory being:

`README`

I then used `cat` which gave me the password for the next level.

## What I learned

SSH is how admins manage servers remotly, so almost everythng in OverTheWire: Bandit starts from this connection. `ls` and `cat` will likely be a large part of this game since they are ways of accessing information.

## Real-world Application

Attackers could probably scan the internet for open SSH ports and guess weak passwords. Defenders can use key based logins instead of passwords and watch logs for failed attempts.
