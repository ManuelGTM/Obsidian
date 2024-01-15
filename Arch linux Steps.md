### Instalation requeriments

- Burned Usb with arch Iso
- A computer
- Internet conection
- Great amount of patience

### Steps to Install 

#### Verify internet Connection

``` Bash 
Ping google.com
```

#### Update time zone

``` Bash
timedatectl set-timezone America/Santo_Domingo
```

##### Disk partitioning

We need to list all the devices to make the partitions

``` Bash
fdisk -l
```

- /dev/sda is a typical name for devices

We mount the device to make the partition:

``` Bash
mount /dev/sda
```

In order to make a fully functional system we need to make 3 partitions:

- The EFI Partition (Minimum 550M of Space)
- The SWAP Partition (Minimun 2G of space)
- The Linux File System (All the space you need)

To create a partition we press the n button and we define the number of the partition, the sector in memory and the amount of space needed for it.

For example:

``` Bash

{The EFI Partition}

Partition number(1-128): 1
First sector 1234312-4567, default): {Hit enter}
Last Sector <- this is for memory space: +550M

-- Press n again --

{The Swap Partition}

Partition number(1-128): 2
First sector 1234312-4567, default): {Hit enter}
Last Sector <- this is for memory space: +2G

-- Press n again --

Partition number(1-128): 3
First sector 1234312-4567, default): {Hit enter}
Last Sector <- this is for memory space: +100G or
{hit enter if you want all the remaining space}

```

Now we need to define the type of the partitions with the t button:

EFI Partition: 1 for EFI type

Swap Partition: 19 for SWAP type

Linux FileSystem: Leave it as it is.

Press w to save the changes
##### Make the file systems

