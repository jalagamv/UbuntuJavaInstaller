# Ubuntu Java Installer (ujavainstaller.sh)
Bash script that automates installation of Oracle Java (JDK) on Ubuntu Linux and its derivatives (like Linux Mint).

## Usage
```
Download the desired JDK archive (.tar.gz) from Oracle website:
http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

Usage:   ./ujavainstaller.sh [options] jdk-archive-file.tar.gz

Available options are:
  --remove-openjdk
      Removes (purges) OpenJDK from the system. Using this option
      ensures that OpenJDK is not present in the system, therefore
      no application will use it instead of Oracle JDK.
      Use this option with caution, as APT may remove other packages
      through dependencies. Before APT start removing OpenJDK from
      the system it will ask for your confirmation and display
      a complete list of software it is going to remove along with
      OpenJDK.

  --help
      Displays this help message.
```

***NOTE***

Before running the script make sure it has permissions to execute and you run it with root permissions.

Set execution permissions with ```chmod +x ujavainstaller.sh```
and execute it with root permissions with ```sudo ./ujavainstaller.sh```

## Example usage and output
The ```jdk-8u72-linux-x64.tar.gz``` file was previously downloaded from the [Oracle Website](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).

```
root@ip-172-31-32-164 ~/Temp $ chmod +x ujavainstaller.sh 
root@ip-172-31-32-164 ~/Temp $ sudo ./ujavainstaller.sh jdk-8u72-linux-x64.tar.gz 

Ubuntu Java Installer

Validating the archive file... OK
Extracting the archive... OK
Updating /etc/profile ... OK
Updating system alternatives... OK
Verifying Java installation... OK

Java is successfully installed!

java version "1.8.0_72"
Java(TM) SE Runtime Environment (build 1.8.0_72-b15)
Java HotSpot(TM) 64-Bit Server VM (build 25.72-b15, mixed mode)

root@ip-172-31-32-164 ~/Temp $ 
```

See my article about [how to install Java on Ubuntu](http://adamscheller.com/linux/how-to-install-java-on-ubuntu/) with UbuntuJavaInstaller.

## License
Please refer to http://java.com/license

