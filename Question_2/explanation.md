# Command Explanations - Question 2

- `umask`: I checked the current umask value to understand the default permissions assigned to newly created files and directories on the system.
- `mkdir ProjectWorkspace`: I created the main project directory under the current working path.
- `cd ProjectWorkspace`: I changed into the project workspace directory to continue setup inside it.
- `mkdir docs src backups`: I created three subdirectories within the workspace for documentation, source code, and backups.
- `touch docs/project_plan.txt`: I created a placeholder project plan file inside the docs directory.
- `touch src/main.c`: I created an empty C source file inside the src directory.
- `ls -R`: I executed this to display the complete recursive directory structure, showing backups, docs, logs, src, testdir, and a top-level testfile.
- `ls -l`: I ran this to inspect the permission and ownership metadata for all top-level files and directories.
- `chmod 700 docs`: I restricted the docs directory so only the owner can access its contents.
- `chmod 600 docs/project_plan.txt`: I restricted the project plan file so only the owner can read and write it.
- `ls -ld docs` and `ls -l docs`: I used these commands to confirm the effective directory and file permissions after modification.
