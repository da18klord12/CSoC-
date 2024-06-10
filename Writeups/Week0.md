# WriteUps for CSoC Infosec Week - 0

## Challenge 1 - Bandit WarGames 
Obviously after each level exit and then again login to another level using ssh and the password retrieved 
### Level 0 - 1 

    login using SSH with the username and password, then after connection being successful, proceed 

    ls 
    cat README

    and you get the password for the next level

### Level 1 - 2

    ls -al
    cat ./-

    and you get the password for the next level

### Level 2 - 3

    ls -al
    cat spaces\ in\ this\ filename

    and you get the password for the next level

### Level 3 - 4

    ls -al 
    cd inhere/
    ls -al
    cat .hidden

    and you get the password for the next level

### Level 4 - 5

    ls -al
    cd inhere/
    ls -al | xargs -a
    cat ./-file07

    and you get the password for the next level

### Level 5 - 6

    ls -al
    cd inhere/
    ls -al
    find . -type f -size 1033c
    cat ./maybehere07/.file2

    and you get the password for the next level

### Level 6 - 7

    ls -al
    find / -type f -user bandit7 -group bandit6 -size 33c
    cat /var/lib/dpkg/info/bandit7.password

    and you get the password for the next level

### Level 7 - 8

    ls -al
    cat data.txt
    grep "millionth" data.txt

    and you get the password for the next level

### Level 8 - 9

    ls -al
    cat data.txt
    sort data.txt | uniq -c

    and you get the password for the next level

### Level 9 - 10

    ls -al
    cat data.txt
    strings data.txt | grep "="

    and you get the password for the next level

### Level 10 - 11

    ls -al
    cat data.txt 

    go to cyber chef and decode the base64 you got after $ cat data.txt

    and you get the password for the next level

### Level 11 - 12

    ls -al
    cat data.txt

    copy ROT13 txt and decode it on Cyberchef 

    and you get the password for the next level

### Level 12 - 13

    ls -al
    mkdir /tmp/da18k
    cp data.txt /tmp/da18k
    cd /tmp/da18k/
    xxd -r data.txt > datausable 
    file datausable
    mv datausable datusable.gz
    gzip -d filenow.gz
    file filenow
    mv filenow filenow.gz
    gzip -d filenow.gz
    ls
    file filenow
    mv filenow filenow.tar
    tar xf filenow.tar
    ls
    file data5.bin
    mv data5.bin data.tar
    tar xf data.tar
    ls
    file data
    mv data data1.tar
    tar xf data1.tar
    ls
    file data8.bin
    mv data8.bin data.gz
    gzip -d data.gz
    ls
    file data
    cat data 

    and you get the password for the next level

### Level 13 - 14

    ls -al
    ssh -i sshkey.private bandit14@localhost -p 2220

### Level 14 - 15

    cat etc/bandit_pass/bandit14
    
    and you get the password for the current lvl

    nc localhost 30000

    enter the lvl 14 password for lvl 15 password 
    and you get the password for the next level

### Level 15 - 16

    ncat --ssl localhost 30001
    
    enter the lvl 15 password for lvl 16 password 
    and you get the password for the next level

### Level 16 - 17

    nmap localhost -p 31000-32000
    ncat --ssl localhost 31790
    
    enter lvl 16 password for lvl 17 password 

    and in this case we got an RSA Private key
    so just copy the key 

Before moving to another lvl you need this key so save it 

 $vim key <br/>
 paste </br>
 :wq </br>
 $chmod 400 key 

now login to next level using the key 

    ssh -i key bandit17@bandit.labs.overthewire.org -p 2220

### Level 17 - 18

    ls 
    diff --normal passwords.old passwords.new

    and you get the password for the next level

For the next lvl i.e. Lvl 18 we need to force pseudo terminal 

    ssh -t bandit18@bandit.labs.overthewire.org -p 2220

### Level 18 - 19

    ls
    cat readme 

### Level 19 - 20

    ls -al
    ./bandit20-do
    ./bandit20-do id
    
    ok so we can use this .exec to run other commands 

    ./bandit20-do cat etc/bandit_pass/bandit20 

    and you get the password for the next level

