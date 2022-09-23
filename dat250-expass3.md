# DAT250 EXPASS3
## Introduction
The objetive of this assignment is to understand how to use mongodb to perform basic CRUD operations as well as aggregation.

## Validation of the installation package
I am using ArchLinux, so there is no official support for mongodb, but [AUR](https://aur.archlinux.org/) repository provides de package from Ubuntu. At the moment of installing it, the repository installer of ArchLinux checks by default the sha256 hashes, so if mongodb was installed correctly, it means that the hashes should be fine. To check it, by following the [verification tutorial](https://www.mongodb.com/docs/manual/tutorial/verify-mongodb-packages/) we get to see that everything should work.
![](imgs/verificationWithWarning.png)
![](imgs/verifyChecksum.png)

Note: in the first picture we can see a warning but the sign is correct. As it is not a big problem and it is probably caused by the problems with the non-official repositories, we can just suppose that everything is fine (or that is what I was told to do by the lab assistant).

## Experiment 1
### Create operation
With the method `insertMany` we can introduce some documents into collections, in this case the collection is `inventory`. Every single document should have an id.
![](imgs/createOperation.png)

### Read operation
With the `find` function we can query data from collections, in this case the collection is `inventory`. We can also apply filters to take the attributes that has an specific value, or that satisfies certain conditions. In this case we are looking for those documents whose status are D, and their qty is lower than 75 or the name of the attribute item starts with p;
![](imgs/findOperation.png)

### Update operation
![](imgs/updateOperation.png)

### Delete operation
![](imgs/deleteOperation.png)

## Experiment 2
