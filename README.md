📌 Project Title:
Custom Implementation of ls -lias Command using C

📚 Description:
This project provides a user-defined implementation of the ls command found in Unix/Linux systems. It mimics common options such as:

-l : Long listing format

-i : Print inode number

-a : Show hidden files (starting with .)

-s : Show allocated file size in blocks

This C program utilizes Linux system calls (opendir, readdir, stat, etc.) and structures like struct stat, struct dirent to replicate these functionalities.

⚙ Compilation:
To compile the code, use the gcc compiler:

bash
Copy
Edit
gcc -o myls myls.c
▶ Usage:
bash
Copy
Edit
./myls                    # Lists current directory without hidden files
./myls -a                 # Lists all files including hidden ones
./myls -l                 # Long format listing
./myls -li                # Long format with inode numbers
./myls -lias              # Long listing + inodes + all files + block size
./myls <directory_name>   # Lists the given directory
./myls -l <directory>     # Apply flags to given directory
🧪 Sample Output:
bash
Copy
Edit
./myls -lias

in function . lias
56789 d rwxr-xr-x  2 1000 1000 4096 Jun 21  Documents
12345 - rw-r--r--  1 1000 1000  123 Jun 19  README.txt
🛠 Features:
Handles multiple flags (combined or separate)

Uses stat() and ctime() for metadata

Handles hidden files with -a option

Displays file permissions and types in ls -l format

Shows inode with -i, block size with -s

🧠 Concepts Used:
Directory Traversal

File Metadata Extraction

Bitwise Operations for Permission Display

Time Formatting

DIR, stat, ctime, strchr, readdir, etc.

🚀 To-Do / Improvements:
Add recursive -R option

Color output for file types

Sorting options (-t, -S, etc.)

Handle symbolic links properly
