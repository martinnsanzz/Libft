<h3 align="center">
  <em>Your very first own library</em>
</h3>

## ⚠️ Disclaimer

- **Full Portfolio:** This repository focuses on this specific project. You can find my entire
42 curriculum 👉 [here](https://github.com/martinnsanzz/42-Curriculum).
- **Subject Rules:** I strictly follow the rules regarding 42 subjects; I cannot share the PDFs,
but I explain the concepts in this README.
- **Archive State:** The code is preserved exactly as it was during evaluation (graded state).
I do not update it, so you can see my progress and mistakes from that time.
- **Academic Integrity:** I encourage you to try the project yourself first. Use this repo only
as a reference, not for copy-pasting. Be patient, you will succeed.

## 📂 Description
**Libft** is the first project from the 42 curriculum. The goal is to recreate the core
behaviour of standard C library functions (libc), and to create a set of utility
functions that can be reuse throughout the entire curriculum since  we are not allowed to use
most standard C libraries such as `<string.h>` or `<stdlib.h>`.

We will also learn to create a `Makefile` to automate compilation of `.c` files and generate a
**static library** (`libft.a`) and the use of header files (`.h`) to organize code efficiently
and declare prototypes and structs.

## 🔷 Usage

### Clone repository
To use this project you first need to clone the repository in your directory.

```bash
git clone git@github.com:martinnsanzz/Libft.git
```

### Run make
To compile this project you need to write `make` in the terminal, this will compile all .c files
and create libft.a at the root of the repository

```bash
make
```

### How to use the libray
To use the library in your project you must include the header on top of the file.

```c
#include "libft.h"
```

Once you use the library within your file you need to link the library with the source file
during compilation file as follow:

The requirements for this project are as follows:
- Compiler: cc with flags -Wall -Wextra -Werror
- Archiver: ar (use of libtool is forbidden)
- Standard: C89/C99 compatible (no restrict qualifier in prototypes)

```bash
cc -Wall -Wextra -Werror your_main.c libft.a && ./a.out
```

> [!WARNING]
> The compilation will fail if some functions are missing from your library.

## 🖱️ Function list

### 🧱 Memory
| Function | Function |
| :--- | :--- |
| `ft_memset` | `ft_memchr` |
| `ft_bzero` | `ft_memcmp` |
| `ft_memcpy` | `ft_calloc` |
| `ft_memmove` | `ft_strdup` |

### 🔡 String Manipulation
| Function | Function | Function |
| :--- | :--- | :--- |
| `ft_strlen` | `ft_strncmp` | `ft_split` |
| `ft_strlcpy` | `ft_strnstr` | `ft_strmapi` |
| `ft_strlcat` | `ft_substr` | `ft_striteri` |
| `ft_strchr` | `ft_strjoin` | |
| `ft_strrchr` | `ft_strtrim` | |

### 🔢 Converters & Checkers
| Function | Function |
| :--- | :--- |
| `ft_isalpha` | `ft_toupper` |
| `ft_isdigit` | `ft_tolower` |
| `ft_isalnum` | `ft_atoi` |
| `ft_isascii` | `ft_itoa` |
| `ft_isprint` | |

### 📠 File Descriptor
| Function |
| :--- |
| `ft_putchar_fd` |
| `ft_putstr_fd` |
| `ft_putendl_fd` |
| `ft_putnbr_fd` |

### ⛓️ Linked List
| Function | Function |
| :--- | :--- |
| `ft_lstnew` | `ft_lstdelone` |
| `ft_lstadd_front` | `ft_lstclear` |
| `ft_lstsize` | `ft_lstiter` |
| `ft_lstlast` | `ft_lstmap` |
| `ft_lstadd_back` | |

## 📖 Resources
For the creation of this project the following resources were used:
- Linux man pages: Official man pages for the creation of part 1 functions
- W3Schools & GeeksforGeeks: Easy to understand guides for c topics such as pointers, memory, syntax, linked lists, etc...
- [Neso Academy](https://www.youtube.com/playlist?list=PLBlnK6fEyqRj9lld8sWIUNwlKfdUoPd1Y): For dynamic memory allocation, in depth linked list understanding.
- Stack overflow forums: For specific questions in C programming

*AI Usage*
AI (Claude - Anthropic) and (Chatgpt - Open AI) was used in this project for the following things:
- As a teacher: To understand complex concepts such as (e.g., what was overlaping for memmove, returning value of strlcat, low-level memory concepts).
- Writing tester functions: Creating personal testers to get visual behaviour on the terminal and find;
	1) Flaws in my code
	2) Segmentation fault errors
	3) Edge cases (NULL input, empty strings, single character delimiters, etc)
	4) Help me debug and see how my code runs
- Comments: In my personal github (where my tester can be found), all functions have a block comment explaining what it does, parameters pass, return values, behaviour (When need for complex functions), and extra notes. Note this block header have been remove for the submission due to the moulinette not accepting comments.

AI was *NOT* used to write or generate any code. All function bodies were written by myself.