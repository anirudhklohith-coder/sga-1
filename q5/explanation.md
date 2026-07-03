# Q5 Explanation

- I used `lsblk` to list the available block devices and their partitions. This helped identify the storage devices visible to the system.
- I inspected mounted filesystems with `mount` and reviewed storage capacity with `df -h`. The output showed that the main filesystems still have adequate free space.
- I checked inode usage with `df -i` to confirm whether the filesystems were close to running out of inode entries. The values were low, so inode exhaustion was not a current concern.
- Based on the observations, the main recommendations are to monitor disk usage regularly, remove temporary files as needed, and archive old logs to keep storage usage under control.
