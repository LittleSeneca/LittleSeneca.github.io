---
layout: post
title:  Hard Drive Auditing Tool
categories: [Bash,Linux,Code,Github]
---

# Introduction
<img align="left" src="/images/GitHub_Logo.png" width="100">Many organizations have stacks of hard drives laying around the office.
Many of these hard drives are unlabeled. Thats dangerous!
This tool provides a fast process to quickly analyze hard drives 
for their file contents. No need to manually click through file systems.

If the drive is a standard un-encrypted windows drive, it will simply crawl 
through the drive, finding and displaying the hostname from the registry 
and the user folder contents.

If its a bitlocker encrypted windows drive, it will prompt you for the recovery
password (which im assuming can be pulled from your Org's ADUC). Once the 
password has been accepted, the script will automatically mount the bitlocker 
drive and scan it like an un-encrypted windows drive. 

If the drive is a filesystem without a operating system, it will output the 
root directory file system of the drive. 

If the drive is a linux filesystem, it will output the root directory file
system of the drive and state that it is a linux boot device. 

# How to Use the tool
First, you need to have a linux computer. <br/>
Second, you need to download the repo - like this:

    git@github.com:LittleSeneca/hard-drive-auditor.git

Third, you need to plug a hard drive into your machine using a usb connection <br/>
Fourth, run the command below from the cloned directory:

    sudo Drive_Scanner.sh

Fifth, Enjoy the profit. <br/>
Rinse and repeat steps 3-5 for each drive you have.

```
