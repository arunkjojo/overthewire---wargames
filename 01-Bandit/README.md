# OverTheWire: ‘Bandit’ Solutions using Google Cloud Shell

    https://shell.cloud.google.com/?show=ide%2Cterminal

    The Bandit wargame is aimed at absolute beginners. It will teach the basics needed to be able to play other wargames.

# Game Start

## Bandit Level 0:

### Level Goal

    The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

### Guid

    ssh

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit0@bandit.labs.overthewire.org -p 2220
    password:
        bandit0

    `bandit0@bandit:~$ ls`
        readme
    `bandit0@bandit:~$ cat readme`
        NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

## Bandit Level 0 → Level 1:

### Level Goal

The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

### Guid

    ls , cd , cat , file , du , find

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit1@bandit.labs.overthewire.org -p 2220
    password:
        NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

    `bandit1@bandit:~$ ls -a`
        -  .  ..  .bash_logout  .bashrc  .profile
    `bandit1@bandit:~$ cat ./-`
        rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

## Bandit Level 1 → Level 2:

### Level Goal

    The password for the next level is stored in a file called - located in the home directory

### Guid

    ls , cd , cat , file , du , find

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit2@bandit.labs.overthewire.org -p 2220
    password:
        rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

    `bandit2@bandit:~$ ls`
        spaces in this filename
    `bandit2@bandit:~$ cat "spaces in this filename"`
        aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

    or

    `bandit2@bandit:~$ dir`
        spaces\ in\ this\ filename
    `bandit2@bandit:~$ cat spaces\ in\ this\ filename`
        UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

## Bandit Level 2 → Level 3:

### Level Goal

    The password for the next level is stored in a file called spaces in this filename located in the home directory

### Guid

    ls , cd , cat , file , du , find

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit3@bandit.labs.overthewire.org -p 2220
    password:
        aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

    `bandit3@bandit:~$ ls`
        inhere
    `bandit3@bandit:~$ cd inhere`
    `bandit3@bandit:~$ ls`
        .  ..  .hidden
    `bandit3@bandit:~$ cat .hidden`
        2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

## Bandit Level 3 → Level 4:

### Level Goal

    The password for the next level is stored in a hidden file in the inhere directory.

### Guid

    ls , cd , cat , file , du , find

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit4@bandit.labs.overthewire.org -p 2220
    password:
        2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

    `bandit4@bandit:~$ ls -a`
        .  ..  .bash_logout  .bashrc  .profile  inhere
    `bandit4@bandit:~$ cd inhere`
    `bandit4@bandit:~/inhere$ ls -a`
        -file00  -file02  -file04  -file06  -file08  .
        -file01  -file03  -file05  -file07  -file09  ..
    `bandit4@bandit:~/inhere$ file ./-*`
        ./-file00: data
        ./-file01: data
        ./-file02: data
        ./-file03: data
        ./-file04: data
        ./-file05: data
        ./-file06: data
        ./-file07: ASCII text
        ./-file08: data
        ./-file09: data
    `bandit4@bandit:~/inhere$ cat ./-file07`
        lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

## Bandit Level 4 → Level 5:

### Level Goal

    The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

### Guid

    ls , cd , cat , file , du , find

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit5@bandit.labs.overthewire.org -p 2220
    password:
        lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

    `bandit4@bandit:~$ ls`
        inhere
    `bandit5@melinda:~/inhere$ ls -a`
        .            maybehere02  maybehere06  maybehere10  maybehere14  maybehere18
        ..           maybehere03  maybehere07  maybehere11  maybehere15  maybehere19
        maybehere00  maybehere04  maybehere08  maybehere12  maybehere16
        maybehere01  maybehere05  maybehere09  maybehere13  maybehere17
    `bandit5@melinda:~/inhere$ find -type f -size 1033c`
        ./maybehere07/.file2
    `bandit5@melinda:~/inhere$ cat ./maybehere07/.file2`
        P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

## Bandit Level 5 → Level 6:

### Level Goal

    The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

    human-readable
    1033 bytes in size
    not executable

### Guid

    ls , cd , cat , file , du , find

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit6@bandit.labs.overthewire.org -p 2220
    password:
        P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

## Bandit Level 6 → Level 7:

### Level Goal

    The password for the next level is stored somewhere on the server and has all of the following properties:

    owned by user bandit7
    owned by group bandit6
    33 bytes in size

### Guid

    ls , cd , cat , file , du , find , grep

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit7@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 7 → Level 8:

### Level Goal

    The password for the next level is stored in the file data.txt next to the word millionth

