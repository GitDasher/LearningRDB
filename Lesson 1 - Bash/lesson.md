# Lesson 1 - Bash

## Bash Commands:
- echo "text" : Print "text" in the terminal
  - ">>" : Used to put text in a file
- pwd : **P**rint **W**orking **D**irectory
- ls -<flag> <directory_name>: **L**i**S**t the items in the current directory in accordance with the flags given
  - Flags
    1. -l : Long list format
    2. -all/-a : List all files
- cd <directory_name> : **C**hange **D**irectory to directory <directory_name>
- cd .. : **C**hange **D**irectory to previous directory
- more <file_name> : To view the contents of a file step by step
- cat <file_name> : To view all the contents of a file at once
- clear : Clear the terminal window
- mkdir <directory_name> : **M**a**K**e**DIR**ectory <directory_name> in the current directory
- touch <file_name> : Create a file with name <file_name>
- cp <file_name> <destination_name> : **C**o**P**y <file_name> into <destination_name>
- rmdir <directory_name> : **R**e**M**ove **DIR**ectory <directory_name>
- rm <filename> : **R**e**M**ove <filename>
  - Flags
    1. -r : Recursively remove, used to remove directories and its contents
- mv <filename> <new_filename> : Used to **M**o**V**e file to a new destination, or rename it
- find : Used to **FIND** things or a view a family tree
  - Flags
    1. -name : Used to find a file under the name <file_name>