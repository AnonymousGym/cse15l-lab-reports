__Tutorial for CSE 15L Week 1__

__Steps:
1.Installing VScode__

Go download VScode at this website:
[Link][1]

[1]:  https://code.visualstudio.com/
Follow the instructions to install, and you shall see this page:
![Image][11]

[11]: 1.png

__2.Remotely Connecting__

The second step is to connect to your account.
_If you're using Windows, you have to install this:_
[Link][2]

[2]:  https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse
Then,look up your course-specific account for CSE15L here:
[Link][3]

[3]:  https://sdacs.ucsd.edu/~icc/index.php
To connect in VSCode, open a new terminal and type command:

$ ssh cs15lwi22zz@ieng6.ucsd.edu

While _zz_ in it should be replaced by your course-specific account.
If it does not work, replace the _cs15lwi22zz_ part with your account.

Type _yes_ if asked to choose yes or no.
Then you type in the password and hopefully you can arrive at this:
![Image][12]

[12]: 2.png


__3.Trying Some Commands__

Lucky to arrive here!
Try running the commands _cd, ls, pwd, mkdir,_ and _cp_ a few times in different ways, 
both on your computer, and on the remote computer after ssh-ing. 
This is some of my tests:
![Image][13]

[13]: 3.png

4.Moving Files with scp
5.Setting an SSH Key
6.Optimizing Remote Running




![Image][4]

[4]: screenshot1.png

