# Command Explanations - Question 5

- `mkdir Storage`: I created a dedicated Storage investigation directory within the current workspace.
- `cd Storage`: I moved into the Storage directory to run the analysis commands from the investigation folder.
- `lsblk`: I listed block devices attached to the system, identifying the disks and any mounted partitions.
- `df -h`: I displayed mounted file systems and their disk usage in human-readable form, including Linux root and WSL mount points.
- `df -i`: I inspected inode usage for mounted file systems to verify inode availability across Linux and WSL mounts.
- `mount | head -20`: I showed the first 20 mount points and options, confirming the root filesystem type, overlay mounts, and WSL-specific mounts.
- `vi Storage_Assessment_Report.txt`: I documented the storage analysis findings in the report file and saved the results.
