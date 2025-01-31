# libft

⚠️ **Information:** This repository has two branches: the original version and an "LTS" version, which is continuously updated throughout my progress at 42.

Libft is a custom implementation of the C standard library functions, created as part of the 42 curriculum. This library provides fundamental utilities for string manipulation, memory handling, linked lists, and more.

## Table of Contents

- [Usage](#usage)
- [Functions](#functions)
- [Compilation](#compilation)
- [License](#license)

## Usage

Include `libft.h` in your project:

```c
#include "libft.h"
```

Clone this repository inside your project directory:

```sh
git clone https://github.com/Eutrius/libft.git
```

Modify your Makefile to use `libft`:

```make
LIBFT_PATH=libft
LIBFT=$(LIBFT_PATH)/libft.a
LIBFT_FLAGS= -L$(LIBFT_PATH) -lft

CFLAGS = -Wall -Werror -Wextra -I$(LIBFT_PATH)

$(NAME): $(LIBFT) $(OBJECTS)
	$(CC) $(CFLAGS) -o $@ $^ $(LIBFT_FLAGS)

$(LIBFT):
	$(MAKE) -C $(LIBFT_PATH)

clean:
	$(RM) $(OBJECTS)
	$(MAKE) -C $(LIBFT_PATH) clean

fclean:
    $(RM) $(OBJECTS)
	$(RM) $(NAME)
	$(MAKE) -C $(LIBFT_PATH) fclean

```

## Functions

Libft includes the following function categories:

- **Libc functions**: `ft_strlen`, `ft_strcpy`, `ft_memset`, etc.
- **Memory management**: `ft_calloc`, `ft_memmove`, etc.
- **String utilities**: `ft_strjoin`, `ft_split`, `ft_itoa`, etc.
- **Linked list utilities**: `ft_lstnew`, `ft_lstadd_front`, `ft_lstmap`, etc.
- **Others**: `ft_print`, `ft_pointcmp`, `ft_strslen`, `ft_strscat`, etc.
- **Also**: `ft_printf`, `get_next_line`, `get_next_line_fds`

For a full list, see `libft.h`.

## Compilation

To compile:

```sh
make
make all
```

To clean object files:

```sh
make clean
```

To remove everything (including `libft.a`):

```sh
make fclean
```

To recompile:

```sh
make re
```

## License

This project is part of the 42 curriculum and follows its academic policies.
