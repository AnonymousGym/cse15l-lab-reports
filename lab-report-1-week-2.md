__Tutorial for CSE 15L Week 1__

# Steps: 1.Installing VScode

Go download VScode at this website:
[Link][1]

[1]:  https://code.visualstudio.com/
Follow the instructions to install, and you shall see this page:
![Image][11]

[11]: 1.png

# 2.Remotely Connecting

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


# 3.Trying Some Commands

Lucky to arrive here!
Try running the commands _cd, ls, pwd, mkdir,_ and _cp_ a few times in different ways, 
both on your computer, and on the remote computer after ssh-ing. 
This is some of my tests:
![Image][13]

[13]: 3.png

# 4.Moving Files with scp

Try to copy a file from your computer to a remote computer.
The command is called _scp_, run it from your computer.
Create a file on your computer called _WhereAmI.java_ and put some code:

_class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}_

Run the java file with javac and java command.
You should see this:
![Image][14]

[14]: 4.png

Then in the terminal from the directory where you made this file, log in to your account using ssh
Use _ls_ and see the file there in your home directory.
Now you can run it on the ieng6 computer using _javac_ and _java_.

![Image][17]

[17]: 7.png

![Image][18]

[18]: 8.png

# 5.Setting an SSH Key

To avoid typing password every time we log in, we can use ssh keys.
Follow these steps:
_# on client (your computer)
$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/joe/.ssh/id_rsa): /Users/joe/.ssh/id_rsa
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /Users/joe/.ssh/id_rsa.
Your public key has been saved in /Users/joe/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:jZaZH6fI8E2I1D35hnvGeBePQ4ELOf2Ge+G0XknoXp0 joe@Joes-Mac-mini.local
The key's randomart image is:
+---[RSA 3072]----+
|                 |
|       . . + .   |
|      . . B o .  |
|     . . B * +.. |
|      o S = *.B. |
|       = = O.*.*+|
|        + * *.BE+|
|           +.+.o |
|             ..  |
+----[SHA256]-----+_
You should follow the steps and see this:
![Image][15]

[15]: 5.png

# 6.Optimizing Remote Running

Welcome to the last step!
Some tips for you!
  You can write a command in quotes at the end of an ssh command to directly run it on the remote server, then exit. 
  For example, this command will log in and list the home directory on the remote server:
_$ ssh cs15lwi22@ieng6.ucsd.edu "ls"_

  You can use semicolons to run multiple commands on the same line in most terminals. For example, try:
_$ cp WhereAmI.java OtherMain.java; javac OtherMain.java; java WhereAmI_

  Use the up-arrow on your keyboard to recall the last command that was run.
![Image][16]

[16]: 6.png

Hopefully you've finished! If you have problems, ask on Piazza or any TA or classmates!