### Level 20 - 21

    ls -al
    ./suconnect 

    ok so now establish connection for this level on another terminal and them connect to another port let's say 1234

    nc -lp 1234

    now return to orginal terminal and then..

    ./suconnect 1234

    enter lvl 20 password for lvl 21 password 

    and you get the password for the next level

### Level 21 - 22

    cd /etc/cron.d
    ls
    cat crojob_22
    cat /usr/bin/cronjob_bandit22.sh
    cat /tmp/t706...

    and you get the password for the next level

### Level 22 - 23

    ls /etc/cron.d/
    cat /etc/cron.d/cronjob_bandit23
    cat /usr/bin/cronjob_bandit23.sh
    whoami
    echo I am user bandit23 | md5sum | cut -d ' ' -f 1
    cat /tmp/<string>

    and you get the password for the next level

### Level 23 - 24

    cat /etc/cron.d/cronojob_bandit24
    cat /usr/bin/cronjob_bandit24.sh
    cd /etc/cron.d/conjob_bandit24
    cd /usr/bin/cronjob_bandit24.sh
    cd /tmp
    mkdir dark/
    cd /dark

    now create a shell script and name it script.sh

    chmod 777 script.sh
    ls 
    touch passwd
    chmod 777 passwd 
    cd .. 
    cd ..
    chmod 777 /tmp/dark
    cd /tmp/dark/
    cp script.sh /var/spool/bandit24/foo
    cat passwd  

    after 1 min 

    and you get the password for the next level

### Level 24 - 25

    nc localhost 30002

    enter password of lvl 24 for lvl 25 password and <pin> (random bruteforcing) failed😭

    mkdir /tmp/band24

    now create a shell script using python for bruteforcing using loop of combination from 0000 to 9999

    chmod 777 pass.sh
    ./pass.sh

    and now you get the pin and paste it along side this lvl passford for nxt password 

    and you get the password for the next level

### Level 25 - 26

    ls
    more bandit26.sshkey

    before proceeding to nxt part if you notice that the Bandit26 img which appears is somewhat glowing on top side so resize the terminal till that part only and then proceed and after connenction you can again enlarge the terminal

    ssh -i bandit26.sshkey bandit26@localhost -p 2220
    i   (insert)
    esc  (exit from insert mode)
    :e /etc/bandit_pass/bandit26

    and you get the password for the next level

### Level 26 - 27

    again reduce the size of terminal and 
    ssh -i bandit26.sshkey bandit26@localhost -p 2220

    i  (insert)
    esc 
    :set shell = /bin/bash
    :shell

    ls
    ./bandit27-do cat /etc/bandit_pass/bandit27

    and you get the password for the next level

### Level 27 - 28

    mkdir /tmp/dark18/
    cd /tmp/dark18/
    
    git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo

    ls -al
    cd repo/
    cat README 

    and you get the password for the next level

### Level 28 - 29

    mkdir /tmp/dark18n/
    cd /tmp/dark18n/
    git clone ssh://....
    ls
    cd repo/
    cat README.md
    git log 
    git checkout <latest commit> 

    and you get the password for the next level

### Level 29 - 30

    mkdir /tmp/da18/
    cd /tmp/da18/
    git clone ssh://....
    ls
    cd repo/
    cat README.md
    git log 
    git branch -r
    git checkout dev
    cat README.md

    and you get the password for the next level

### Level 30 - 31

    mkdir /tmp/da18n/
    cd /tmp/da18n/
    git clone ssh://...
    ls 
    cd repo/
    cat README.md
    git tag
    git show secret 

    and you get the password for the next level

### Level 31 - 32

    mkdir /tmp/darkn/
    cd /tmp/darkn/
    git clone ssh://...
    ls 
    cd repo/
    ls
    cat README.md
    git branch 
    eho "May I come in?"
    git commit -m "added key.txt"
    git push
    
    enter lvl 31 password for lvl 32 password 

    and you get the password for the next level

### Level 32 - 33

    $0
    export SHELL=/bin/bash
    echo $SHELL
    $SHELL

    and we are done with the Challenge 

## Challenge 2 - Programming 
### 1. Russian Roulette 
> unable to figure out how to randomly revolve the rounds, so i will write the code once i get that

> same is the case with other programs so i will figure about them and upload 







    



