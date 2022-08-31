# DAT250 EXPASS1

## Introduction
The goal of the assigment is to create a working Software Development Enviroment needed for the rest of the subject. The main thing we are going to use is [Heroku](https://www.heroku.com) which is a Cloud Application Platform that will help us to make Cloud Computation. In my case, I am using a Linux distro, based on ArchLinux, so every explanation will refer to my own case.

## Instalation
First of all, I updated my computer, so everything is up to the lastest version.

```
paru -Syu
```

After this, I installed maven in my PC, as JDK, Eclipse and a git client were already installed in my PC. So I downloaded Maven from the [official site](https://maven.apache.org/), decompress the zip and added the bin folder to the path.
```
wget https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.zip
unzip apache-maven-3.8.6-bin.zip
cd apache-maven-3.8.6/bin
export PATH=$PATH:$(pwd)
```
