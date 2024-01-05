# Linux---Commands-cheat-sheet
    
which firefox : To find the path of any program such as firefox

gedit firefox : To open the code file of any program such as firefox

whoami : To know the account of exising user such as a local host or a root account of that user

useradd tom : To add a user suuch as tom

passwd tom :To set a password for any user such as tom

jobs : To know what all jobs/programs/softwares are running

free : Tells us the system's memory usage in kilobytes

free -m : Tells us the system's memory usage in megabytes

man free : To access the manual of any command such as free

date +%r : It displays the current time in 12-hour clock format with AM or PM

gnome-screenshot :  It is used to take screenshots of your desktop or specific areas of your screen when you are using the GNOME desktop environment. GNOME is a popular graphical user interface used in many Linux distributions.

cd .. : Go back in path 

pwd[print working directory]

eog sn1.png : The eog command in Linux stands for "Eye of GNOME." It is the default image viewer for the GNOME desktop environment, and it allows you to view and interact with images and photos on your Linux system. You can use the eog command in the terminal to open an image file for viewing.

firefox  & : This command in Linux is used to start any program in the background such as firefoxr. The & symbol is used to run a command as a background process, which means that you can continue to use the terminal for other tasks while Firefox is running in the background.


Any program/application which we run on our computer can be run in 2 ways: 1. CLI-curl www.google.com    2. GUI - chrome

rpm -q software_name : To check any software availbility 

netstat - tnlp : To find the port number of a running software(But this has become older)

ss - tnlp

mkdir dir_name : To make a new directory

rm dir  dir_name : To remove directory

pgrep : To find process id of any running application

ssh -l root IP/ssh root@IP : 	To login to another computer through ssh command

vim /etc/ssh/sshd_config : To open the configuration file of ssh (In this file # means default settings)

systemctl reload sshd : To reload the existing already started sshd

rpm -q -c openssh_server

# To disable the SELinux security
getenforce 
setenforce 0
system restart sshd

While changing the port number of any service/program,make sure that the new port number which you will assig should be free i.e shoulld not be already taken by any other service/program

whoami : Will tell you that from which user you are logged in

who : Will tell that what all users were logged in

ssh root@IP -p31 : Will login to other computer,run the program of which port number we will mention and immediately log out

cat secure : secure file is a log file which stores all the information of the users logging in and what all activities they did

semanage port -l : By running this command,you will see all the default port numbers which SELinux had already assigned and providing it to you

ssh - Secure Shell  (ssh client,ssh server) (supports connection b/w two different O.S and works on almost every O.S)

scp(Secure Copy) - This command is used for file transfer between two computers (Downloading and uploading)

scp -l root@IP:/root/vimal.txt (We need to mention the path of download/upload) (l stands for login)

scp is just a command but the protocol it is working on is SFTP(Secure file transfer protocol). SFTP is one feature of ssh

scp -r root@IP:/root/code/Path to download : -r means recursive download which means one by one file will get download from the entire folder. Here code/ means that we are giving a folder ?????upload command

Some GUI's for logging in to computer and running a command : Putty

Some GUI's for logging in to computer and uploading or downloading file basically file transfer - WinSCP

cat/var/log/secure - to see all the history

passwd -d jack : -d means to remove password for the user jack so that next time whenever user will login,he/she can login without the password.But this can happen only locally and is not allowed during ssh networking. Still if there is a need to do the same for ssh networking,we need to make some changes in the empty passwd tag in configration files.

************Multi user login is possible in both the ways. i.e locally as well as remotely

printmotd : motd means message of the day. This message will be displayed whenever a user logs in

