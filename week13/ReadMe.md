
## Homework chapter9

# 1)
```bash 

sudo adduser controller
```
# 2)
```bash
sudo  usermod –a -G sudo controller
```
# 3) 
```bash

 sudo adduser nsa-spy
     sudo userdel nsa-spy
```
# 4)
```bash

sudo adduser mysql-backup 
sudo visudo 
```
then : 
![ITM]( ../Images/q4.png "Family" )

# 5)
```bash

sudo addgroup mysql-admins
sudo visudo
```
then:
![ITM](../Images/q5.png "q5")

# 6)
```bash

sudo adduser mysql-admin
sudo visudo
```
then: 
![ITM](../Images/q6.png "q6")

# 7)
```bash

sudo visudo
```
then: 
![ITM](../Images/q7.png "q7")

# 8)
![ITM](../Images/q8.png "q8")

Journatctl is a command, it is use to acces the logs files. It is not a file or a directory so you cannot use it with tail. It is necessary to add parameter to the command journalctl to make it display the content the way you want it to be. 

Journalctl –options

# 9)
```bash

journalctl _COMM=sshd
```
# 10)
```bash

journalctd  _PID=1 --since=yesterday
```
# 11)
```bash

journalctl –b
```
# 12)
We will have to edit the storage part of the file /etc/systemd/journald.conf
And add : - Storage=volatile

# 13)
I have 11G on the /dev/sda1. so 20% of 11 is 2.2GB and 30% is 3.3GB
I need to edit the file and change the value as follow.
I type, vim journald.conf
SystemMaxUse=2.2GB
RuntimeMaxUse=3.3GB


# 14)
tap crontab -e. then I edit the document as follow:

0 2 * * 0  mysqldump –xml -u root world City


# 15)
tap crontab -e. then I edit the document as follow:

 \* * 1 * *  mysqldump –xml -u root world City


# 16)
tap crontab -e. then I edit the document as follow:

/45 * * * *  mysqldump –xml -u root world City


# 17)
tap crontab -e. then I edit the document as follow:

45 * * * 0  mysqldump –xml -u root world City

# 18)
tap crontab -e. then I edit the document as follow:

45 2 * * 2  mysqldump –xml -u root world City



# 19)
- sudo addgroup accounting
- chgrp accounting todo-list.txt


# 20)
sudo chown root:root todolist.txt




