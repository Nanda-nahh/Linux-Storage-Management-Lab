# Linux Storage Management Project

## Overview

This project demonstrates fundamental Linux storage administration tasks, including disk detection, partition creation, filesystem creation, mounting storage, and storage verification.

The project was performed on a Red Hat Enterprise Linux-based virtual machine as part of a Linux System Administration learning roadmap.

## Objectives

* Add and detect a new storage device
* Create a disk partition
* Create an XFS filesystem
* Mount the filesystem to a directory
* Verify storage availability and usage
* Generate a storage report for documentation

## Environment

* Operating System: Red Hat Enterprise Linux
* Virtualization Platform: VirtualBox
* Additional Disk Size: 5 GB
* Filesystem Type: XFS

## Tasks Performed

### 1. Verify Available Storage

Used the following commands to inspect existing storage devices and partitions:

```bash
lsblk
fdisk -l
```

### 2. Create a New Partition

Created a primary partition on the newly added disk.

```bash
fdisk /dev/sdb
```

### 3. Create an XFS Filesystem

Formatted the partition with the XFS filesystem.

```bash
mkfs.xfs /dev/sdb1
```

### 4. Verify Filesystem Information

Checked filesystem details and UUID information.

```bash
blkid /dev/sdb1
```

### 5. Create a Mount Point

Created a directory to serve as the mount point.

```bash
mkdir /data
```

### 6. Mount the Filesystem

Mounted the new filesystem to the system.

```bash
mount /dev/sdb1 /data
```

### 7. Verify Storage Configuration

Confirmed successful mounting and storage availability.

```bash
df -h
lsblk
```

## Project Outcome

Successfully added and configured a new storage device, created an XFS filesystem, mounted it to the Linux filesystem hierarchy, and verified its functionality through storage and filesystem validation commands.

## Skills Demonstrated

* Linux Storage Administration
* Disk and Partition Management
* Filesystem Creation
* Storage Mounting
* Filesystem Verification
* Basic System Documentation

## Files Included

* `README.md` – Project documentation
* `storage_report.txt` – Storage configuration report generated during the lab

## Author

Nandana Mohan J
Linux System Administration Learning Project