### Guid

    man, grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit8@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 8 → Level 9:

### Level Goal

    The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

### Guid

    grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit9@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 9 → Level 10:

### Level Goal

    The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

### Guid

    grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit10@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 10 → Level 11:

### Level Goal

    The password for the next level is stored in the file data.txt, which contains base64 encoded data

### Guid

    grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit11@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 11 → Level 12:

### Level Goal

    The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

### Guid

    grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit12@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 12 → Level 13:

### Level Goal

    The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

### Guid

    grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit13@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 13 → Level 14:

### Level Goal

    The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

### Guid

    ssh, telnet, nc, openssl, s_client, nmap

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit14@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 14 → Level 15:

### Level Goal

    The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

### Guid

    ssh, telnet, nc, openssl, s_client, nmap

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit15@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 15 → Level 16:

### Level Goal

    The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

    Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…

### Guid

    ssh, telnet, nc, openssl, s_client, nmap

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit16@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 16 → Level 17:

### Level Goal

    The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

### Guid

    ssh, telnet, nc, openssl, s_client, nmap

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit17@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 17 → Level 18:

### Level Goal

    There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

    NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

### Guid

    cat, grep, ls, diff

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit18@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 18 → Level 19:

### Level Goal

    The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

### Guid

    ssh, ls, cat

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit19@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 19 → Level 20:

### Level Goal

    To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

### Guid

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit20@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 20 → Level 21:

### Level Goal

    There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

    NOTE: Try connecting to your own network daemon to see if it works as you think

### Guid

    ssh, nc, cat, bash, screen, tmux, Unix ‘job control’ (bg, fg, jobs, &, CTRL-Z, …)

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit21@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 21 → Level 22:

### Level Goal

    A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

### Guid

    cron, crontab, crontab(5) (use “man 5 crontab” to access this)

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit22@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 22 → Level 23:

### Level Goal

    A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

    NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

### Guid

    cron, crontab, crontab(5) (use “man 5 crontab” to access this)

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit23@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 23 → Level 24:

### Level Goal

    A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

    NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

    NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

### Guid

    cron, crontab, crontab(5) (use “man 5 crontab” to access this)

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit24@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 24 → Level 25:

### Level Goal

    A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.
    You do not need to create new connections each time

### Guid

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit25@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 25 → Level 26:

### Level Goal

    Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

### Guid

    ssh, cat, more, vi, ls, id, pwd

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit26@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 26 → Level 27:

### Level Goal

    Good job getting a shell! Now hurry and grab the password for bandit27!

### Guid

    ls

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit27@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 27 → Level 28:

### Level Goal

    There is a git repository at ssh://bandit27-git@localhost/home/bandit27-git/repo via the port 2220. The password for the user bandit27-git is the same as for the user bandit27.

    Clone the repository and find the password for the next level.

### Guid

    git

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit28@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 28 → Level 29:

### Level Goal

    There is a git repository at ssh://bandit28-git@localhost/home/bandit28-git/repo via the port 2220. The password for the user bandit28-git is the same as for the user bandit28.

    Clone the repository and find the password for the next level.

### Guid

    git

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit29@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 29 → Level 30:

### Level Goal

    There is a git repository at ssh://bandit29-git@localhost/home/bandit29-git/repo via the port 2220. The password for the user bandit29-git is the same as for the user bandit29.

    Clone the repository and find the password for the next level.

### Guid

    git

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit30@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 30 → Level 31:

### Level Goal

    There is a git repository at ssh://bandit30-git@localhost/home/bandit30-git/repo via the port 2220. The password for the user bandit30-git is the same as for the user bandit30.

    Clone the repository and find the password for the next level.

### Guid

    git

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit31@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 31 → Level 32:

### Level Goal

    There is a git repository at ssh://bandit31-git@localhost/home/bandit31-git/repo via the port 2220. The password for the user bandit31-git is the same as for the user bandit31.

    Clone the repository and find the password for the next level.

### Guid

    git

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit32@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 32 → Level 33:

### Level Goal

    After all this git stuff its time for another escape. Good luck!

### Guid

    sh, man

### Commands

    arunkjojo@cloudshell:~ (ceh-training-42786)$
        ssh bandit33@bandit.labs.overthewire.org -p 2220
    password:

## Bandit Level 33 → Level 34:

### Level Goal

    At this moment, level 34 does not exist yet.

# Thank you

    Thank you for checking out my course! If you have any questions or suggestions, feel free to open an issue or contact me.
