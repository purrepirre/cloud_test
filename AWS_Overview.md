# AWS Overview

## How to add more disk to instance

from [AWS Using Volumes](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-using-volumes.html)

- Create new volume in AWS console
- Attach volume to correct instance
	- Note that name can change depending on instance type
- Use *lsblk* command to see available devices
- Use *sudo file -s /dev/xxxx* to check file system on device
	- if "data" there is no file system in place
- To create filesystem:
	- sudo mkfs -t ext4 device_name