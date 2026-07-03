# Command Explanations - Question 4

- `mkdir IOInvestigation`: I created a dedicated directory for the I/O investigation tasks.
- `cd IOInvestigation`: I changed into the new investigation directory.
- `echo "Linux I/O Test" > log.txt`: I created a test file named `log.txt` to use in the I/O investigation.
- `lsof log.txt`: I checked whether `log.txt` was open by any running process.
- `lsof | head`: I listed the first open file records from the system to observe active processes and their file descriptors, including permission-denied `/proc` entries.
- `ulimit -a`: I displayed the shell resource limits, including the number of open files, max user processes, stack size, and other I/O-related constraints.
- `echo "Hello World" > output.txt`: I redirected standard output into `output.txt` to verify stdout redirection.
- `cat output.txt`: I read the file back to confirm the content was written successfully.
- `ls nonexistentfile 2> error.txt`: I redirected the stderr from a failing `ls` command into `error.txt`.
- `cat error.txt`: I confirmed the captured error message was `ls: cannot access 'nonexistentfile': No such file or directory`.
- `ls log.txt nonexistentfile > combined.txt 2>&1`: I combined stdout and stderr into `combined.txt`, capturing both the existing file name and the error in one file.
- `cat combined.txt`: I verified that the combined output file contained both `log.txt` and the error message from the failed `ls` command.
