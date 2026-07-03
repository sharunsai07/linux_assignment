# Command Explanations - Question 3

- `echo "Linux Link Analysis" > original.txt`: I created a new file and used redirection to write a test string into it for link behavior validation.
- `ln original.txt hardlink.txt`: I created a hard link to the original file, generating a second directory entry that points to the same inode.
- `ln -s original.txt symlink.txt`: I created a symbolic link, which creates a separate file entry that points to the original file path.
- `ls -li original.txt hardlink.txt symlink.txt`: I displayed the files with inode numbers to confirm the original file and hard link share the same inode, while the symbolic link uses a different inode.
- `stat original.txt`: I inspected the original file metadata, including inode number, link count, ownership, and timestamps.
- `stat hardlink.txt`: I inspected the hard link metadata to verify it shares the same inode and link count as the original file.
- `stat symlink.txt`: I examined the symbolic link metadata to confirm it points to `original.txt` and has its own inode.
- `rm original.txt`: I deleted the original file to observe the effect on both the hard link and the symbolic link.
- `cat hardlink.txt` & `cat symlink.txt`: I attempted to read from both links, observing that the hard link still returned the file content while the symbolic link failed with "No such file or directory".
