# Get Next Line

## Project Overview
Get Next Line is a project that involves programming a function to read a line from a file descriptor. This function allows efficient line-by-line reading, leveraging static variables to maintain state between calls.

## Features
- **Reads from a file descriptor one line at a time**
- **Supports standard input and file reading**
- **Handles various buffer sizes dynamically**
- **Includes helper functions for efficient string manipulation**

## Directory Structure
```
./
├── Mandatory_part
    ├──
    ├── get_next_line.c
    ├── get_next_line.h
    ├── get_next_line_utils.c
./
├── Bonus_part
    ├── get_next_line_bonus.c
    ├── get_next_line_bonus.h
    ├── get_next_line_utils_bonus.c
```

## Installation & Usage
1. Clone the repository:
   ```sh
   git clone https://github.com/ElmehdiBennix/Get_Next_Line_42.git
   cd Get_Next_Line_42
   ```
2. Compile with a custom buffer size:
   ```sh
   cc -Wall -Wextra -Werror -D BUFFER_SIZE=42 get_next_line.c get_next_line_utils.c -o gnl_test
   ```
3. Use in a program:
   ```c
   #include "get_next_line.h"
   int fd = open("file.txt", O_RDONLY);
   char *line = get_next_line(fd);
   ```

## Mandatory Implementation
- `char *get_next_line(int fd);` function to return a line from a file descriptor.
- Reads efficiently and handles dynamic buffer sizes.
- Properly frees allocated memory to avoid leaks.

## Bonus Features
- **Multiple File Descriptor Handling**: Allows reading from different FDs simultaneously.
- **Single Static Variable**: Implements logic using only one static variable.

## Notes
- No usage of `lseek()` or global variables.
- The function must work correctly for different buffer sizes.

