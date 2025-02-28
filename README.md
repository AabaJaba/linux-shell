# Custom Shell Utilities

This project implements basic shell utilities in C, including commands for file and directory management. Each utility mimics standard Linux commands with similar functionality and options.

## Included Commands

### 1. `mkdir` - Create directories

- **Usage:** `mkdir [-v|-p] directory_name`
- **Options:**
  - `-v` : Verbose output, confirms directory creation
  - `-p` : Creates parent directories as needed

### 2. `rm` - Remove files

- **Usage:** `rm [-i|-I] file_name`
- **Options:**
  - `-i` : Interactive mode, asks before deleting each file
  - `-I` : Asks once before deleting all files

### 3. `ls` - List directory contents

- **Usage:** `ls [-a|-l]`
- **Options:**
  - `-a` : Show hidden files
  - `-l` : Display in list format

### 4. `cat` - Display file contents

- **Usage:** `cat [-n|-e] file_name`
- **Options:**
  - `-n` : Show line numbers
  - `-e` : Highlight end of lines with `$`

### 5. `date` - Display current date and time

- **Usage:** `date`

### 6. `pwd` - Print working directory

- **Usage:** `pwd [-L|-P]`
- **Options:**
  - `-L` or `-l` : Print logical path
  - `-P` or `-p` : Print physical path

### 7. `echo` - Print arguments

- **Usage:** `echo [string]`
- **Options:**
  - `--help` : Display help menu
  - `*` : Print directory contents

### 8. `cd` - Change directory

- **Usage:** `cd directory_name`

### 9. `exit` - Exit the shell

- **Usage:** `exit`

## Compilation and Execution

To compile all utilities:

```sh
make
```

To run the custom shell:

```sh
./test
```

## Notes

- The `test` program provides a command-line interface supporting all custom commands.
- Commands are executed via `execv`, and invalid inputs produce error messages.
- Some commands utilize `pthread` for threading (e.g., `date&t`).

## Author

Developed by Navnoor Singh as a custom shell utility project.

