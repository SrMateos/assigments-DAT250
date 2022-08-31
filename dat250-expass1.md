# DAT250 EXPASS1

## Introduction
The goal of the assigment is to create a working Software Development Enviroment needed for the rest of the subject. The main thing we are going to use is [Heroku](https://www.heroku.com) which is a Cloud Application Platform that will help us to make Cloud Computation. In my case, I am using a Linux distro, based on ArchLinux, so every explanation will refer to my own case.

## Instalation
### Updating
First of all, I updated my computer, so everything is up to the lastest version.

```
paru -Syu
```

### Maven instalation
As JDK, Eclipse and a git client were already installed in my PC, the next step is to install Maven, so I downloaded it from the [official site](https://maven.apache.org/), unzipped the compressed file and added the bin folder to the enviroment variable PATH.
```
wget https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.zip
unzip apache-maven-3.8.6-bin.zip
cd apache-maven-3.8.6/bin
export PATH=$PATH:$(pwd)
```
To check if maven is already working, I just did:
```
mvn -v
```
Something like this should appear:
```
Apache Maven 3.8.6 (84538c9988a25aec085021c365c560670ad80f63)
Maven home: /opt/maven
Java version: 18.0.2, vendor: N/A, runtime: /usr/lib/jvm/java-18-openjdk
Default locale: es_ES, platform encoding: UTF-8
OS name: "linux", version: "5.15.60-1-manjaro", arch: "amd64", family: "unix"
```

### Heroku instalation
For the Heroku instalation we need some requirements. As I have already installed Maven and it is easy to create a Heroku account I skip this parts. The next thing is Java 8, that I had already installed but not working, as the output of `java --version` is the following: 
``` 
openjdk 18.0.2 2022-07-19
OpenJDK Runtime Environment (build 18.0.2+9)
OpenJDK 64-Bit Server VM (build 18.0.2+9, mixed mode)
```

As I said if I check the java versions I have installed with `archlinux-java status`, the following appears:
```
Available Java environments:
  java-11-openjdk
  java-18-openjdk (default)
  java-8-openjdk
```

We just have to change the version with `sudo archlinux-java set java-8-openjdk`, and if we do `java -version` we can check that we changed the version.
```
openjdk version "1.8.0_345"
OpenJDK Runtime Environment (build 1.8.0_345-b01)
OpenJDK 64-Bit Server VM (build 25.345-b01, mixed mode)
```