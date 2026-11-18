# Secure File Locker in C

A menu-driven C application for managing files with master-password
authentication and basic XOR-based encryption. This project demonstrates
file handling, structures, dynamic memory allocation, and other core C
programming concepts.

## Features

-   Set and verify a master password
-   Create and write files
-   Store file contents in the demo's encrypted format
-   Open and read saved files
-   List saved files with size and timestamp
-   Delete stored files
-   Change the master password and re-encrypt stored files
-   Record activity in an access log

## Requirements

-   A C compiler, such as GCC
-   Windows or a POSIX-compatible operating system

## Compile

Using GCC:

``` bash
gcc main.c -o secure_file_locker
```

## Run

On Linux/macOS:

``` bash
./secure_file_locker
```

On Windows:

``` bash
secure_file_locker.exe
```

On the first run, the program asks you to create a master password. On
later runs, enter that password to access the menu.

## Data Storage

The program creates a `vault` directory to store:

-   `master.dat` --- the password salt and demo checksum
-   `index.dat` --- metadata for saved files
-   `<filename>.enc` --- each file's header and encrypted content
-   `access.log` --- activity timestamps

## Important Security Note

This is an educational demonstration, not production-grade security. The
XOR stream and custom password checksum are not secure cryptographic
mechanisms. Do not use this program to protect sensitive or confidential
information.

## License

Add a license file if you intend to publish or distribute this project.
