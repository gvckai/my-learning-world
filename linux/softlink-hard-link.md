# inode - symlink and hard link
 - Person Metadata
    - Name :
    - Last Name
    - data of birth
    - aadhar ect
# file or folder has metadata
 - who is the owner 
 - which group has access
 - what are the permissions 
 - when it is created 
 - when is it updated 
 - where is the actual contenet -> is not part of metadata

 ## To find inode number
  - **ls -li pile name - it prints inode number that you created **
 ```
 ls -li sample.txt (filename) we can see inode number
 ```

  - If you want see full informatio of the file (the meta data of the file)

stat file name -> **we acn see inode information**

```
stat gvckai
```

  File: gvckai
  size: 411             Blocks: 8          IO Block: 4096   regular file
Device: 8,48    Inode: 16408       Links: 1
Access: (0600/-rw-------)  Uid: ( 1000/   vijay)   Gid: ( 1000/   vijay)
Access: 2026-11-01 03:56:11.188031816 +0000
Modify: 2026-10-19 15:09:13.699013738 +0000
Change: 2026-10-19 15:09:13.699013738 +0000
 Birth: 2026-10-19 15:09:13.699013738 +0000

 # Symlink - shortcut/home/vijay/repositories/devops/symlink/symlink.txt
 - /home/vijay/repositories/devops/symlink/symlink.txt
 ```
 ln -s /home/vijay/repositories/devops/symlink/symlink.txt sl.txt
 ```
 
 - **up to rhel 7 we are yousing yum**
 - **from rhel8 we are using dnf**
```
which yum
```
## symlink or soft lint
- Works as shortcut to file/folder
- used for backword compatability
- used for version switching at the time of updrading (your refferencing no be changed)
- if we remove actual file, symlink will brack
- **if 3.15 is faild ? again unlink and point at to 3.15**
 ln -s prometheus-3.13.5.linux-amd64 prometheus
 rm prometheus -->unlink 

## shortcut inode and main file inode no are different
- **inode number of symlink and actual file is different**
- just it is pointer only
```
ln -li sl.txt 
# 14385 lrwxrwxrwx 1 vijay vijay 51 Nov 16 11:40 sl.tx
```
- **mainfile inod number is deferent**
```
ls -li /home/vijay/repositories/devops/symlink/symlink.txt
#14265 -rw-r--r-- 1 vijay vijay 82 Nov 16 09:11 /home/vijay/repositories/devops/symlink/symlink.txt
```

- if I remove main file, symlink is not working

## Hardlink
 - ln /home/vijay/aws/ec2/security.txt sg.txt
 - ln **source file full path and destination file**
   - **inode has same both file**
     - ls -li  /home/vijay/aws/ec2/security.txt
       **16237** -rw-r--r-- 2 vijay vijay 18 Nov 17 01:58 /home/vijay/aws/ec2/security.txt
     - ls -li sg.txt
       **16237** -rw-r--r-- 2 vijay vijay 18 Nov 17 01:58 sg.txt
- Hardlink
 1. inode is same for hard link
 2. hardlink is used for backup
 3. even we delete file, it will not be deleted completely untill all the rederene
 4. hard link will not work folders

 DK vs JRE

Sivakumar Reddy Me....

JDK -> Java development kit -> extra tools and packages

JRE -> Java runtime envronment
JRE < JDK

JDK JRE + extra tools for development

## maven lifecycle
**source code** -> install dependencies -> compile -> test cases -> bytecode (packing the applicaton)

**build tool** -> package the code into artifact

**it is a sequential process execution to build the project with different phases like**

  - **cleaning the old builds**
  - **install dependencies**
  - **compile the source code**
  - **run the test cases**
  - **package the application -> bytecode**
  - **install the application**