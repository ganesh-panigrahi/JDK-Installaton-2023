# Installing JDK-19 in Ubuntu 22.04

## 1. Installing the jdk-19 debian package from the official website of oracle jdk downloads page.

![1.](Google.png "Google Search") <br />
Click on Java Downloads <br />

![2.](oracle.png "Oracle Downloads page") <br />
Click on the link next to x64 Debian Package for Ubuntu. <br />
Your JDK will be downloaded. <br />


## 2. Installing process in terminal
Open terminal in your downloads directory and type the following: <br />
1. `sudo dpkg -i jdk-19_linux-x64_bin.deb` : Unpacking the JDK file. <br /> <br />
![3.](3.png "Unpacking JDK File") <br />

- If encountered an error like this :  <br />
![4.](4.png "error1") <br />
then the solution is to type `sudo apt --fix-broken install` and then unpack debian package <br /> again. The error will get solved. <br />

2. `ls /usr/lib/jvm` : to check jdk installation. <br />
![5.](5.png "jdk") <br />

3. `sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-19/bin/java 1` : to install java and then check the installatin of java by typing `java -version`.<br />
![6.](java.png "java") <br />

4. `sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk-19/bin/javac 1` : to install javac and then check the installatin of javac by typing `javac -version`.<br />
![7.](7.png "javac") <br />

5. `sudo update-alternatives --config java` : to update and then copy this `/usr/lib/jvm/jdk-19/bin/java` which will be used further. <br />
![8.](8.png "config") <br />

6. `sudo gedit /etc/environment` <br />
![9.](9.png "gedit") <br />
After entering the password a text editor window will open like this: <br />
![10.](10.png "gedit") <br />
In this write this `JAVA_HOME="/usr/lib/jvm/jdk-19"` in the second/ last line and then save it and close the window. <br />
![11.](11.png "gedit") <br />

7. `source /etc/environment` then press enter. <br />

8. `echo $JAVA_HOME` then press enter. <br />
![12.](12.png "gedit") <br />

9. Congratulations! You've installed JDK-19 successfully in your Ubuntu 22.04 system.  <br />



