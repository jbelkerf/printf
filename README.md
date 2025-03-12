# ft_printf

ft_printf is a custom implementation of the standard `printf` function in C. It is a variadic function capable of handling different format specifiers and printing formatted output to the standard output. This project is part of the 42 curriculum.

## Features

- Supports various format specifiers:
  - `%c` : Prints a character
  - `%s` : Prints a string
  - `%d` / `%i` : Prints a decimal (integer)
  - `%u` : Prints an unsigned integer
  - `%p` : Prints a pointer address
  - `%x` / `%X` : Prints a number in hexadecimal (lowercase/uppercase)
  - `%%` : Prints a percentage symbol
- Handles variadic arguments
- Custom implementation without using standard I/O functions like `printf`

## Installation

To compile and use `ft_printf`, clone this repository and run:

```sh
make
```

This will generate the `libftprintf.a` static library.

## Usage

To use `ft_printf` in your project, include it in your compilation:

```sh
gcc your_program.c -L. -lftprintf -o your_program
```

Or in a Makefile:

```make
LIBFTPRINTF = ./libftprintf.a

all:
	gcc -o my_program main.c $(LIBFTPRINTF)
```

## File Structure

- `ft_printf.h` – Header file with function prototypes
- `Makefile` – Compilation rules
- `libftprintf.a` – Compiled static library
- Source files:
  - `printf.c` – Core function handling format parsing and variadic arguments
  - `print_char.c` – Handles character output (`%c`)
  - `print_str.c` – Handles string output (`%s`)
  - `print_dec.c` – Handles integer output (`%d`, `%i`)
  - `print_unsigned.c` – Handles unsigned integer output (`%u`)
  - `print_pointer.c` – Handles pointer output (`%p`)
  - `print_lhexa.c` – Handles lowercase hexadecimal output (`%x`)
  - `print_uhexa.c` – Handles uppercase hexadecimal output (`%X`)
  - `check_flag.c` – Checks format specifiers
  - `main.c` – Example main file (for testing purposes)

## Example Usage

```c
#include "ft_printf.h"

int main() {
    ft_printf("Hello, %s!\n", "world");
    ft_printf("Character: %c\n", 'A');
    ft_printf("Number: %d\n", 42);
    ft_printf("Pointer: %p\n", &main);
    return 0;
}
```

## Contributing

If you want to contribute, fork the repository, make changes, and submit a pull request.

## License

This project is open-source under the MIT License.

## Author

Developed by Jaouad Belkerf (jbelkerf) as part of the 42 curriculum.

