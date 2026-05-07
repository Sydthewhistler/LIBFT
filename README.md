<div align="center">

# libft

**A custom C standard library — built from scratch.**

</div>

---

## Overview

`libft` is the foundational project of the 42 curriculum. The goal is to reimplement a subset of the C standard library — along with a set of additional utility functions — without relying on any existing library.

This project establishes the bedrock of every subsequent 42 project. Rather than calling `strlen`, `split`, or `printf` from libc, students build, own, and extend their own library throughout the entire cursus.

---

## Structure

```
libft/
├── Makefile
├── libft.h
├── ft_*.c          # All source files
└── README.md
```

The library is compiled into a static archive `libft.a`, which can be linked into any future project with:

```bash
make
gcc main.c -L. -lft -o program
```

---

## Makefile Targets

| Target | Description |
|--------|-------------|
| `make` / `make all` | Compile the library into `libft.a` |
| `make clean` | Remove object files |
| `make fclean` | Remove object files and `libft.a` |
| `make re` | Full recompile from scratch |
| `make bonus` | Compile with bonus linked-list functions |


---

## What This Project Teaches

`libft` is far more than a reimplementation exercise. It builds the following fundamental skills:

- **Memory management** — manual allocation, deallocation, and handling edge cases without safety nets
- **Pointer arithmetic** — navigating raw memory and understanding how strings and arrays actually work in C
- **Code robustness** — handling `NULL` inputs, zero sizes, overlapping regions, and undefined behavior
- **Modular C design** — separating concerns cleanly across many `.c` files with a shared header
- **Static libraries** — understanding how object files are archived and linked into a binary
- **The Norm** — writing readable, consistent code under 42's strict style rules (`norminette`)

The resulting `libft.a` is carried forward and extended across the entire 42 cursus — used in projects like `ft_printf`, `get_next_line`, `push_swap`, `minishell`, and beyond.

---

## Usage

```bash
# Clone the repository
git clone https://github.com/Sydthewhistler/libft.git
cd libft

# Build the library
make

# Link against your project
gcc -Wall -Wextra -Werror main.c -L. -lft -I. -o program
```

---

## Requirements

- **Compiler:** `gcc` with flags `-Wall -Wextra -Werror`
- **Standard:** C99 or later
- **Norm:** [Norminette v3](https://github.com/42School/norminette) compliant
- **No forbidden functions:** only the explicitly allowed libc calls per function

---

## Author

**scavalli** — [GitHub](https://github.com/Sydthewhistler) · 42 School